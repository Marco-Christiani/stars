---
repo: juni-purr/tmux-cht-sh
url: 'https://github.com/juni-purr/tmux-cht-sh'
homepage: ''
starredAt: '2023-09-11T18:53:34Z'
createdAt: '2023-07-05T02:13:34Z'
updatedAt: '2025-11-18T04:50:59Z'
language: Shell
license: MIT
branch: main
stars: 39
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:56.043Z'
description: Access cheatsheets easily in a popup in tmux!
tags: []
---

# Tmux cht.sh

Access cheatsheets easily in a popup in tmux!

![FZF Selection](./assets/selection.png)
![Viewing](./assets/pager.png)

## Requirements

- `curl`
- `tmux`
- `fzf`
- `bash`

## Installation

### Install using TPM

Put this in your configuration file,

```sh
set -g @plugin 'kenos1/tmux-cht-sh'
```

### Install manually using git

1. Clone the repository

```sh
git clone https://github.com/kenos1/tmux-cht-sh ~/clone/path
```

2. Put this line in your config

```sh
run-shell ~/clone/path/tmux-cht-sh.tmux
```

3. Restart `tmux`

## Usage

To invoke the cheatsheet use the keybind <kbd>prefix</kbd>–<kbd>S</kbd>

## Configuration

Change the pager by changing your `PAGER` environment variable. This means adding this to your shell config:

```sh
# Bash/ZSH example using less
export PAGER="less"
```
