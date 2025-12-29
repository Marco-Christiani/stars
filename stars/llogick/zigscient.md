---
repo: llogick/zigscient
url: 'https://github.com/llogick/zigscient'
homepage: ''
starredAt: '2025-01-17T04:26:45Z'
createdAt: '2024-10-16T09:58:26Z'
updatedAt: '2025-12-20T04:24:38Z'
language: Zig
license: NOASSERTION
branch: dev
stars: 119
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:37.312Z'
description: A Zig Language Server
tags:
  - language-server
  - language-server-protocol
  - zig
  - zig-auto-complete
  - zig-language
  - zig-language-server
---

A drop-in alternative to the original Zig Language Server, with several enhancements.

Key features and improvements:
- Reworked Modules Collection and Lookup
  - Modules are grouped by CompileStep (root ID). See [How to set/switch `root_id`](https://github.com/llogick/zigscient/wiki/Modules:-Switching-%60root_id%60)
- Improved parser performance:
  - Slightly better syntax error handling
  - Faster reparsing of large documents
- Enhanced code completions:
  - Declaration literals: autocompletion and navigation support
  - Error and function return type completions, e.g. `return .`, `return error.`, and `switch(err) { error. }`


> [!NOTE]  
> Remember to rename the executable or update your editor's configuration
