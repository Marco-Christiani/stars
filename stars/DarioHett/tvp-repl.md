---
repo: DarioHett/tvp-repl
url: 'https://github.com/DarioHett/tvp-repl'
homepage: null
starredAt: '2024-06-10T15:41:55Z'
createdAt: '2020-02-29T21:35:00Z'
updatedAt: '2024-06-10T15:41:55Z'
language: Shell
license: MIT
branch: master
stars: 2
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:44.586Z'
description: Tmux-enabled vim-ipython REPL
tags: []
---

## tvp-repl

![Demo](https://raw.githubusercontent.com/DarioHett/tvp-repl/master/demo.gif)

This repository configures [t]mux in junction with [v]im and [p]ython for a 
comfy REPL experience. Fixed plugins on the one hand and convoluted blog posts 
on the other, I decided to upload my gist.  

Debian-based distributions can be configured using the setup.sh.

The magic consists of four inputs:
1. xclip
2. vim with +clipboard
    .vimrc: 
    ```
    set clipboard=unnamedplus
    vnoremap <C-c> "+y
    ```
3. tmux bindings to dump the clipboard
.tmux.conf:
```
bind-key Enter run "tmux send-keys -t 0 C-c" \; 
    run "tmux select-pane -t 1" \; 
    run "tmux set-buffer \"$(xclip -o -sel clipboard)\"; tmux paste-buffer" \; 
    run "tmux send-keys -t 1 Enter" \; 
    run "tmux select-pane -t 0"
```
4. Load tmux with vim and ipython in a pre-set comfy REPL setup.
~/bin/tvp-repl:
```
#!/bin/sh
FILE=$1
tmux new-session \; \
  send-keys 'vim '${FILE} C-m \; \
  split-window -h \; \
  send-keys 'ipython '${FILE} C-m \; \
  select-pane -t 0 \; 
```

**Suggestions:**
1. .vimrc: Set a custom short cut. CTRL+C is a personal default.
2. Choose different window setup, i.e. put the ipython pane to the bottom with
```
split-window -v -l 5
```
3. Add an input for a conda environment for ipython.
``` 
ENV=$2
[...]
  send-keys 'conda activate '${ENV}'; clear; ipython '${FILE} C-m \; \
 [...]
```
