---
repo: nitrogenez/zig-river-config
url: 'https://github.com/nitrogenez/zig-river-config'
homepage: ''
starredAt: '2025-08-30T21:32:45Z'
createdAt: '2024-06-05T21:31:10Z'
updatedAt: '2025-10-14T17:43:54Z'
language: Zig
license: BSD-3-Clause
branch: main
stars: 2
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:27.106Z'
description: River configuration with the power of a programming language.
tags:
  - configuration
  - river
  - riverwm
  - utility
  - wayland
  - wayland-compositor
  - zig
  - zig-lang
  - zig-language
  - zig-library
  - zig-package
  - ziglang
---

= zig-river-config
Andrij Glyko <nitrogenez.dev@tuta.io>
v0.3.0, 2024-06-06

:toc:
:homepage: https://github.com/nitrogenez/zig-river-config

zig-river-config is a Zig library made for 
https://github.com/riverwm/river[river] wayland compositor configuration. It provides
an API to define your configuration for the compositor while still having the 
power of a low-level, robust, and fast programming language. The version of zig-river-config is the same as
the version of https://github.com/riverwm/river[river]. zig-river-config has no 
official affiliation with the https://github.com/riverwm[riverwm] organisation.

== Warning

Keep in mind, that when working with a low-level programming language like Zig you need to
manage your resources manually. Any damage dealt to your machine is not my responsibility.

== Examples

For examples see link:src/init.zig[the default init].

== Usage

First of, run `zig fetch --save "git+https://github.com/nitrogenez/zig-river-config#COMMIT_HASH"`.
After that you need to add something like that to your build.zig:

.build.zig
[source,zig]
----
const zrc_dep = b.dependency("zig_river_config", .{ .optimize = optimize, .target = target });
your_exe.root_module.addImport("zrc", zrc_dep.module("zig-river-config"));
----

== License
This software is licensed under the 3-Clause BSD License.
See link:LICENSE[LICENSE] for more info.
