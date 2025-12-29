---
repo: LuRsT/hr
url: 'https://github.com/LuRsT/hr'
homepage: ''
starredAt: '2024-05-26T20:41:40Z'
createdAt: '2014-02-10T19:54:39Z'
updatedAt: '2025-12-21T08:10:48Z'
language: Roff
license: MIT
branch: master
stars: 1297
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:45.525Z'
description: ' A horizontal :straight_ruler: for your terminal'
tags:
  - cli
  - shell
  - utils
---

hr
==

A horizontal ruler for your terminal

Tired of not finding things in your terminal because there's a lot of logs and
garbage? Tired of destroying the Enter key by creating a "void zone" in your
terminal so that you can see the error that you're trying to debug?

## Setup

### Linux

#### Quick install

    $ curl https://raw.githubusercontent.com/LuRsT/hr/master/hr > ~/bin/hr
    (Examine ~/bin/hr)
    $ chmod +x ~/bin/hr

Note: You should have `~/bin` in your `$PATH` for this to work.

#### Complete install

    $ git clone git@github.com:LuRsT/hr.git
    $ cd hr

Open `Makefile` and edit the `PREFIX` variable, specifying the directory
where you'd want the software to reside. Then:

    $ sudo make install

### OSX

OSX users can install using Homebrew:

    $ brew install hr

## How to use it?

    $ hr
    ################################## # Till the end of your terminal window
    $

    $ hr '*'
    ********************************** # Till the end of your terminal window
    $

You can also make "beautiful" ASCII patterns

    $ hr - '#' -
    ----------------------------------
    ##################################
    ----------------------------------
    $ hr '-#-' '-' '-#-'
    -#--#--#--#--#--#--#--#--#--#--#--
    ----------------------------------
    -#--#--#--#--#--#--#--#--#--#--#--


That's it, no requirements, just pure old POSIX shell and `tput`, check the source,
it's free.

## More

Check out more information in `hr`s [wiki](https://github.com/LuRsT/hr/wiki)
