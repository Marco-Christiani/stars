---
repo: runtimed/runtimed
url: 'https://github.com/runtimed/runtimed'
homepage: ''
starredAt: '2025-11-14T05:47:33Z'
createdAt: '2024-02-16T21:43:30Z'
updatedAt: '2025-12-23T04:19:48Z'
language: Jupyter Notebook
license: BSD-3-Clause
branch: main
stars: 72
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:24.066Z'
description: Jupyter libraries for Rust
tags:
  - jupyter
  - runtime
---

## runtimed

![lilrunt](https://github.com/runtimed/runtimed/assets/836375/f5d36136-5154-4c2c-b968-4354c29670b1)

The runtimed project is tooling for working with Jupyter.

The primary crates are:

- [`jupyter-protocol`](./crates/jupyter-protocol): Core types for Jupyter messages, independent of the underlying transport
- [`jupyter-websocket-client`](./crates/jupyter-websocket-client): Connect to Jupyter servers, both local and remote, over WebSockets
- [`nbformat`](./crates/nbformat): Parse and work with Jupyter Notebooks
- [`runtimelib`](./crates/runtimelib): Interact natively with Jupyter kernels over ZeroMQ

As both examples of usage and as standalone applications, check out:

- [`ollama-kernel`](./crates/ollama-kernel): A Jupyter kernel for interacting with the Ollama model
- [`sidecar`](./crates/sidecar): A lightweight viewer of Jupyter output to run next to your terminal session

### Goal

The goal of `runtimed` is to provide Rust developers with simple, easy to use, and powerful access to interactive computing. We want to enable a new generation of builders to:

- Create new notebook applications
- Create new kinds of REPLs
- Allow large language models to reason about code and data
