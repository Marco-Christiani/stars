---
repo: dani2112/llmtopic
url: 'https://github.com/dani2112/llmtopic'
homepage: null
starredAt: '2024-04-01T17:36:17Z'
createdAt: '2024-02-10T18:27:08Z'
updatedAt: '2024-05-20T10:47:20Z'
language: Jupyter Notebook
license: NA
branch: main
stars: 7
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:47.195Z'
description: >-
  A library that leverages large language models (llms) for extracting topics
  from text documents.
tags: []
---

# llmtopic
A library that leverages large language models (llms) for extracting topics from text documents.

## Install
To install for CPU run `pip install llmtopic`.

To install with GPU support run `CMAKE_ARGS="-DLLAMA_CUBLAS=on" pip install llmtopic`.

If you are under Ubuntu and encounter errors regarding a failed build consider upgrading your cuda version to >=12.1. Also, it could be you have to point to the new nvcc version but modifying the install command as follows: `PATH="/usr/local/cuda-12.3/bin:$PATH" CMAKE_ARGS="-DLLAMA_CUBLAS=on" pip install llmtopic`. Note that you of course have to adjsut that to your specific CUDA version.

For vision application use this install command:

`PATH="/usr/local/cuda-12.3/bin:$PATH" CMAKE_ARGS="-DLLAMA_CUBLAS=on -DLLAVA_BUILD=on" pip install --upgrade --force-reinstall --no-c
ache-dir llama-cpp-python==0.2.55`
