---
repo: tamton-aquib/neorg-jupyter
url: 'https://github.com/tamton-aquib/neorg-jupyter'
homepage: ''
starredAt: '2024-06-28T15:35:31Z'
createdAt: '2023-01-13T18:16:57Z'
updatedAt: '2025-08-31T04:36:58Z'
language: null
license: NA
branch: main
stars: 30
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:43.882Z'
description: A neorg module to work with jupyter notebooks inside neorg.
tags:
  - jupyter
  - jupyter-notebook
  - neorg
  - neovim
---

# Neorg Jupyter

A [neorg](https://github.com/nvim-neorg/neorg) module that allows integration with jupyter notebook inside a neorg file.<br />
Pretty bare-bones right now.

https://user-images.githubusercontent.com/77913442/212394503-4197470f-0802-49b3-9c4f-2919032d038a.mp4

### Setup

Set this inside neorg's setup.
```lua
["external.jupyter"] = {}
```

### Configuration
Currently there are no configuration options

### Usage
Provides 3 options
- `:Neorg jupyter init` (to load up the kernel)
- `:Neorg jupyter generate filename.ipynb` (generate a neorg file from the provided notebook)
- `:Neorg jupyter run` (to run the code block)
