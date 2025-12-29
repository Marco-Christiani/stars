---
repo: diggit/ulauncher-lolcate
url: 'https://github.com/diggit/ulauncher-lolcate'
homepage: null
starredAt: '2022-11-21T22:12:09Z'
createdAt: '2021-10-17T17:07:05Z'
updatedAt: '2025-03-29T21:50:46Z'
language: Python
license: NA
branch: master
stars: 7
isPublic: true
isTemplate: false
isArchived: false
isFork: true
hasReadMe: true
refreshedAt: '2025-12-29T17:35:10.167Z'
description: 'Extension for ulauncher to visit your files anytime, anywhere'
tags: []
---

# Lolcate wrapper for Ulauncher

Extension for [ulauncher](https://ulauncher.io/) to visit your files anytime, anywhere.

This is "fork" of [ulauncher-searchfile extension](https://github.com/compilelife/ulauncher-searchfile) which is not maintained anymore.

## Dependencies

### lolcate
- [`lolcate`](https://github.com/ngirard/lolcate-rs) is alternative to `locate`. (Note that it's lo**l**cate not locate)
- fast, configurable indexing tool
- lolcate configuration is topic for official documentation, please [head there](https://github.com/ngirard/lolcate-rs#guide) if you need help with config

## Usage 

All aguments are passed to `lolcate`, which accepts plain text, but also regexes.

Press Alt+Number/Enter to open files using `xdg-open`.

Alternative, you can press Alt-Enter to switch to copy-to-clipboard menu.

### Limitations
- Only default database is used
- No way to reach results which did not fit into result list (depends on limit settings)
