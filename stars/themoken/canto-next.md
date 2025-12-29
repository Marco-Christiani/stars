---
repo: themoken/canto-next
url: 'https://github.com/themoken/canto-next'
homepage: ''
starredAt: '2023-01-31T22:24:41Z'
createdAt: '2011-08-30T18:48:01Z'
updatedAt: '2025-10-27T10:57:50Z'
language: Python
license: GPL-2.0
branch: master
stars: 159
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:00.960Z'
description: The next generation Canto RSS daemon
tags: []
---

# Canto Daemon

This is the RSS backend for Canto clients.

Canto-curses is the default client at:

http://github.com/themoken/canto-curses

## Requirements

    Debian / Ubuntu
    - python3
    - python3-feedparser

    Arch (Py3 is default)
    - python
    - python-feedparser

## Install

From this directory, run

```sh
    $ sudo python3 setup.py install
```


If you're a systemd user you can easily run it on startup

```sh
    $ systemctl --user enable canto-daemon
```

Or start it manually with

```sh
    $ systemctl --user start canto-daemon
```

By default, user sessions start on login, and end on logoff stopping daemons.
This is good behavior, but if you don't want canto-daemon to stop when you
log out (to keep gathering news) enable "lingering" for your account.

```
    $ loginctl enable-linger <username>
```

This will start one session for you on boot that will last until shutdown.
