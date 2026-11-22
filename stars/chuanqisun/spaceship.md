---
repo: chuanqisun/spaceship
url: 'https://github.com/chuanqisun/spaceship'
homepage: 'https://chuanqisun.github.io/spaceship/'
starredAt: '2026-11-19T07:45:27Z'
createdAt: '2026-11-16T14:43:45Z'
updatedAt: '2026-11-22T01:10:50Z'
language: HTML
license: MIT
branch: master
stars: 1024
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-11-22T02:19:12.272Z'
description: Steer ideas like a space pilot!
tags: []
---

# 🕹️ Spaceship IDE

Steer ideas like a space pilot!

![Screencast](./extra/screencast.gif)

## Demos

Watch on [Instagram](https://www.instagram.com/reels/DfyQPhFtW-z/) and [YouTube](https://www.youtube.com/watch?v=3WmNLWUmcnY). You can try the simulator at [https://chuanqisun.github.io/spaceship/](https://chuanqisun.github.io/spaceship/) with the option to go live with your API keys for Cerebras and Gemini. Keys stay in your browser local storage. Do it at your own risk.

## Conjecture

> In the near future, LLM and Decision Models will reach 60 FPS interactivity.

When that happens, what new interaction paradigms will unlock? This project demonstrates plausible and desirable interactions for that future.

1. **Focus monitor**: can we visualize what LLM is paying attention to, and use that to guide human's focus towards what's important?

   ![focus monitor](./extra/clips/focus-monitor.gif)

2. **Attention lock**: can we force LLM to pay more attention to specific phrases so as to bias its future behavior?

   ![attention lock](./extra/clips/attention-lock.gif)

3. **Future Vector Steering**: can we decompose the task into eigenvectors, independently tune each, and re-compose them to influence the incoming text?

   ![future steering](./extra/clips/future-steering.gif)

4. **Realtime re-generation**: when text generation is cheap and fast, can we explore alternative futures by scrubbing?

   ![realtime regeneration](./extra/clips/realtime-regeneration.gif)

## Design process

I used Claude Code for most of the implementation but stayed hands-on for the UI/UX. I iterate using interactive style swatch, a technique where I prompt AI to give me diverse options of designs, I provide feedback, and it iterates. You can see the design artifacts in the [extra page](https://chuanqisun.github.io/spaceship/extra/style-1.html).

To achieve the realtime experience, I have to use agreesive speculative generation and manage cache invalidation based on user interactions. For example, when the main knob moves backward, I have to empty future texts and cancel ongoing requests. There are many considerations like this throughout the system and that took a lot of human judgement - claude didn't one shot them.

## Theory

I'm currently focusing on systems that help human shape ideas in realtime. This project is a small step towards my [upcoming thesis](https://code.chuanqisun.com/master-thesis/) at the MIT Media Lab, where I investigate how semantic and symoblic systems can be coupled to enhance human creativity, agency, and joy of craft.

## Community

This repo can be the conceptual launchpad for new designs and applications. Here is what the community has built. Open a PR to add yours!

- [Spaceship Writer](https://marketplace.visualstudio.com/items?itemName=brentlee-personal.spaceship-writer), a VSCode Extension by [brentlee](https://github.com/brentlee-personal), an independent adaptation of Chuanqi Sun’s Future Vector Steering design ([Source](https://github.com/brentlee-personal/spaceship-vscode) · [Demo in VS Code on Linux](https://github.com/brentlee-personal/spaceship-vscode/releases/download/v0.3.0/spaceship-writer-0.3.0-linux.mp4))
- [Spaceship Lime](https://spaceship-lime.vercel.app), steer local models in browser, by [Philippe](https://github.com/philippe-page)
- [Story Pilot](https://beyondchat.design/lab/story-pilot/), design pattern distilled by [Dominik](https://www.linkedin.com/in/dominikwitzke/)

## Citation

If you build on this work, please cite it as:

```bibtex
@misc{sun2026spaceship,
  author       = {Sun, Chuanqi},
  title        = {Spaceship {IDE}: Steer Your Ideas in Realtime, Space Pilot Style},
  year         = {2026},
  publisher    = {GitHub},
  howpublished = {\url{https://github.com/chuanqisun/spaceship}},
  note         = {Demo: \url{https://chuanqisun.github.io/spaceship/}}
}
```
