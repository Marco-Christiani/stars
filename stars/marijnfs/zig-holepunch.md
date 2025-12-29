---
repo: marijnfs/zig-holepunch
url: 'https://github.com/marijnfs/zig-holepunch'
homepage: null
starredAt: '2024-04-17T05:16:37Z'
createdAt: '2021-11-04T19:40:09Z'
updatedAt: '2024-04-17T05:16:37Z'
language: Zig
license: MPL-2.0
branch: master
stars: 1
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:46.694Z'
description: UDP to TCP hole punching in Zig
tags: []
---

# Zig based UDP holepunching to create a TCP connection


# Building:
zig build

# Usage on server side
```Bash
./zig-out/bin/zig-holepunch-server 3000
```

# Usage on client sides (x 2)
```Bash
./zig-out/bin/zig-holepunch 0.0.0.0 3000
```

Ip Address _0.0.0.0_ is used here for localhost, replace it with the ip of the server
