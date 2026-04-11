---
repo: n0-computer/sendme
url: 'https://github.com/n0-computer/sendme'
homepage: null
starredAt: '2026-03-31T07:10:54Z'
createdAt: '2023-12-12T08:20:28Z'
updatedAt: '2026-04-07T20:58:26Z'
language: Rust
license: NOASSERTION
branch: main
stars: 978
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-04-11T22:33:48.997Z'
description: 'A tool to send files and directories, based on iroh'
tags: []
---

# Sendme

This is an example application using [iroh](https://crates.io/crates/iroh) with
the [iroh-blobs](https://crates.io/crates/iroh-blobs) protocol to send files and
directories over the internet.

It is also useful as a standalone tool for quick copy jobs.

Iroh will take care of hole punching and NAT traversal whenever possible,
and fall back to a relay if hole punching does not succeed.

Iroh-blobs will take care of [blake3](https://crates.io/crates/blake3) verified
streaming, including resuming interrupted downloads.

Sendme works with 256 bit node ids and is, therefore, location transparent. A ticket
will remain valid if the IP address changes. Connections are encrypted using
TLS.

# Installation

```
cargo install sendme
```

# Usage

## Send side

```
sendme send <file or directory>
```

This will create a temporary [iroh](https://crates.io/crates/iroh) node that
serves the content in the given file or directory. It will output a ticket that
can be used to get the data.

The provider will run until it is terminated using `Control-C`. On termination, it
will delete the temporary directory.

This currently will create a temporary directory in the current directory. In
the future this won't be needed anymore.

### Receive side

```
sendme receive <ticket>
```

This will download the data and create a file or directory named like the source
in the **current directory**.

It will create a temporary directory in the current directory, download the data
(single file or directory), and only then move these files to the target
directory.

On completion, it will delete the temp directory.

All temp directories start with `.sendme-`.
