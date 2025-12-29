---
repo: lawrence-laz/neotest-zig
url: 'https://github.com/lawrence-laz/neotest-zig'
homepage: ''
starredAt: '2025-02-17T18:37:41Z'
createdAt: '2023-10-01T13:29:42Z'
updatedAt: '2025-12-22T20:08:10Z'
language: Lua
license: MIT
branch: main
stars: 42
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:34.618Z'
description: Test runner for Zig in Neovim using Neotest backend.
tags:
  - lua
  - neotest
  - neovim
  - test
  - zig
---

# Neotest Zig ⚡

![Zig v0.14.0](https://img.shields.io/badge/Zig-v0.14-orange?logo=zig)
![Neovim v0.10](https://img.shields.io/badge/Neovim-v0.10-green?logo=neovim)

[Neotest](https://github.com/nvim-neotest/neotest) test runner for [Zig](https://github.com/ziglang/zig).

https://github.com/lawrence-laz/neotest-zig/assets/8823448/9a003d0a-9ba4-4077-aa1b-3c0c90717734

## ⚙️ Requirements
- [`zig` v0.14 installed](https://ziglang.org/download/) and available in PATH
    - If you are using `zig` v0.13, then use the tagged `neotest-zig` 1.3.* version.
- [Neotest](https://github.com/nvim-neotest/neotest#installation)
- [Treesitter](https://github.com/nvim-treesitter/nvim-treesitter#installation) with [Zig support](https://github.com/maxxnino/tree-sitter-zig)

## 📦 Setup
Install & configure using the package manager of your choice.
Example using lazy.nvim:
```lua
return {
	"nvim-neotest/neotest",
	dependencies = {
		"lawrence-laz/neotest-zig", -- Installation
		"nvim-lua/plenary.nvim",
		"nvim-treesitter/nvim-treesitter",
		"antoinemadec/FixCursorHold.nvim",
	},
	config = function()
		require("neotest").setup({
			adapters = {
				-- Registration
				require("neotest-zig")({
					dap = {
						adapter = "lldb",
					}
				}),
			}
		})
	end
}
```

## ⭐ Features
 - Can run tests in individual `.zig` files and projects using `build.zig` 
   - Does not support a mix of individual files and `build.zig`:w
   - `buil.zig` must have a standard `test` step
 - Exact test filtering
 - Timing all tests individually

## 📄 Logs
Enabling logging in `neotest` automatically enables logging in `neotest-zig` as well:
```lua
require("neotest").setup({
    log_level = vim.log.levels.TRACE,
    -- ...
})
```
The logs can be openned by:
```vim
:exe 'edit' stdpath('log').'/neotest-zig.log'
```
