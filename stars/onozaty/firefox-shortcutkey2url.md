---
repo: onozaty/firefox-shortcutkey2url
url: 'https://github.com/onozaty/firefox-shortcutkey2url'
homepage: ''
starredAt: '2023-12-10T19:24:39Z'
createdAt: '2013-07-14T08:20:25Z'
updatedAt: '2023-12-10T19:24:39Z'
language: JavaScript
license: NA
branch: master
stars: 12
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:52.900Z'
description: ShortcutKey2URL - Firefox Extension
tags:
  - firefox
---

# ShortcutKey2URL for Firefox WebExtensions

ShortcutKey2URL for Firefox WebExtensions is an extension for Firefox that allows you to open, and move url using shortcut keys. You can also run JavaScript.

Display the action list with the startup key and execute the action with the next key.

The startup key default is Ctrl+Period(on mac, Command+Period). You can change this key later. 

Characters that can be used as keys are not limited to one character. It can be set as multiple characters. ShrotcutKey2URL executes its action from the characters entered consecutively as keys when the target is narrowed down to one.

The items that can be set as actions are as follows.

* Jump to URL. For already opened URL, go to that tab. Open it as a new tab if it is not already open.
* Open URL in new tab.
* Open URL in current tab.
* Execute the JavaScript on the current tab.
* Open URL as a new tab and then execute the JavaScript.
* Open specified URL in incognito window.
* Open same URL as the current tab in incognito window.

I released WebExtensions version in Firefox 60.

## Installation

Install from the following.

* [ShortcutKey2URL \(WebExtensions\) \- Add\-ons for Firefox](https://addons.mozilla.org/en-US/firefox/addon/shortcutkey2url/)

## Usage

Since it is same to Chrome version, please refer to the following.

* [chrome\-shortcutkey2url/README\.md at master · onozaty/chrome\-shortcutkey2url](https://github.com/onozaty/chrome-shortcutkey2url/blob/master/README.md)

To enable the Open Private Window actions, go to Extension Details and set "Run in Private Window" to "Allow".
