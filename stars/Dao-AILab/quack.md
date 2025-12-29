---
repo: Dao-AILab/quack
url: 'https://github.com/Dao-AILab/quack'
homepage: ''
starredAt: '2025-12-19T04:31:04Z'
createdAt: '2025-05-20T18:34:37Z'
updatedAt: '2025-12-29T05:55:33Z'
language: Python
license: Apache-2.0
branch: main
stars: 725
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:23.155Z'
description: A Quirky Assortment of CuTe Kernels
tags: []
---

# 🦆 QuACK: A Quirky Assortment of CuTe Kernels 🦆

Kernels are written in the [CuTe-DSL](https://docs.nvidia.com/cutlass/media/docs/pythonDSL/cute_dsl_general/dsl_introduction.html).

## Installation

``` bash
pip install quack-kernels
```

## Requirements

- H100 or B200 GPU
- CUDA toolkit 12.9+
- Python 3.12

## Kernels 🐥

- 🦆 RMSNorm forward + backward
- 🦆 Softmax forward + backward
- 🦆 Cross entropy forward + backward
- 🦆 Layernorm forward
- 🦆 Hopper gemm + epilogue
- 🦆 Blackwell gemm + epilogue

## Usage

```
from quack import rmsnorm, softmax, cross_entropy
```

## Documentations

[2025-07-10] We have a comprehensive
[blogpost](media/2025-07-10-membound-sol.md) on how to get memory-bound kernels
to speed-of-light, right in the comfort of Python thanks to the [CuTe-DSL](https://docs.nvidia.com/cutlass/media/docs/pythonDSL/cute_dsl_general/dsl_introduction.html).

## Performance

<div align="center">
<figure>
  <img
  src="media/bf16_kernel_benchmarks_single_row.svg"
  >
</figure>
</div>

See our [blogpost](media/2025-07-10-membound-sol.md) for the details.

## Development

To set up the development environment:

```bash
pip install -e '.[dev]'
pre-commit install
```
