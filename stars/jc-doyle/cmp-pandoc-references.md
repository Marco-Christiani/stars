---
repo: jc-doyle/cmp-pandoc-references
url: 'https://github.com/jc-doyle/cmp-pandoc-references'
homepage: ''
starredAt: '2022-07-01T17:26:36Z'
createdAt: '2021-09-25T12:01:00Z'
updatedAt: '2025-10-14T03:48:18Z'
language: Lua
license: NA
branch: master
stars: 65
isPublic: true
isTemplate: false
isArchived: true
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:22.633Z'
description: >-
  A source for nvim-cmp, providing completion for bibliography, reference and
  cross-ref items in Pandoc/Markdown.
tags:
  - nvim-cmp
---

# cmp-pandoc-references

A source for [nvim-cmp](https://github.com/hrsh7th/nvim-cmp), providing completion for bibliography, reference and cross-ref items.

## Demo
![cmp-pandoc-references](https://user-images.githubusercontent.com/59124867/134782887-33872ae0-a23e-4f5b-99cd-74c3b0e6f497.gif)

Note I have overridden the `ItemKinds`, they are set to `cmp.lsp.CompletionItemKind.Reference` by default.

## Installation & Usage

Assuming Packer:

``` lua
use({
  "hrsh7th/nvim-cmp",
  requires = {
    { "jc-doyle/cmp-pandoc-references" }
  }
})
```

Add the source:

``` lua
require('cmp').setup {
  sources = {
    { name = 'pandoc_references' }
  }
}
```

## Explanation & Limitations

This source parses and validates the `bibliography: [your/bib/location.bib]` YAML metadata field, to determine the destination of the file (see [Pandoc](https://pandoc.org/MANUAL.html#specifying-bibliographic-data)). If it is not included (or you specify it through a command-line argument), no bibliography completion items will be found.

(I use the metadata block to reference bibliographies, if you'd like automatic scanning of directories/sub-directories, feel free to submit a PR)



