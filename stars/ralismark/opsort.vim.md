---
repo: ralismark/opsort.vim
url: 'https://github.com/ralismark/opsort.vim'
homepage: ''
starredAt: '2022-07-09T05:03:25Z'
createdAt: '2022-07-08T15:07:48Z'
updatedAt: '2024-07-01T06:09:02Z'
language: Vim script
license: MIT
branch: main
stars: 29
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:21.437Z'
description: Custom operator that sorts lines
tags:
  - neovim-plugin
  - vim-plugin
---

# opsort.vim

This plugin provides one thing: an operator that sorts the lines it is applied to.

# Requirements

- vim *or* neovim
- [tpope/vim-repeat](https://github.com/tpope/vim-repeat/) (optional)

# Summary

By default, `gs` is mapped to sort.

When applied linewise (e.g. Visual-line mode, motions, and text objects), it sorts the lines lexicographically.
For example:

- `gsip` sorts the current paragraph (like `dip`).
- `10gss` and `10gsgs` both sort 10 lines (like `10dd`).

With Visual-block mode, the selected lines are sorted according to the selected columns.
For example, if the region bounded by `|` is selected,

```
Apple  |10|
Orange | 3|
Banana |40|
```

pressing `gs` will change that to

```
Orange  3
Apple  10
Banana 40
```
