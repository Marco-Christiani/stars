---
repo: declancm/maximize.nvim
url: 'https://github.com/declancm/maximize.nvim'
homepage: ''
starredAt: '2022-10-18T18:46:11Z'
createdAt: '2022-05-04T22:39:54Z'
updatedAt: '2025-12-18T05:57:31Z'
language: Lua
license: MIT
branch: master
stars: 70
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:14.192Z'
description: Maximize window splits. A Neovim plugin written in Lua!
tags:
  - lua
  - maximize
  - neovim
  - nvim
  - plugin
  - vim
---

# maximize.nvim

Maximize Neovim windows.

## ✨ Features

* Toggle maximizing the current window without any ugly borders.
* Has builtin integration for the following plugins:
  * aerial.nvim
  * nvim-dap-ui
  * nvim-tree.lua

## 🛠️ Requirements

* Neovim >= 0.8.0 (use a tagged version for older Neovim versions)

## 📦 Installation

Install with your favourite plugin manager and run the setup function.

### Packer

```lua
use {
  'declancm/maximize.nvim',
  config = function() require('maximize').setup() end
}
```

### Lazy

```lua
return {
  'declancm/maximize.nvim',
  config = true
}
```

## ℹ️ Usage

### Vim Commands

* Toggle maximizing the current window:

  `:Maximize`

### Lua API

* Toggle maximizing the current window:

  `require('maximize').toggle()`

* Maximize the current window:

  `require('maximize').maximize()`

* Restore windows:

  `require('maximize').restore()`

## ⚙️  Configuration

A settings table can be passed into the setup function for custom options.

### Default Options

```lua
{
  plugins = {
    aerial = { enable = true }, -- enable aerial.nvim integration
    dapui = { enable = true },  -- enable nvim-dap-ui integration
    tree = { enable = true },   -- enable nvim-tree.lua integration
  }
}
```

## 📅 User Events

The following user events are triggered:

* **WindowMaximizeStart**: before maximizing
* **WindowRestoreEnd**: after restoring

## 🚥 statusline & winbar

Use the variable `vim.t.maximized` to check whether the tab has a maximized window.

### Lualine

```lua
local function maximize_status()
  return vim.t.maximized and '   ' or ''
end

require('lualine').setup {
  sections = {
    lualine_c = { maximize_status }
  }
}
```

### winbar

```lua
-- ~/.config/nvim/lua/winbar.lua
local M = {}

M.maximize_status = function()
  return vim.t.maximized and '   ' or ''
end

return M

-- ~/.config/nvim/init.lua
vim.o.winbar = "%{%v:lua.require('winbar').maximize_status()%}"
```
