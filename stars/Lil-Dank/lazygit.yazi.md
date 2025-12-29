---
repo: Lil-Dank/lazygit.yazi
url: 'https://github.com/Lil-Dank/lazygit.yazi'
homepage: null
starredAt: '2025-10-07T15:00:39Z'
createdAt: '2024-08-16T09:32:35Z'
updatedAt: '2025-12-25T21:52:48Z'
language: Lua
license: MIT
branch: main
stars: 50
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:26.299Z'
description: lazygit plugin for yazi
tags: []
---

# lazygit.yazi
Plugin for [Yazi](https://github.com/sxyazi/yazi) to manage git repos with [lazygit](https://github.com/jesseduffield/lazygit)
## Dependencies
Make sure [lazygit](https://github.com/jesseduffield/lazygit) is installed and in your `PATH`.
## Installation

### Using `ya pkg`
```
 ya pkg add Lil-Dank/lazygit
```

### Manual
**Linux/macOS**
```
git clone https://github.com/Lil-Dank/lazygit.yazi.git ~/.config/yazi/plugins/lazygit.yazi
```
**Windows**
```
git clone https://github.com/Lil-Dank/lazygit.yazi.git %AppData%\yazi\config\plugins\lazygit.yazi
```
## Configuration
add this to your **keymap.toml** file
```toml
[[mgr.prepend_keymap]]
on   = [ "g", "i" ]
run  = "plugin lazygit"
desc = "run lazygit"
```
you can customize the keybinding however you like. Please refer to the [keymap.toml](https://yazi-rs.github.io/docs/configuration/keymap) documentation
## Disclaimer
**THIS PLUGIN IS FOR THE STABLE RELEASE OF YAZI, DON'T PROPOSE ANY CHANGES BASED ON PRE-RELEASES OF YAZI**
