---
repo: mil-ad/stui
url: 'https://github.com/mil-ad/stui'
homepage: ''
starredAt: '2025-03-07T06:48:32Z'
createdAt: '2020-05-28T22:32:02Z'
updatedAt: '2025-12-20T14:14:32Z'
language: Python
license: MIT
branch: main
stars: 101
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:33.059Z'
description: A Slurm dashboard for the terminal.
tags:
  - python
  - slurm
  - slurm-cluster
  - slurm-utility
  - terminal-based
  - tui
  - urwid
---

![PyPI](https://img.shields.io/pypi/v/stui)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

# stui
A Slurm dashboard for the terminal.

<img src="https://mil.ad/assets/stui_screenshot.png" alt="stui screenshot" width="80%"/>

## Features
* Connect to local Slurm cluster or remote clusters via SSH
* Quickly filter jobs based on commonly-used criteria
* Cancel, attach to, or modify properties of selected jobs.

## Installation

```shell
$ pip install stui
```

## Usage

On a machine that's part of a Slurm cluster simply fire up `stui`:

```shell
$ stui
```

To connect to a remote Slurm cluster via SSH:

```shell
$ stui --ssh REMOTE_HOST
```

where `REMOTE_HOST` is the hostname (or IP address) of the remote machine and may include the user and/or port parameters, of the form `user@host`, `host:port`, or `user@host:port`. If authentication via SSH keys or agent fails you will be prompted to manually enter username and password.
