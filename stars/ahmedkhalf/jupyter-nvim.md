---
repo: ahmedkhalf/jupyter-nvim
url: 'https://github.com/ahmedkhalf/jupyter-nvim'
homepage: ''
starredAt: '2022-06-22T16:55:54Z'
createdAt: '2021-06-02T11:25:11Z'
updatedAt: '2025-09-17T21:51:20Z'
language: Python
license: MIT
branch: main
stars: 98
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:25.139Z'
description: Jupyter notebook client in neovim
tags: []
---

# 🪐 Jupyter-Nvim

Read jupyter notebooks in neovim

![image](https://user-images.githubusercontent.com/36672196/120599447-958acd80-c458-11eb-9ed1-2c6b2bb9424c.png)

*Note:* The plugin is still in alpha stage

## ⚡️ Requirements

- Neovim >= 0.5.0

## 📦 Installation

Install the plugin with your preferred package manager:

### [vim-plug](https://github.com/junegunn/vim-plug)

```vim
" Vim Script
Plug 'ahmedkhalf/jupyter-nvim', { 'do': ':UpdateRemotePlugins' }

lua << EOF
  require("jupyter-nvim").setup {
    -- your configuration comes here
    -- or leave it empty to use the default settings
    -- refer to the configuration section below
  }
EOF
```

### [packer](https://github.com/wbthomason/packer.nvim)

```lua
-- Lua
use {
  "ahmedkhalf/jupyter-nvim",
  run = ":UpdateRemotePlugins",
  config = function()
    require("jupyter-nvim").setup {
      -- your configuration comes here
      -- or leave it empty to use the default settings
      -- refer to the configuration section below
    }
  end
}
```

## ⚙️ Configuration

**jupyter-nvim** comes with the following defaults:

```lua
{
  -- Nothing till now
}
```

## 👾 Usage

Just open any `*.ipynb` file and voila!

## ✨ Contributing

All contributions are welcome! Even bug report count as a contribution, so if there is anything off don't hesitate to open an issue.

## 🚀 TODO

You can find the todo on [github projects](https://github.com/ahmedkhalf/jupyter-nvim/projects/1).
