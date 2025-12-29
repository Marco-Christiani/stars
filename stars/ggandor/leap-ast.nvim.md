---
repo: ggandor/leap-ast.nvim
url: 'https://github.com/ggandor/leap-ast.nvim'
homepage: ''
starredAt: '2023-05-30T23:09:19Z'
createdAt: '2022-07-13T14:41:48Z'
updatedAt: '2025-09-29T22:37:58Z'
language: Lua
license: Unlicense
branch: main
stars: 59
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:58.768Z'
description: >-
  Jump to, select and operate on AST nodes via the Leap interface with
  Treesitter (WIP)
tags: []
---

# leap-ast.nvim

Jump to, select and operate on AST nodes via the
[Leap](https://github.com/ggandor/leap.nvim) interface with Tree-sitter.

## Requirements

* Neovim >= 0.7.0
* [leap.nvim](https://github.com/ggandor/leap.nvim)
* [nvim-treesitter](https://github.com/nvim-treesitter/nvim-treesitter) (This
  dependency is only temporary; it will not be necessary in the future.)

## Installation

Use your preferred plugin manager - no extra steps needed.

## Usage

Just define one mapping, and you're good to go:

```lua
vim.keymap.set({'n', 'x', 'o'}, '<some-key>', function() require'leap-ast'.leap() end, {})
```
