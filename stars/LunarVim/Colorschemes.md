---
repo: LunarVim/Colorschemes
url: 'https://github.com/LunarVim/Colorschemes'
homepage: ''
starredAt: '2022-06-19T19:04:57Z'
createdAt: '2021-07-11T02:44:12Z'
updatedAt: '2025-11-10T12:46:52Z'
language: Lua
license: AGPL-3.0
branch: master
stars: 103
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:26.389Z'
description: "\U0001F308 Collection of colorschemes made to be compatible with LunarVim"
tags:
  - theme
  - vim
---

# LunarVimColorschemes

Collection of colorschemes made to be compatible with LunarVim

## Setup

```sh
pip install -r requirements.txt
```

## Adding a template

I recommend copying one of the themes in template and using it as a base to create your own

## Generate your colorscheme

```
python ez.py <your_cool_theme>.yml
```

## After generating your colorscheme the following configuration options should be available
```lua
vim.g.transparent_background = true        -- transparent background(Default: false)
vim.g.italic_comments = true               -- italic comments(Default: true)
vim.g.italic_keywords = true               -- italic keywords(Default: true)
vim.g.italic_functions = true              -- italic functions(Default: false)
vim.g.italic_variables = true              -- italic variables(Default: false)
```

**Credit** for the script for creating colorschemes: [repo](https://github.com/Murtaza-Udaipurwala/ez.nvim)
