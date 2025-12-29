---
repo: markfirmware/zig-bare-metal-raspberry-pi
url: 'https://github.com/markfirmware/zig-bare-metal-raspberry-pi'
homepage: ''
starredAt: '2024-04-15T18:27:49Z'
createdAt: '2019-09-20T02:55:23Z'
updatedAt: '2025-12-23T10:13:48Z'
language: Zig
license: NA
branch: master
stars: 104
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:46.694Z'
description: Bare metal raspberry pi program written in zig
tags:
  - bare-metal
  - raspberry-pi
  - zig
---

Privacy
-------

Bluetooth signals are collected and displayed on the screen

Function
--------

zig logo is displayed

The frame buffer cursor moves around the screen in response to the tv remote controller buttons. This requires the Consumer Electronics Control (CEC) feature on the tv.

Presently only working on rpi3b+ due to some code generation issues

Not yet working on armv6 raspberry pi models

Not yet tested on rpi4b

Testing
-------

    zig build qemu -Dqemu

(yes, the -Dqemu is needed at this time)

or

    zig build qemu -Dqemu -Dnodisplay

to omit the frame buffer display
