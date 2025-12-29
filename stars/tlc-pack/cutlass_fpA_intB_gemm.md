---
repo: tlc-pack/cutlass_fpA_intB_gemm
url: 'https://github.com/tlc-pack/cutlass_fpA_intB_gemm'
homepage: null
starredAt: '2024-12-08T22:51:57Z'
createdAt: '2023-06-06T22:26:34Z'
updatedAt: '2025-10-22T16:42:07Z'
language: C++
license: Apache-2.0
branch: main
stars: 96
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:38.965Z'
description: >-
  A standalone GEMM kernel for fp16 activation and quantized weight, extracted
  from FasterTransformer 
tags: []
---

Extracted fp16 A and int8/4 B CUTLASS GEMM kernels from FasterTransformer for easier integration in third-party projects. See the original code below.
* https://github.com/NVIDIA/FasterTransformer/tree/main/src/fastertransformer/cutlass_extensions/include/cutlass_extensions
* https://github.com/NVIDIA/FasterTransformer/tree/main/src/fastertransformer/kernels/cutlass_kernels/fpA_intB_gemm

Build with
```
mkdir build && cd build
cmake ..
make
```
