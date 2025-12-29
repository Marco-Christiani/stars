---
repo: getditto/authtool
url: 'https://github.com/getditto/authtool'
homepage: null
starredAt: '2023-11-20T15:41:42Z'
createdAt: '2022-05-05T00:00:32Z'
updatedAt: '2025-01-16T23:44:59Z'
language: Rust
license: Apache-2.0
branch: main
stars: 3
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:54.158Z'
description: Generate authentication for devices in a Ditto mesh
tags: []
---

# Ditto authtool

A CLI tool and Rust library to generate authentication for devices in [a Ditto mesh](https://ditto.live).

To generate a key for [shared key authentication](https://docs.ditto.live/security/shared-key) install the tool and run:

```
ditto-authtool generate-shared-key
```

## Install

### Prebuilt Release

Head to the [Releases page](https://github.com/getditto/authtool/releases) and download the binary for your platform.

Mac users may need to remove the quarantine flag:

```
xattr -r -d com.apple.quarantine ./ditto-authtool
```

### From Source

Ensure you have a stable Rust toolchain installed with [rustup](https://rustup.rs/). Clone this repository and open a
terminal inside it. Run:

```
cargo install --path . 
```

The `ditto-authtool` binary will be built and placed in your PATH (generally `~/.cargo/bin`).

### Library Use

The `ditto-authtool` crate can also be embedded in your own Rust software to automate your authentication workflows.
Generate docs with `cargo doc --open`.
