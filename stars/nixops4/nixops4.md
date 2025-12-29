---
repo: nixops4/nixops4
url: 'https://github.com/nixops4/nixops4'
homepage: null
starredAt: '2025-10-19T23:16:02Z'
createdAt: '2024-03-18T14:07:58Z'
updatedAt: '2025-12-29T00:42:59Z'
language: Rust
license: LGPL-2.1
branch: main
stars: 761
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:25.797Z'
description: Deploy with Nix and manage resources declaratively
tags: []
---


# NixOps4

See https://nixops.dev.

This project is intended to replace and improve on [NixOps 2](https://github.com/NixOS/nixops).
It fixes a number of structural issues through a rewrite from first principles.

**Status: in development**

## Goals

- Support stateless and stateful deployments.
- Fix the NixOps resource syntax.
- Provide a stable interface for defining resources, so that resource developers have a well-defined task, and minimal maintenance afterwards.
- Deployment projects provide can choose or provide their own resource implementations.
- Sustainable development, by reusing existing technologies such as the module system and OpenTofu.
- Maintainable code base in Rust.

## Hacking

The following will open a shell with dependencies, and install pre-commit for automatic formatting.

```console
$ nix develop
```

### VSCode

#### rust-analyzer

If the rust-analyzer extension fails, make sure the devShell was loaded into VSCode via Nix Env Selector or direnv.

## Credits

Thank you to the NixOps 1 / 2 authors and maintainers, for exploring the domain, and for their efforts to maintain and improve it.

Another special thanks goes to the [Fediversity](https://www.fediversity.eu) project, for their support to push NixOps over the bump that is NixOps4, and for their commitment to give back to the Nix community.
