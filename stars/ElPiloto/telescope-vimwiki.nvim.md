---
repo: ElPiloto/telescope-vimwiki.nvim
url: 'https://github.com/ElPiloto/telescope-vimwiki.nvim'
homepage: null
starredAt: '2022-06-29T16:53:45Z'
createdAt: '2021-09-30T21:41:15Z'
updatedAt: '2025-10-09T08:55:45Z'
language: Lua
license: NA
branch: main
stars: 79
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:23.117Z'
description: look through your vimwiki with your telescope
tags: []
---

# telescope-vimwiki.nvim

Look for your vimwiki pages using telescope!

### Requirements:

- [neovim](https://github.com/neovim/neovim) (>= 0.5.0)
- [vimwiki](https://github.com/vimwiki/vimwiki)
- [nvim-telescope](https://github.com/nvim-telescope/telescope.nvim)
  - with `live_grep` [support](https://github.com/nvim-telescope/telescope.nvim#suggested-dependencies)

### Installation and Configuration

1. Install using your favorite plug-in manager (e.g. [packer](https://github.com/wbthomason/packer.nvim), [vim-plug](https://github.com/junegunn/vim-plug), etc.)

2. Configure [telescope](https://github.com/nvim-telescope/telescope.nvim)

3. Load extension:

```require('telescope').load_extension('vimwiki')```

or use `vw` alias:

```require('telescope').load_extension('vw')```

If you load as `vw`, you should use `vw` in the commands below.


### Usage

#### List vimwiki pages for default (0-th) vimwiki:

```:Telescope vimwiki```

or use the `vw` alias:

```:Telescope vw```

You can specify a different vimwiki via `index` or `i` for short

```:Telescope vw index=1```
or
```:Telescope vw i=1```

#### Use telescope live grep on your vimwiki files:

```:Telescope vw live_grep```

Also supports specifying a different vimwiki:

```:Telescope vw live_grep i=1```

#### Insert link in current cursor position:

```:Telescope vw link```


#### Keybindings

**Seach vimwiki page filenames:**

```nnoremap <leader>vw <cmd>lua require('telescope').extensions.vimwiki.vimwiki()<cr>```

or (if you're loading the extension using the vw extension) 

```nnoremap <leader>vw <cmd>lua require('telescope').extensions.vw.vw()<cr>```

**Live grep vimwiki files:**

```nnoremap <leader>vg <cmd>lua require('telescope').extensions.vw.live_grep()<cr>```



### TODO

- [X] Add way of configuring which vimwiki you want, currently just defaults to 0-th wiki.
- [ ] Add support for vimwiki tags.
