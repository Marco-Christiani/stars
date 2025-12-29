---
repo: Alex108-lab/Qtile-config
url: 'https://github.com/Alex108-lab/Qtile-config'
homepage: ''
starredAt: '2022-11-27T21:03:17Z'
createdAt: '2021-03-27T01:51:33Z'
updatedAt: '2025-12-02T21:42:41Z'
language: Python
license: NA
branch: master
stars: 19
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:07.555Z'
description: >-
  Qtile configuration is very nice, contains everything you need to run on both
  desktops and laptops
tags:
  - archlinux
  - python
  - qtile
  - windowmanager
---

# Qtile Config


![Qtile](./Screenshot/screen01.png)

***Language***
- [Español](./README.es.md)
- English

## Installation (Arch based)

Install Qtile and dependencies:

```
sudo pacman -S qtile pacman-contrib
yay -S nerd-fonts-ubuntu-mono
pip install psutil
```

Clone this repository and copy my configs:

```bash
git clone https://github.com/Alex108-lab/Qtile-config.git
cp -r Qtile-config/qtile ~/.config/
```

Test it with **[Xephyr](https://wiki.archlinux.org/index.php/Xephyr)**:

```bash
Xephyr -br -ac -noreset -screen 1280x720 :1 &
DISPLAY=:1 qtile
```

If the network widget doesn't work check ```./settings/widgets.py``` and look
for this line, you should find it inside a list called *primary_widgets*:

```python
# Change interface arg, use ip address to find which one you need
 widget.Net(**base(bg='color3'), interface='wlp2s0'),
```

## Structure

In ```config.py```, which is the file where most people write all their config,
I only have an *autostart* function and some other variables like
*cursor_warp*.

```python
@hook.subscribe.startup_once
def autostart():
    subprocess.call([path.join(qtile_path, 'autostart.sh')])
```

If you want to change *autostart* programs, open  ```./autostart.sh```.

```bash
#!/bin/sh

# systray battery icon
cbatticon -u 5 &
# systray volume
volumeicon &
```

If you want to modify keybindings, open ```./settings/keys.py```. To modify
workspaces, use ```./settings/groups.py```. Finally, if you want to add more
layouts, check ```./settings/layouts.py```, the rest of files don't need any
configuration.

## Themes

To set a theme, check which ones are available in ```./themes```, and write
the name of the theme you want in a file named ```./config.json```:

```json
{
    "theme": "material-ocean"
}
