---
repo: wronnyhuang/gen-viz
url: 'https://github.com/wronnyhuang/gen-viz'
homepage: ''
starredAt: '2025-10-06T08:00:43Z'
createdAt: '2019-05-30T16:41:28Z'
updatedAt: '2025-12-15T07:52:07Z'
language: Python
license: NA
branch: master
stars: 65
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:26.497Z'
description: Code for the paper "Understanding Generalization through Visualizations"
tags: []
---

# Visualizing Generalization Phenomena 

The code for this paper is split up into different directories for each section of the paper, and each directory has its own README for how to run the code.
- [`minefield`](minefield) contains the code to train a good model and look for
  bad minima along its trajectory (Figure 1)
- [`linear_model`](linear_model) contains the code for training the overparametrized linear model and neural net (Figure 2)
- [`optimizers`](optimizers) contains the code for training on CIFAR using different optimizers (Figure 2, Table 1)
- [`swissroll`](swissroll) contains the code for all figures on the swiss roll dataset (Figures 3, 5, 6)
- [`svhn`](svhn) contains the code for all figures on the SVHN dataset (Figures 4, 5, 7)
- [`concentric_circles`](concentric_circles) contains the code for the concentric circles wide margins experiments (Figure 8)
