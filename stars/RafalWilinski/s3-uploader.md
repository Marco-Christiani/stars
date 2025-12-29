---
repo: RafalWilinski/s3-uploader
url: 'https://github.com/RafalWilinski/s3-uploader'
homepage: 'http://rwilinski.me'
starredAt: '2022-06-24T05:53:49Z'
createdAt: '2016-07-05T16:57:48Z'
updatedAt: '2025-06-29T08:11:11Z'
language: JavaScript
license: NA
branch: master
stars: 142
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:24.685Z'
description: "\U0001F34E macOS Electron+React App for uploading files to S3 directly from Status Bar"
tags:
  - election
  - electron
  - macos
  - s3
  - storage
  - upload
---

## aws-s3-uploader
Simple macOS app for uploading files to Amazon Web Services.
 
Just drag & drop files you'd like to upload on bucket icon displayed on your status bar or application window.

![Upload Animation](/upload_anim.gif?raw=true "Upload Anim")

#### Configuration
Simply click on bucket and follow instructions. You'll need access key and secret key for AWS user with S3 Exec Role.
You can also try modifying `.awscredentials.json` file on your own. 

#### Features
- logging in to AWS S3 account with access + secret keys
- upload files by dragging them on status bar icon and on window
- settings permissions and storage classes for uploads
- get S3 link by clicking uploaded file from list
- support for dropping many files at once and directories

#### Todo
- [x] Automatic login on start (no need to enter credentials with every start)
- [ ] Add possibility to abort uploads
- [ ] Tests!
- [ ] Packages for distribution
- [ ] Possibility to disable notifications & automatic URL-to-clipboard write

#### Credits
Special thanks to [parkjisun](https://thenounproject.com/naripuru/), [Sergey Furtaev](https://thenounproject.com/furtaev/), [Timothy Miller](https://thenounproject.com/tmthymllr/), [Joe Mortell](https://thenounproject.com/JoeMortell/) for Icons from [nounproject.com](https://thenounproject.com/)
