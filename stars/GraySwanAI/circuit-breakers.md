---
repo: GraySwanAI/circuit-breakers
url: 'https://github.com/GraySwanAI/circuit-breakers'
homepage: ''
starredAt: '2024-08-25T18:27:44Z'
createdAt: '2024-06-06T15:44:56Z'
updatedAt: '2025-12-22T02:38:55Z'
language: Jupyter Notebook
license: MIT
branch: main
stars: 251
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:42.970Z'
description: Improving Alignment and Robustness with Circuit Breakers
tags: []
---

# Circuit Breakers

[[Paper](https://arxiv.org/abs/2406.04313)] | [[Website](http://circuit-breaker.ai/)] | [[Models](https://huggingface.co/collections/GraySwanAI/model-with-circuit-breakers-668ca12763d1bc005b8b2ac3)]

We present Circuit Breaking, a new approach inspired by [representation engineering](https://ai-transparency.org/), designed to prevent AI systems from generating harmful content by directly altering harmful model representations. The family of circuit-breaking (or short-circuiting as one might put it) methods provide an alternative to traditional methods like refusal and adversarial training, protecting both LLMs and multimodal models from strong, unseen adversarial attacks without compromising model capability. Our approach represents a significant step forward in the development of reliable safeguards to harmful behavior and adversarial attacks.

<img align="center" src="assets/splash.png" width="800">

## Snapshot of LLM Results

<img align="center" src="assets/llama_splash.png" width="800">

## Citation
If you find this useful in your research, please consider citing our [paper](https://arxiv.org/abs/2406.04313):
```
@misc{zou2024circuitbreaker,
title={Improving Alignment and Robustness with Circuit Breakers},
author={Andy Zou and Long Phan and Justin Wang and Derek Duenas and Maxwell Lin and Maksym Andriushchenko and Rowan Wang and Zico Kolter and Matt Fredrikson and Dan Hendrycks},
year={2024},
eprint={2406.04313},
archivePrefix={arXiv},
primaryClass={cs.LG}
}
```
