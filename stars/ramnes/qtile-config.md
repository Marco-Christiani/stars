---
repo: ramnes/qtile-config
url: 'https://github.com/ramnes/qtile-config'
homepage: ''
starredAt: '2022-11-27T21:00:15Z'
createdAt: '2014-03-11T03:26:37Z'
updatedAt: '2025-06-14T02:50:03Z'
language: Python
license: NA
branch: master
stars: 35
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:07.811Z'
description: My ~/.config/qtile
tags:
  - config
  - python
  - qtile
  - window-manager
---

qtile-config
============

My `~/.config/qtile`


Dependencies
------------

* [Qtile](https://github.com/qtile/qtile) (I'm constantly running on Qtile's
  HEAD, don't expect backward compatibility)
* Python (any >=3.5 version should work)


Install
-------

```
git clone git@github.com:ramnes/qtile-config.git ~/.config/qtile
```


Debug
-----

```
sudo DEBUG=1 startx ~/.config/qtile/xinitrc -- :1 vt8
```

(this command can be simplified depending on your Linux setup)


Manhole
-------

This config adds a manhole to Qtile if `aiomanhole` is installed.

Access the manhole with:

```
nc localhost 7113
```

For example:

```
$ nc localhost 7113
>>> qtile.current_window.hide()
>>> ^C
```

What it looks like (or used to)
-------------------------------

![Screenshot (empty)](https://i.imgur.com/P64wjPd.jpg)
![Screenshot (busy)](http://i.imgur.com/9QXliel.jpg)
