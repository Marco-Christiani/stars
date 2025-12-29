---
repo: zigtools/zls
url: 'https://github.com/zigtools/zls'
homepage: 'https://zigtools.org/zls/install/'
starredAt: '2025-01-12T17:44:23Z'
createdAt: '2020-04-24T22:19:50Z'
updatedAt: '2025-12-29T12:56:57Z'
language: Zig
license: MIT
branch: master
stars: 4449
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:37.435Z'
description: >-
  A language server for Zig supporting developers with features like
  autocomplete and goto definition
tags:
  - language-server
  - language-server-protocol
  - lsp
  - lsp-server
  - zig
  - ziglang
  - zls
---

<img src="https://raw.githubusercontent.com/zigtools/zls/master/.github/assets/zls-opt.svg" alt="ZLS Logo" width=200>

[![CI](https://github.com/zigtools/zls/actions/workflows/main.yml/badge.svg)](https://github.com/zigtools/zls/actions/workflows/main.yml)
[![codecov](https://codecov.io/github/zigtools/zls/graph/badge.svg?token=WE18MPF00W)](https://codecov.io/github/zigtools/zls)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Discord](https://discord.com/api/guilds/997174129532866701/widget.png?style=shield)](https://discord.gg/5m5U3qpUhk)

ZLS is a non-official implementation of the [Language Server Protocol](https://microsoft.github.io/language-server-protocol/) for [Zig](https://ziglang.org/) in Zig. It provides developers with IDE [features](#features) in their editor.

## Installation

The complete installation guide is available on the [Zigtools website](https://zigtools.org/zls/install/). It covers editor setup, prebuilt binaries and additional documentation.

### Build From Source

Building ZLS requires [a build of Zig master](https://ziglang.org/download/).

```bash
git clone https://github.com/zigtools/zls
cd zls
zig build -Doptimize=ReleaseSafe
```

When upgrading Zig, make sure to update ZLS too keep them in sync.

## Features

ZLS supports most language features, including simple type function support, using namespace, payload capture type resolution, custom packages, cImport and others. Support for comptime and semantic analysis is Work-in-Progress.

The following LSP features are supported:

- Completions
- Hover
- Goto definition/declaration
- Document symbols
- Find references
- Rename symbol
- Formatting using `zig fmt`
- Semantic token highlighting
- Inlay hints
- Code actions
- Selection ranges
- Folding regions

## Related Projects

- [`sublime-zig-language` by @prime31](https://github.com/prime31/sublime-zig-language)
  - Supports basic language features
  - Uses data provided by `src/data` to perform builtin autocompletion
- [`zig-lsp` by @xackus](https://github.com/xackus/zig-lsp)
  - Inspiration for ZLS
- [`known-folders` by @ziglibs](https://github.com/ziglibs/known-folders)
  - Provides API to access known folders on Linux, Windows and Mac OS
- [`zls` by @zigtools](https://github.com/zigtools/zls)
  - Used by many ZLS developers to more efficiently work on ZLS

## Quick Thanks :)

We'd like to take a second to thank all our awesome [contributors](https://github.com/zigtools/zls/graphs/contributors) and donators/backers/sponsors; if you have time or money to spare, consider partaking in either of these options - they help keep ZLS awesome for everyone!

[![OpenCollective Backers](https://opencollective.com/zigtools/backers.svg?width=890&limit=1000)](https://opencollective.com/zigtools#category-CONTRIBUTE)
