---
repo: allyourcodebase/tracy
url: 'https://github.com/allyourcodebase/tracy'
homepage: ''
starredAt: '2025-02-04T21:32:27Z'
createdAt: '2024-12-18T20:56:55Z'
updatedAt: '2025-12-16T17:10:08Z'
language: C++
license: NOASSERTION
branch: master
stars: 5
isPublic: true
isTemplate: false
isArchived: false
isFork: true
hasReadMe: true
refreshedAt: '2025-12-29T17:34:36.449Z'
description: 'Tracy ported to the zig build system '
tags:
  - zig
  - zig-package
---

[![CI](https://github.com/allyourcodebase/tracy/actions/workflows/build.yml/badge.svg)](https://github.com/allyourcodebase/tracy/actions)

# Tracy Profiler

This is [Tracy](https://github.com/wolfpld/tracy), packaged for [Zig](https://ziglang.org/).

## Installation

Install Zig 0.15.2 and then run the following command:

```bash
zig build install-profiler
./zig-out/bin/tracy-profiler
```

You can also directly run the Tracy Profiler with the "run" step:

```bash
zig build run
```

### System Dependencies

When building for Windows or macOS, no system dependencies are required.

The graphical profiler has the following dependencies on linux:

- `libGL`: runtime dependency
- `libEGL`: runtime dependency, not required when using `-Dlegacy`
- `libxkbcommon`: not required when using `-Dlegacy`
- `libdbus-1`: can be disabled with `-Dno-fileselector` or `-Dportal=false`
- `libgtk+-3.0`: only required when using `-Dportal=false`

#### System Integrations

Tracy has been ported with support for Zig's [System Integration Options](https://ziglang.org/download/0.12.0/release-notes.html#Ability-to-Declare-Optional-System-Library-Integration). By default, all system dependencies will be avoided except `libxkbcommon`.

### Cross Compilation

#### Windows

Cross compiling to windows works out of the box. It can even connect to a client that is running a different host (Linux).

```bash
zig build -Dtarget=x86_64-windows
zig build run -Dtarget=x86_64-windows -fwine # run the tracy profiler with Wine
```

#### Linux

Cross compiling to macOS can successfully produce a binary. The binary has a runtime dependency on `libGL` and will fail if it can't be found with `dlopen`.

```bash
zig build -Dtarget=x86_64-linux -Dno-fileselector -Dlegacy
```
