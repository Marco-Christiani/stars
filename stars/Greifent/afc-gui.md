---
repo: Greifent/afc-gui
url: 'https://github.com/Greifent/afc-gui'
homepage: ''
starredAt: '2022-12-27T20:27:27Z'
createdAt: '2020-04-24T21:12:17Z'
updatedAt: '2025-12-12T09:00:00Z'
language: Python
license: MIT
branch: master
stars: 44
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:05.165Z'
description: GUI for the asus-fan-control project
tags:
  - afc
  - afc-gui
  - asus-fan-control
  - gitpack
  - gtk4
  - gui
  - linux
  - python
---

# afc-gui
GUI for the asus-fan-control project

# Dependency:
* asus-fan-control installed
* python3
* Gtk4, for those that are unable to install gtk4, [here](https://github.com/Greifent/afc-gui-gtk3/) there is the gtk3 version, with the same functionalities 

# Installation:
 * If you have a previous version installed delete afc-gui and MAINGUI.glade from ~/.local/bin/ and then install using one of the methods below

 * Using [GitPack](https://github.com/dominiksalvet/gitpack): `sudo gitpack install https://github.com/Greifent/afc-gui.git`, then just type in the terminal `afc-gui` or look for afc-gui in your launcher.

 * Manual installation:
 
To install just run these commands
```
git clone https://github.com/Greifent/afc-gui.git
cd afc-gui/src/
sudo cp afc-gui /usr/bin/
sudo mkdir /usr/share/afc-gui
sudo cp afc-gui-gtk4.ui /usr/share/afc-gui/
sudo cp afc-gui.desktop /usr/share/applications/
```
To uninstall these:
```
sudo rm /usr/bin/afc-gui
sudo rm -r /usr/share/afc-gui/
sudo rm /usr/share/applications/afc-gui.desktop
```
To update the version run the uninstall commands, then the install ones.

# Photo:

This is the preset page

![](images/Preset.png)

This is the main page

![](images/Mainpage.png)

This is the info page

![](images/Infopc.png)

This is the about page

![](images/About.png)
