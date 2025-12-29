---
repo: laggingreflex/chatgpt-search
url: 'https://github.com/laggingreflex/chatgpt-search'
homepage: 'https://laggingreflex.github.io/chatgpt-search/'
starredAt: '2024-10-29T02:42:33Z'
createdAt: '2024-02-29T18:27:54Z'
updatedAt: '2025-12-24T11:55:48Z'
language: JavaScript
license: NA
branch: master
stars: 12
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:40.251Z'
description: Yet another tool to search through your (exported) ChatGPT conversations
tags:
  - chatgpt
  - search
---

# Purpose

ChatGPT has no search functionality.

There are extensions and tools to overcome this issue, but they all lack in one way or another.

This is yet another such tool.

# Usage

1. Goto [ChatGPT » Export data](https://chat.openai.com/#settings/DataControls) download your data.
1. Upload (the zip file) to this tool ([https://laggingreflex.github.io/chatgpt-search/](https://laggingreflex.github.io/chatgpt-search/))

# Features

- [Fuzzy search](https://github.com/lucaong/minisearch) through all your conversations
- Entirely in your browser, no data is sent to any server
- No need to install anything, just open the page and upload your data
- Free and open source

# Limitations

- No support for live searches, you have to update the exported data to search through new conversations

# Made with

- [react](https://react.dev/)
- [vite](https://vitejs.dev/)
- [jszip](https://stuk.github.io/jszip/)
- [minisearch](https://github.com/lucaong/minisearch)
