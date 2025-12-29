---
repo: rlhk/logseq-url-plus
url: 'https://github.com/rlhk/logseq-url-plus'
homepage: ''
starredAt: '2022-12-29T07:05:49Z'
createdAt: '2022-11-04T15:52:12Z'
updatedAt: '2025-09-26T14:37:33Z'
language: Clojure
license: MIT
branch: main
stars: 61
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:04.019Z'
description: >-
  A Logseq plugin that takes the last token of an editing block, be it a word or
  URL, and augments the block with associated metadata in various formats
tags:
  - clojure
  - clojurescript
  - logseq
  - logseq-plugin
  - plugin
  - url
---

# URL+ Plugin for Logseq

URL+ is a [Logseq](https://logseq.com) plugin written in [ClojureScript](https://clojurescript.org) with [shadow-cljs](https://github.com/thheller/shadow-cljs) as the main tooling.

The plugin takes the last token of an editing block, be it a word or URL, and augments the block with associated metadata in various formats. 

If the last token is a valid URL, metadata or API response is fetched, then the block is modified by applying a selected template. The plugin also fetches compact dictionary definition of a word term, or attach a few useful links to it.

![demo](demo.gif)

## Slash Commands

- `URL+ [title](url)`
- `URL+ [title](url) description`
- `URL+ Metadata -> Logseq Attributes`
- `URL+ Metadata -> EDN Code`
- `URL+ Metadata -> JSON Code`
- `URL+ API -> Logseq Attributes`
- `URL+ API -> Logseq Attribute Blocks`
- `URL+ API -> EDN Code`
- `URL+ API -> JSON Code`
- `URL+ Append Definition`
- `URL+ Extract tweet text of twitter.com`
  - Twitter developer access token required
  - Paste the token in the plugin settings panel
  - For details on the Twitter developer programme, see https://developer.twitter.com/en/docs/authentication/oauth-2-0/bearer-tokens
- `URL+ Inspector ...`
  - Opens the inspector UI for token insights and template customization
  ![Inspector UI](inspector-ui.png)

## Known Issues

### YouTube Short URL Handling
- The plugin currently does not handle YouTube short URLs (e.g., `https://youtu.be/abc123`)
- These short URLs need to be normalized to the full YouTube URL format (e.g., `https://www.youtube.com/watch?v=abc123`) for proper metadata extraction
- **TODO**: Implement URL normalization to convert short YouTube URLs to their canonical form before processing

## Why Another URL Formatter?

- Prefer slash command `/` over autoformat
- Need more formatting templates beyond the default `[title](url)`
- Works for block with multiple terms and even multiline. The plugin only considers the last term without other content in the active editing block
- Persist URL metadata or API response in graph
- Learn Logseq plugin dev with ClojureScript + Rum + Babashka + tailwindcss (Sample ClojureScript based plugin projects are rare when this project started)

## Plugin Devevelopment in ClojureScript

See [technical notes](./doc/dev-notes.md).
