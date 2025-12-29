---
repo: ionelmc/python-packaging-blunders
url: 'https://github.com/ionelmc/python-packaging-blunders'
homepage: null
starredAt: '2025-02-25T23:32:51Z'
createdAt: '2014-06-02T19:43:44Z'
updatedAt: '2025-08-26T16:16:53Z'
language: Python
license: NA
branch: master
stars: 10
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:34.194Z'
description: null
tags: []
---

``with-src`` - correct develop handling
=======================================

::

    + python setup.py develop
    ...
    + test-module
    ()
    + test-package
    ()
    + python -c 'import some_test_junk'
    Traceback (most recent call last):
      File "<string>", line 1, in <module>
    ImportError: No module named some_test_junk
    + true
    + python -c 'import setup'
    Traceback (most recent call last):
      File "<string>", line 1, in <module>
    ImportError: No module named setup

Perfect - we don't have junk on the import path.

``no-src`` - incorrect develop handling
=======================================

::

    + python setup.py develop
    ...
    + test-module
    ()
    + test-package
    ()
    + python -c 'import some_test_junk'
    This junk should not be importable !
    + python -c 'import setup'
    usage: -c [global_opts] cmd1 [cmd1_opts] [cmd2 [cmd2_opts] ...]
       or: -c --help [cmd1 cmd2 ...]
       or: -c --help-commands
       or: -c cmd --help

    error: no commands supplied

This is bad, setuptools just added the root of the project on ``sys.path``. 
All the junk that would never go in ``site-packages`` (when you install the 
distribution) is now importable ...
