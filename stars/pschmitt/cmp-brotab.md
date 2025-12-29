---
repo: pschmitt/cmp-brotab
url: 'https://github.com/pschmitt/cmp-brotab'
homepage: ''
starredAt: '2022-11-21T23:11:48Z'
createdAt: '2022-05-05T07:02:35Z'
updatedAt: '2025-12-20T01:20:13Z'
language: Lua
license: GPL-3.0
branch: main
stars: 9
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:09.774Z'
description: Brotab completion for nvim-cmp
tags:
  - brotab
  - browser
  - neovim
  - nvim
  - nvim-cmp
---

# cmp-brotab

Browser tab content content completion for 
[nvim-cmp](https://github.com/hrsh7th/nvim-cmp).

# Requirements

- [neovim](https://github.com/neovim/neovim)
- [nvim-cmp](https://github.com/hrsh7th/nvim-cmp)
- [BroTab](https://github.com/balta2ar/brotab)

# Installation (packer.nvim)

```lua
use {
  'pschmitt/cmp-brotab',
  requires = "hrsh7th/nvim-cmp",
}
```

# Configuration

```lua
require('cmp').setup({
  sources = {
    { name = 'brotab' }
  }
})
```

# LunarVim Configuration

```lua
lvim.plugins = {
  {
    "pschmitt/cmp-brotab"
    requires = "hrsh7th/nvim-cmp",
    event = "InsertEnter",
    setup = function()
      table.insert(lvim.builtin.cmp.sources, { name = "brotab" })
      lvim.builtin.cmp.formatting.source_names.brotab = "(BROTAB)"
    end
  },
}
```lua
