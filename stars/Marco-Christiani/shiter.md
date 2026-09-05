---
repo: Marco-Christiani/shiter
url: 'https://github.com/Marco-Christiani/shiter'
homepage: null
starredAt: '2026-08-10T21:35:24Z'
createdAt: '2026-08-09T19:35:57Z'
updatedAt: '2026-08-10T21:35:25Z'
language: Zig
license: MIT
branch: main
stars: 2
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-09-05T23:58:27.381Z'
description: Iterate on shell commands in a retained terminal viewport
tags: []
---

# shiter

Shell commands often take a few attempts to get right. Each attempt normally
means recalling the command, navigating back to the edit point, changing it,
and running it again. The intermediate commands remain in shell history.

`shiter` keeps one command and its cursor position above a retained terminal
viewport. You can edit and rerun the command without adding each intermediate
version to the parent shell's history. When you leave, the final command
returns to the original prompt.

Without shiter:
![Before: Iterating on a command without shiter](demo/problem.gif)

With shiter:
![After: Iterating on a command with shiter](demo/shiter.gif)

## Try it

The default Nix app starts a temporary interactive instance of `$SHELL` with
shiter installed and Alt-R bound.

```sh
nix run github:Marco-Christiani/shiter
# Or explicitly request one
nix run github:Marco-Christiani/shiter#<fish/bash/zsh>
```

Exit the temporary shell to return to the original one.

## Home Manager

Add shiter as a flake input:

```nix
inputs.shiter.url = "github:Marco-Christiani/shiter";
```

Import its module in your Home Manager configuration:

```nix
{
  inputs,
  ...
}: {
  imports = [inputs.shiter.homeModules.default];
  programs.shiter.enable = true;
}
```

The module installs shiter and configures Bash, Fish, and Zsh according to the
corresponding `home.shell.enable*Integration` defaults. Each integration can be
overridden under `programs.shiter`:

```nix
programs.shiter = {
  enable = true;
  enableBashIntegration = false;
  enableFishIntegration = true;
  enableZshIntegration = false;
  fishKeyBinding = "alt-r";
  settings = {
    scrollback_bytes = 1000000;
    completion_timeout_ms = 750;
    revision_history_limit = 100;
    post_exit = {
      idle_timeout_ms = 500;
      total_timeout_ms = 4000;
      output_limit_bytes = 16777216;
    };
    appearance = {
      prompt = {
        text = "run>";
        foreground = "bright_cyan";
        bold = true;
      };
      status.dim = true;
      selection = {
        foreground = "black";
        background = "bright_cyan";
        bold = true;
        reverse = false;
      };
      scroll = {
        mode = "progress";
        max_width = 20;
        primary = {
          glyph = "━";
          style.foreground = "bright_blue";
        };
        secondary = {
          glyph = "─";
          style.foreground = "bright_black";
        };
      };
    };
    bindings = {
      up = "previous_revision";
      down = "next_revision";
      ctrl-p = "scroll_line_up";
      ctrl-n = "scroll_line_down";
    };
  };
};
```

The default binding is Alt-R. The `bashKeyBinding`, `fishKeyBinding`, and
`zshKeyBinding` options accept shell-specific key names or `null` to load the
widget without binding it.

## Build from source

For a local checkout:

```sh
# without nix
zig build
./zig-out/bin/shiter -- 'printf "hello\n"'

# with nix
nix build
./result/bin/shiter -- 'printf "hello\n"'
```

`shiter` runs commands with `$SHELL -c`. It falls back to `/bin/sh` when
`SHELL` is unset or empty.

## Shell integration

The interface reads and writes `/dev/tty`. Standard output contains only the
final edited command, which lets a shell widget capture it without capturing
the interface.

### Fish

```fish
shiter --shell-integration fish | source
# Bind to Alt-R, change as desired
bind \er __shiter_widget
```

### Bash

```bash
source <(shiter --shell-integration bash)
# Bind to Alt-R, change as desired
bind -x '"\er":__shiter_widget'
```

### Zsh

```zsh
source <(shiter --shell-integration zsh)
# Bind to Alt-R, change as desired
bindkey '^[r' shiter-widget
```

## Direct Usage

```text
shiter [--set key=value] [--bind chord=action] [--] [initial command]
shiter --dump -- <command>
shiter --shell-integration <fish|bash|zsh>
```

Enter runs the current command. Editing remains available while a command is
active, but Enter does not start a second run until the first finishes.

Up and Down scroll the retained output by one row. Page Up and Page Down scroll
by one viewport, while Ctrl-Home and Ctrl-End jump to its bounds. Scrolling away
from the bottom pauses output following until the viewport returns to the
bottom.

Ctrl-P and Ctrl-N select commands already run during the current shiter
session. Moving past the newest command restores the draft that was present
before revision navigation.

The editor supports printable Unicode and Readline-style bindings. Alt-B and
Alt-F move by words. Alt-D and Ctrl-W delete words. Ctrl-U and Ctrl-K delete to
the beginning and end. Left, Right, Home, End, Backspace, Delete, Ctrl-A,
Ctrl-D, and Ctrl-E retain their usual editing behavior.

Ctrl-C sends one `SIGINT` to an active command and exits when idle. Escape or
Alt-R exits, terminating an active command if needed. Ctrl-Z is unbound.

### Completion and shell scope

Tab completion is available when `$SHELL` is Fish. Shiter starts a fresh Fish
process and asks Fish's supported `complete -C --escape` interface for the
buffer through the cursor. A unique result replaces the current token. When
there are several results, Tab applies the first and later Tab presses cycle
through them. The result list uses the output viewport below the prompt and
keeps the selected candidate visible. The footer shows when more candidates
are above or below the visible page. Shift-Tab and Up or Down move through the
list. Page Up and Page Down move by a viewport, while Ctrl-Home and Ctrl-End
jump to the first and last candidate. Enter keeps the selected completion,
while Escape cancels the list and exits as usual.

Completion waits at most 500 ms and does not block editing. Any non-Tab key
cancels a pending query or candidate cycle before it performs its normal
action. Bash and Zsh completion are not supported in this version.

Each run starts a fresh `$SHELL -c` process with a copy of the environment.
Exported variables and the working directory are available. Aliases and
functions defined only in the active shell session are not transferred to the
child process. For Fish, installed completion definitions, configuration, and
functions saved on Fish's autoload path are available to the new process.
Session-local aliases and unsaved functions are not transferred.

### Key configuration

Each chord can be assigned a different action or set to `null` to disable it in
`$XDG_CONFIG_HOME/shiter/config.json`, or `$HOME/.config/shiter/config.json`
when `XDG_CONFIG_HOME` is unset:

```json
{
  "scrollback_bytes": 1000000,
  "completion_timeout_ms": 750,
  "revision_history_limit": 100,
  "post_exit": {
    "idle_timeout_ms": 500,
    "total_timeout_ms": 4000,
    "output_limit_bytes": 16777216
  },
  "appearance": {
    "prompt": { "text": "run>", "foreground": "bright_cyan", "bold": true },
    "status": { "dim": true },
    "selection": {
      "foreground": "black",
      "background": "bright_cyan",
      "bold": true,
      "reverse": false
    },
    "scroll": {
      "mode": "progress",
      "max_width": 20,
      "primary": {
        "glyph": "━",
        "style": { "foreground": "bright_blue" }
      },
      "secondary": {
        "glyph": "─",
        "style": { "foreground": "bright_black" }
      }
    }
  },
  "bindings": {
    "up": "previous_revision",
    "down": "next_revision",
    "ctrl-p": "scroll_line_up",
    "ctrl-n": "scroll_line_down",
    "escape": null
  }
}
```

`scrollback_bytes` limits Ghostty's retained terminal page storage and defaults
to `10000`.

`completion_timeout_ms` limits a Fish completion request and defaults to `500`.
Increase it when a useful completion takes longer to load. `revision_history_limit`
limits commands retained for revision navigation. It defaults to `0`, which keeps
all commands for the current shiter session.

`post_exit` bounds output draining after a command's direct child exits. Its
defaults are `250` ms idle time, `2000` ms total time, and `8388608` bytes.
Increase these limits for commands that intentionally leave descendants writing
to the PTY after the direct child exits.

`appearance` styles only Shiter-owned interface elements: `prompt`, `status`,
and the selected completion `selection`. Set the prompt label with
`appearance.prompt.text`. Each style accepts `foreground`,
`background`, `bold`, `dim`, `underline`, and `reverse`. Colors are `black`,
`red`, `green`, `yellow`, `blue`, `magenta`, `cyan`, `white`, and their
`bright_` variants. The default prompt is bold and the default completion
selection uses reverse video.

`appearance.scroll` controls the indicator for scrollable output and completion
lists. Its default `scrollbar` mode keeps the viewport-sized moving thumb.
Set `mode` to `progress` for a filled meter, or `text` for position text alone.
`max_width` limits the indicator to that many cells. `show_position` and
`show_percent` hide the numeric position and output percentage. `primary` and
`secondary` configure one-cell glyphs and optional styles. They represent the
thumb and track in scrollbar mode, or filled and unfilled portions in progress
mode. The examples use `━` and `─` with blue and bright-black styling, similar
to a Rich progress meter.

### Command-line overrides

`--set key=value` overrides a configuration setting for one interactive run.
`--bind chord=action` overrides one binding, and `null` unbinds it. These flags
override the configuration file and appear before the command. Use `--` before
a command that starts with a dash.

```sh
shiter --set completion_timeout_ms=750 --set appearance.prompt.text='run>' \
  --set appearance.prompt.foreground=bright_cyan \
  --set appearance.scroll.mode=progress \
  --set appearance.scroll.primary.glyph=━ \
  --set appearance.scroll.secondary.glyph=─ \
  --set appearance.scroll.primary.style.foreground=bright_blue \
  --set appearance.scroll.secondary.style.foreground=bright_black \
  --bind tab=null -- git status
```

The supported `--set` keys are `scrollback_bytes`, `completion_timeout_ms`,
`revision_history_limit`, `post_exit.idle_timeout_ms`,
`post_exit.total_timeout_ms`, `post_exit.output_limit_bytes`, and every style
field under `appearance.prompt`, `appearance.status`, or
`appearance.selection`, plus `appearance.scroll.mode`,
`appearance.scroll.max_width`, `appearance.scroll.show_position`,
`appearance.scroll.show_percent`, and every style field under
`appearance.scroll.primary.style` or `appearance.scroll.secondary.style`, plus
the `appearance.scroll.primary.glyph` and `appearance.scroll.secondary.glyph`
fields. Prompt text uses `appearance.prompt.text`.

Chord names combine `ctrl-`, `alt-`, or `shift-` with a printable character or
one of `enter`, `backspace`, `escape`, `tab`, `left`, `right`, `up`, `down`, `home`,
`end`, `delete`, `page-up`, and `page-down`. Action names match the defaults
described above, such as `previous_revision`, `move_word_left`,
`scroll_page_down`, `complete`, `complete_previous`, and `accept`. A `null`
action explicitly unbinds a chord.

Dump mode runs one command through the same PTY and terminal emulator without
opening the interactive interface:

```sh
shiter --dump -- 'printf "\033[31mred\033[0m\n"'
```

## Terminal behavior

Commands run in a bidirectional PTY. `libghostty-vt` parses the PTY byte stream
and owns the screen, styles, cursor state, wrapping, reflow, and scrollback.
Terminal queries are returned to the child through the PTY. Shiter restores the
terminal state on normal exit, handled termination signals, and errors.
