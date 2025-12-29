---
repo: dmlc/dlpack
url: 'https://github.com/dmlc/dlpack'
homepage: 'https://dmlc.github.io/dlpack/latest'
starredAt: '2025-12-08T23:08:23Z'
createdAt: '2017-02-24T16:56:47Z'
updatedAt: '2025-12-29T07:13:17Z'
language: C++
license: Apache-2.0
branch: main
stars: 1128
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:23.578Z'
description: 'common in-memory tensor structure '
tags:
  - deep-learning
  - operator
  - tensor
---

# DLPack: Open In Memory Tensor Structure

[![Build Status](https://github.com/dmlc/dlpack/actions/workflows/main.yaml/badge.svg?branch=main)](https://github.com/dmlc/dlpack/actions/workflows/main.yaml)

Documentation: [https://dmlc.github.io/dlpack/latest](https://dmlc.github.io/dlpack/latest)

DLPack is an open in-memory tensor structure for sharing tensors among frameworks. DLPack enables

- Easier sharing of operators between deep learning frameworks.
- Easier wrapping of vendor level operator implementations, allowing collaboration when introducing new devices/ops.
- Quick swapping of backend implementations, like different version of BLAS
- For final users, this could bring more operators, and possibility of mixing usage between frameworks.

We do not intend to implement Tensor and Ops, but instead use this as common bridge
to reuse tensor and ops across frameworks.

## Proposal Procedure
RFC proposals are opened as issues. The major release will happen as a vote issue to make
sure the participants agree on the changes.

## Project Structure
There are two major components so far
- include: stabilized headers
- contrib: in progress unstable libraries

## People
Here are list of people who have been involved in DLPack RFC design proposals:

@soumith @piiswrong @Yangqing @naibaf7 @bhack @edgarriba @tqchen @prigoyal @zdevito
