---
repo: openai/finetune-transformer-lm
url: 'https://github.com/openai/finetune-transformer-lm'
homepage: >-
  https://s3-us-west-2.amazonaws.com/openai-assets/research-covers/language-unsupervised/language_understanding_paper.pdf
starredAt: '2023-11-10T19:53:32Z'
createdAt: '2018-06-11T06:04:40Z'
updatedAt: '2025-12-19T08:17:22Z'
language: Python
license: MIT
branch: master
stars: 2263
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:54.443Z'
description: >-
  Code and model for the paper "Improving Language Understanding by Generative
  Pre-Training"
tags:
  - paper
---

**Status:** Archive (code is provided as-is, no updates expected)

# finetune-transformer-lm
Code and model for the paper "Improving Language Understanding by Generative Pre-Training"

Currently this code implements the ROCStories Cloze Test result reported in the paper by running:
`python train.py --dataset rocstories --desc rocstories --submit --analysis --data_dir [path to data here]`

Note: The code is currently non-deterministic due to various GPU ops. The median accuracy of 10 runs with this codebase (using default hyperparameters) is 85.8% - slightly lower than the reported single run of 86.5% from the paper. 

The ROCStories dataset can be downloaded from the associated [website](http://cs.rochester.edu/nlp/rocstories/).
