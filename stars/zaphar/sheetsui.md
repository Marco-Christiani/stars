---
repo: zaphar/sheetsui
url: 'https://github.com/zaphar/sheetsui'
homepage: ''
starredAt: '2024-12-10T16:08:55Z'
createdAt: '2024-11-30T14:29:21Z'
updatedAt: '2025-12-25T07:50:13Z'
language: Rust
license: Apache-2.0
branch: main
stars: 231
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:38.670Z'
description: Sheetui is a console based spreadsheet inspired by sc-im and vim
tags:
  - cli-app
  - console-application
  - spreadhseets
---

# SheetsUI - a console based spreadsheet application

## Installing

### Nix Flake

```sh
nix profile install github:zaphar/sheetsui
```

### Cargo

```sh
cargo install --git https://github.com/zaphar/sheetsui --locked
```

## Running

```sh
sheetui --help #print the help text for the cli

Usage: sheetui [OPTIONS] <WORKBOOK>

Arguments:
  <WORKBOOK>

Options:
  -l, --locale-name <LOCALE_NAME>      [default: en]
  -t, --timezone-name <TIMEZONE_NAME>  [default: America/New_York]
  -h, --help                           Print help
  -V, --version                        Print version
```

```sh
sheetui path/to/file.xlsx # edit/view a spreadsheet
```

### Supported files

Currently we only support the [ironcalc](https://docs.ironcalc.com/) xlsx
features for spreadsheet. CSV import and expor are planned.

### Screenshot

<img src="./assets/screenshot.png" />

## Reference

* [Documentation](./docs/index.md)
