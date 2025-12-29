---
repo: HazyResearch/Megakernels
url: 'https://github.com/HazyResearch/Megakernels'
homepage: null
starredAt: '2025-11-19T19:35:47Z'
createdAt: '2025-05-27T18:25:49Z'
updatedAt: '2025-12-27T15:32:15Z'
language: Python
license: MIT
branch: main
stars: 636
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:23.954Z'
description: 'kernels, of the mega variety'
tags: []
---

# Megakernels!

## Installation

Clone this repo and run:

```bash
git submodule update --init --recursive
pip install uv
uv pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu128
uv pip install -e .
```

## Low-Latency Llama Demo

First, to compile the megakernel, run:

```bash

# from the repo root
export THUNDERKITTENS_ROOT=$(pwd)/ThunderKittens
export MEGAKERNELS_ROOT=$(pwd)
export PYTHON_VERSION=3.12 # adjust if yours is different
export GPU=H100 # options are {H100, B200}, else defaults to B200
cd demos/low-latency-llama
make

```

To start an interactive chat session with the model, run:

```bash

# from the repo root
python megakernels/scripts/llama_repl.py

```

To benchmark the megakernel, run:

```bash

# from the repo root
python megakernels/scripts/generate.py mode=mk prompt="tell me a funny joke about cookies" ntok=100

```
