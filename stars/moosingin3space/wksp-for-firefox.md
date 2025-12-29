---
repo: moosingin3space/wksp-for-firefox
url: 'https://github.com/moosingin3space/wksp-for-firefox'
homepage: null
starredAt: '2023-08-09T16:11:21Z'
createdAt: '2018-04-10T18:31:43Z'
updatedAt: '2025-10-21T06:56:01Z'
language: JavaScript
license: Apache-2.0
branch: main
stars: 11
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:57.040Z'
description: 'Workspaces for Firefox, inspired by those in Linux desktop environments.'
tags: []
---

# Workspaces for Firefox

A Firefox Quantum extension designed to make interacting with tabs across
multiple Firefox windows, spread across different virtual desktops/workspaces,
easy.

[Get it from addons.mozilla.org](https://addons.mozilla.org/en-US/firefox/addon/workspaces-for-firefox/).

## Usage

![The Palette in action](./help/palette.png)

Press **Alt-Space** (**Ctrl-Space** on Windows) to launch the Palette. In the
Palette, you may search for a tab, regardless of where it is. Press **Enter**,
or click the tab, to switch to it. Hold **Shift** while pressing **Enter**, or
click the "paste" icon next to the tab, to "teleport" the tab into the current
window. The tab will be transferred with no loss in history or other state.
Finally, you can close tabs by clicking the close box at the right side of the
tab in the list.

## Building

To build this extension, simply run:

```sh
$ yarn
$ yarn build
```

inside the project directory. It will create the output file
`web-ext-artifacts/workspaces_for_firefox-${VERSION}.zip`.
