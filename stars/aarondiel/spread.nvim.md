---
repo: aarondiel/spread.nvim
url: 'https://github.com/aarondiel/spread.nvim'
homepage: ''
starredAt: '2023-07-11T23:49:35Z'
createdAt: '2022-07-19T18:37:48Z'
updatedAt: '2025-09-29T22:40:24Z'
language: Lua
license: NA
branch: main
stars: 98
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:57.543Z'
description: 'a neovim plugin to spread out inline objects, arrays, parameter lists, etc.'
tags:
  - formatter
  - formatting
  - neovim
  - nvim
  - plugin
  - vim
---

<h1 align="center">spread.nvim</h1>

<p align="center"><img width=500 src="assets/spread.webp"/></p>

<p align="center">
	a plugin to refactor and spread out objects, arrays, parameter lists, etc
	onto multiple lines.
</p>

<p align="center">
	this plugin is still <em>work in progress</em>, so don't expect it to work
	with every language and container.
</p>

## installation

> this plugin uses [treesitter][nvim-treesitter] so be sure to also install it

using [packer][packer]:

```lua
use({
	"aarondiel/spread.nvim",
	after = "nvim-treesitter",
	config = function()
		local spread = require("spread")
		local default_options = {
			silent = true,
			noremap = true
		}

		vim.keymap.add("n", "<leader>ss", spread.out, default_options)
		vim.keymap.add("n", "<leader>ssc", spread.combine, default_options)
	end
})
```

[nvim-treesitter]: https://github.com/nvim-treesitter/nvim-treesitter
[packer]: https://github.com/wbthomason/packer.nvim
