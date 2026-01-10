---
repo: schuelermine/xhmm
url: 'https://github.com/schuelermine/xhmm'
homepage: null
starredAt: '2026-01-08T22:16:32Z'
createdAt: '2022-12-07T17:10:05Z'
updatedAt: '2026-01-08T22:16:32Z'
language: Nix
license: Apache-2.0
branch: b0
stars: 58
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-01-10T22:31:08.274Z'
description: Extra home manager modules
tags: []
---

# xhmm—extra home-manager modules

Extra home manager modules.

To import, use either flakes or import a file directly.

You are encouraged to look through the code yourself! Many options have been described via the description fields.

Current contents:

- `console`: Shell things
    - `fish`: Fish
        - Fish prompt
    - `nano`: More options for `nano`
        - ⚠️ Requires `program-variables`
    - `program-variables`: Program variables
        - `$PAGER`
        - `$EDITOR`
        - `$VISUAL`
- `desktop`: Desktop configuration
    - `gnome`: GNOME configuration
        - Shell theme
        - GTK theme
        - Cursor theme
        - Extensions
        - Fonts
    - `fonts`: Alias for `home.packages` for fonts
- `languages`: Programming languages
    - `haskell`: Haskell
        - Cabal
        - GHC
        - GHCup
        - HLS
        - Stack
    - `python`: Python
        - Python
        - Mypy
        - Pip
        - Pytest
    - `rust`: Rust (note that you may need to also have a CC installed)
        - Cargo
        - Clippy
        - RLS
        - Rust analyzer
        - Rustc
        - Rustfmt
        - Rustup
        - Expose rust source location for language servicess
