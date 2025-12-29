---
repo: plibither8/ulauncher-zoom
url: 'https://github.com/plibither8/ulauncher-zoom'
homepage: 'https://ext.ulauncher.io/-/github-plibither8-ulauncher-zoom'
starredAt: '2022-11-21T22:55:03Z'
createdAt: '2021-06-25T07:17:38Z'
updatedAt: '2025-03-31T23:36:09Z'
language: Python
license: MIT
branch: master
stars: 9
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:09.886Z'
description: "\U0001F4F9 Join a Zoom meeting quickly from Ulauncher"
tags:
  - ulauncher
  - ulauncher-extension
  - zoom
---

# ulauncher-zoom

> 📹 Join a Zoom meeting quickly.

Quickly connect to a Zoom meeting using the meeting ID, and `xdg-open`.

## Install

### Requirements

- [Ulauncher 5](https://ulauncher.io/)
- Python >= 3

### Steps

1. Ulauncher > Preferences > Extensions > Add extension

2. Paste the following URL:

```
https://github.com/plibither8/ulauncher-zoom
```

3. Navigate to the `meetings.json` file and populate the JSON list with the meeting name, ID and password. Example:

```json
[
  {
    "name": "Personal Meeting",
    "id": "1234567890",
    "pwd": "ABC123"
  },
  {
    "name": "Engineering all-hands",
    "id": "3141592651",
    "pwd": "DEF456"
  }
]
```

You will find the `meetings.json` file where the Ulauncher extension has been downloaded. In most cases, look for it in: `~/.local/share/ulauncher/extensions/com.github.plibither8.ulauncher-zoom`.

## Usage

Default keyword to trigger this extension is **`zm`**. This can be changed in the preferences.

## License

[MIT](LICENSE)
