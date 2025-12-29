---
repo: openai/imitation
url: 'https://github.com/openai/imitation'
homepage: 'https://arxiv.org/abs/1606.03476'
starredAt: '2024-01-28T08:49:10Z'
createdAt: '2016-06-10T20:40:03Z'
updatedAt: '2025-12-28T14:48:53Z'
language: Python
license: MIT
branch: master
stars: 729
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:49.226Z'
description: ' Code for the paper "Generative Adversarial Imitation Learning"'
tags:
  - paper
---

**Status:** Archive (code is provided as-is, no updates expected)

=========================================
Generative Adversarial Imitation Learning
=========================================
-----------------------------------------
Jonathan Ho and Stefano Ermon
-----------------------------------------

Contains an implementation of Trust Region Policy Optimization (Schulman et al., 2015).

Dependencies:

* OpenAI Gym >= 0.1.0, mujoco_py >= 0.4.0
* numpy >= 1.10.4, scipy >= 0.17.0, theano >= 0.8.2
* h5py, pytables, pandas, matplotlib

Provided files:

* ``expert_policies/*`` are the expert policies, trained by TRPO (``scripts/run_rl_mj.py``) on the true costs
* ``scripts/im_pipeline.py`` is the main training and evaluation pipeline. This script is responsible for sampling data from experts to generate training data, running the training code (``scripts/imitate_mj.py``), and evaluating the resulting policies.
* ``pipelines/*`` are the experiment specifications provided to ``scripts/im_pipeline.py``
* ``results/*`` contain evaluation data for the learned policies
