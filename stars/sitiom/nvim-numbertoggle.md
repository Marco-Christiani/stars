---
repo: sitiom/nvim-numbertoggle
url: 'https://github.com/sitiom/nvim-numbertoggle'
homepage: ''
starredAt: '2022-10-06T00:18:34Z'
createdAt: '2022-07-04T10:24:08Z'
updatedAt: '2025-12-22T15:25:59Z'
language: Lua
license: MIT
branch: main
stars: 212
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:15.794Z'
description: >-
  Neovim plugin to automatically toggle between relative and absolute line
  numbers. Written in Lua.
tags:
  - line-numbers
  - lua
  - neovim
  - neovim-plugin
  - nvim
---

# nvim-numbertoggle

Neovim plugin to automatically toggle between relative and absolute line numbers. Written in Lua.

![demo](https://user-images.githubusercontent.com/56180050/177167997-652a43b1-c94a-4b73-94d6-e4b85fbd4606.gif)

Relative numbers are used in a buffer that has focus and is in normal mode since that's where you move around. They're turned off when you switch out of Vim, switch to another split, or go into insert and command modes.

## Getting started

### Requirements

- Neovim 0.7 or later

### Installation

Use your favorite package manager. Example config with [packer.nvim](https://github.com/wbthomason/packer.nvim):

```lua
use { "sitiom/nvim-numbertoggle" }
```

## Acknowledgment

https://github.com/jeffkreeftmeijer/vim-numbertoggle
