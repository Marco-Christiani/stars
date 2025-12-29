---
repo: sbucaille/phd_template
url: 'https://github.com/sbucaille/phd_template'
homepage: ''
starredAt: '2024-03-20T15:51:04Z'
createdAt: '2023-02-22T20:10:35Z'
updatedAt: '2024-05-10T21:53:58Z'
language: Python
license: NA
branch: master
stars: 3
isPublic: true
isTemplate: true
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:47.802Z'
description: >-
  Template to create training pipeline using PytorchLighning, Hydra and DVC
  frameworks
tags:
  - deep-learning
  - dvc
  - hydra
  - pytorch-lightning
---

# phd_template
Template to create training pipeline using PytorchLighning, Hydra and DVC tools

Medium article : soon

Instructions :
```bash
cd docker
docker build -t phd .
cd ..
docker run -it -shm-size=1g -v .:/app phd python <train|model_to_onnx|...>.py 
```
