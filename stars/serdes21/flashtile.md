---
repo: serdes21/flashtile
url: 'https://github.com/serdes21/flashtile'
homepage: ''
starredAt: '2026-02-16T08:57:24Z'
createdAt: '2026-02-06T10:10:35Z'
updatedAt: '2026-02-20T16:30:18Z'
language: Rust
license: Apache-2.0
branch: main
stars: 51
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-02-21T22:32:42.877Z'
description: >-
  FlashTile is a CUDA Tile IR compiler that is compatible with NVIDIA's
  tileiras, targeting SM70 through SM121 NVIDIA GPUs. 
tags:
  - compiler
  - cutile
  - gpu
  - tile
---

# FlashTile

English | [中文](README.zh-cn.md)

FlashTile is a CUDA Tile IR compiler that is compatible with NVIDIA's `tileiras`, targeting SM70 through SM121 NVIDIA GPUs. 


## Quick Start

1. Download the latest binary for your platform from [GitHub Releases](https://github.com/serdes21/flashtile/releases).

2. Rename and add to PATH:

**Linux**

```bash
mv flashtile tileiras
chmod +x tileiras
export PATH="/path/to/tileiras:$PATH"
```

**Windows**

```powershell
Rename-Item flashtile.exe tileiras.exe
$env:PATH = "C:\path\to\tileiras;" + $env:PATH
```


## Correctness Testing

Validated with 74 test files (54 from cutile-python, 20 from TileGym, excluding benchmarks). For efficiency, only 1 representative case is sampled per test file.
![Test Results](docs/images/test_results.png)


## Performance Testing

FlashTile is still in early development. Performance benchmarks have not yet been conducted.


## Debugging

FlashTile provides multiple ways to inspect intermediate representations at each compilation stage.

**Step 1:** Export the bytecode file from cutile-python by setting the environment variable:

```bash
export CUDA_TILE_DUMP_BYTECODE=/path/to/cutile
```

This causes cutile-python to save `.cutile` files to the working directory when compiling kernels.

**Step 2:** Use `--dump-*` flags to inspect each stage of the compilation pipeline:

```bash
flashtile --dump-ir        kernel.cutile   # Parsed CUDA Tile IR
flashtile --dump-mlir      kernel.cutile   # MLIR textual format (cutile-compatible)
flashtile --dump-tir       kernel.cutile   # Lowered TVM TIR
flashtile --dump-tvmscript kernel.cutile   # TVMScript (TVM IR printer)
flashtile --dump-cuda --gpu-name=sm_90 kernel.cutile   # Generated CUDA source
flashtile --dump-ptx  --gpu-name=sm_90 kernel.cutile   # Generated PTX assembly
```



## Building from Source

**Linux** — see [`docker/`](docker/) for Dockerfiles and build script:

```bash
bash docker/build.sh
```

**Windows** — see [`scripts/build-windows-static.ps1`](scripts/build-windows-static.ps1):

```powershell
.\scripts\build-windows-static.ps1
```


## Notes

- NVIDIA driver version **580+** is required, due to the host launch mechanism used by cutile-python.


## Join the Discussion

Welcome to join our Discord community for discussions, support, and collaboration!

[![Join our Discord](https://img.shields.io/badge/Discord-Join%20Us-blue?logo=discord&style=for-the-badge)](https://discord.gg/v6CD6vG4fq)

QQ group: 1056444998
Wechat ID: serdes21
