---
repo: Rapha149/ulauncher-bluetooth
url: 'https://github.com/Rapha149/ulauncher-bluetooth'
homepage: 'https://ext.ulauncher.io/-/github-rapha149-ulauncher-bluetooth'
starredAt: '2022-11-21T22:03:01Z'
createdAt: '2022-04-22T21:19:36Z'
updatedAt: '2023-10-27T18:55:44Z'
language: Python
license: GPL-3.0
branch: main
stars: 5
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:10.550Z'
description: Powerful Ulauncher tool for managing Bluetooth devices
tags:
  - bluetooth
  - ulauncher
  - ulauncher-extension
---

# Ulauncher Bluetooth
Powerful Ulauncher extension for managing Bluetooth devices

## Features
- Turn Bluetooth on/off
- Change adapter settings (alias, discoverable, pairable)
- Connect to paired devices
- Scan for nearby devices and pair
- Manage settings for paired devices (alias, trusted, blocked)

![home (bluetooth off)](https://user-images.githubusercontent.com/49787110/164912021-47f9374f-32fc-460f-86de-726e35a0de06.png)
![home (bluetooth on)](https://user-images.githubusercontent.com/49787110/164912123-a857ca97-e3c5-4f15-8d82-d68965a1278b.png)
![adapter settings](https://user-images.githubusercontent.com/49787110/164912052-2d6e21c8-43b5-47ef-959b-36551f00402a.png)
![device settings](https://user-images.githubusercontent.com/49787110/164912166-8bc239c3-7a80-4dae-8945-e7b68384af99.png)
![devices found while scanning](https://user-images.githubusercontent.com/49787110/164912265-31cb2cd4-c134-4166-b16f-35e8bc4f3df9.png)


## Requirements
- `tlp` package for the default command to turn bluetooth on/off (e.g. `sudo apt install tlp`)
- `pip install pydbus`
- `pip install PyGObject`
- `pip install wrapt-timeout-decorator`
