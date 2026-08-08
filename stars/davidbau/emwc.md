---
repo: davidbau/emwc
url: 'https://github.com/davidbau/emwc'
homepage: null
starredAt: '2026-08-07T19:28:27Z'
createdAt: '2026-08-03T10:15:08Z'
updatedAt: '2026-08-07T19:28:28Z'
language: TeX
license: NA
branch: main
stars: 4
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-08-08T22:50:28.819Z'
description: >-
  Engineering Machine-Written Code: a modern software engineering textbook for
  building large, dependable systems with LLM coding agents
tags: []
---

# Engineering Machine-Written Code

Working manuscript and research for a modern software engineering textbook
about building large, dependable systems with LLM coding agents.

## Repository layout

- [`text/`](text/) — the book manuscript; see the
  [reading-order table of contents](text/README.md)
- [`figures/`](figures/) — editable diagram sources
- [`notes/book-plan.md`](notes/book-plan.md) — thesis, structure, course plan,
  and editorial questions
- [`notes/manuscript-plan.md`](notes/manuscript-plan.md) — complete first-draft
  architecture and chapter production protocol
- [`research/`](research/) — chapter source maps, fact checks, and comparative
  analysis

Pinned third-party source trees used for research live locally under
`research/vendor/`. Their upstream URLs and commits are recorded in
[`research/SOURCES.md`](research/SOURCES.md); the trees themselves are not
stored in this repository.

## Build the book

The PDF build requires Pandoc 3, XeLaTeX, and GNU Make. From the repository
root, run:

```sh
make
```

This assembles the manuscript in reading order, renders the Mermaid diagrams
as native vector figures, and writes
`build/engineering-machine-written-code.pdf`. It also creates the convenient
local link `book.pdf`.

Use `make check` to render the book and run basic PDF integrity checks, or
`make clean` to remove generated artifacts.
