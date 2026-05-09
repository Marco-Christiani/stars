---
repo: hermeticbuild/llvm-redist
url: 'https://github.com/hermeticbuild/llvm-redist'
homepage: null
starredAt: '2026-05-02T04:39:10Z'
createdAt: '2026-03-03T15:27:58Z'
updatedAt: '2026-05-02T04:39:11Z'
language: Shell
license: NA
branch: main
stars: 13
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-05-09T22:35:14.867Z'
description: >-
  A repository that publishes more lightweight LLVM releases (mirroring official
  releases)
tags: []
---

# llvm-redist

`llvm-redist` republishes official LLVM source release archives in `.tar.zst` format.

Scope:
- take upstream LLVM source releases (`llvm-project-*.src.tar.xz`)
- publish equivalent source archives as `.tar.zst`
- keep version-aligned artifacts, including release candidates (`-rc`)

Why this exists:
- provide a fast-to-consume mirror format for LLVM source redistribution
- keep upstream version identity while offering a different compression/container variant

Verify attestations:
- release artifacts are attested by GitHub Actions via the reusable builder workflow [`reusable-repack.yml`](/Users/corentinkerisit/code/github.com/hermeticbuild/llvm-redist/.github/workflows/reusable-repack.yml)
- verify a local artifact with:

```sh
tools/verify-attestation.sh out/llvm-project-21.1.8.src.tar.zst refs/heads/main
```

- equivalent raw `gh` command:

```sh
gh attestation verify out/llvm-project-21.1.8.src.tar.zst \
  --repo hermeticbuild/llvm-redist \
  --signer-workflow hermeticbuild/llvm-redist/.github/workflows/reusable-repack.yml \
  --source-ref refs/heads/main
```
