---
repo: LeaVerou/inspire.js
url: 'https://github.com/LeaVerou/inspire.js'
homepage: 'https://inspirejs.org'
starredAt: '2025-02-12T16:27:39Z'
createdAt: '2010-10-28T22:09:05Z'
updatedAt: '2025-12-14T05:41:06Z'
language: JavaScript
license: MIT
branch: master
stars: 1749
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:35.090Z'
description: 'Lean, hackable, extensible slide deck framework. Previously known as CSSS.'
tags:
  - presentation
  - slidedeck
  - slideshow
---

# Inspire.js

### Lean, hackable, extensible slide deck framework. Create basic slides by just writing HTML and CSS, do fancy custom stuff with JS, the sky is the limit!

## Getting started

### CDN

```html
<script src="https://inspirejs.org/inspire.js"></script>
```

or

```js
import Inspire from "https://inspirejs.org/inspire.mjs";
```

### NPM

```sh
npm install inspirejs.org
```

then


```html
<script src="node_modules/inspirejs.org/inspire.js"></script>
```

or

```js
import Inspire from "node_modules/inspirejs.org/inspire.mjs";
```

or if you use a bundler:

```js
import Inspire from "inspirejs.org";
```


### Quick start

- Copy (and rename) blank.html somewhere
- Also copy talk.css, theme.css
- Add Your Own Content
- Add talk-specific styling to talk.css

## Previously known as CSSS.

If you were using CSSS and would rather stay at it, run `git checkout v1.0.0` and stay there.

<details>

<summary>Migrating from CSSS</summary>

- Almost all HTML syntax is the same! The same JS events are still fired. So, very little should break.
- `slideshow.css` is now `inspire.css`
- `slideshow.js` is now `inspire.js`
- You don't need to run JS to create a slideshow, it is created automatically.
- The `SlideShow` JS class is now `Inspire`
- The `slideshow` JS variable is now `Inspire`
- Presenter view will not be loaded unless there is at least one `class="presenter-notes"` item.
- The CSS Controls plugin is now gone. Use [Mavo](https://mavo.io) if you need this functionality.
- The CSS Snippets plugin is now gone. We will soon add a much better one, extracted based on the live demo script in https://github.com/leaverou/talks.
- Incrementable is no longer a plugin. Use the separate script from https://github.com/leaverou/incrementable.
- `reusable.css` has now been merged into the default theme, `theme.css`.
- `data-import` is now `data-insert`

</details>

## API FAQ

### Running code after any imports have loaded

```js
await Inspire.importsLoaded;
// code to run after imports have loaded
```

Note that `await` needs to be inside an async function otherwise it will error. However, this could just be a self-executing async function.

### Running code after a specific plugin has loaded

```js
await Inspire.importsLoaded;
await Inspire.plugins.loaded.PLUGIN_ID.loaded;
// code to run after the plugin with id PLUGIN_ID has loaded and executed
```

or:

```js
await Inspire.loadPlugin(PLUGIN_ID);
// code to run after the plugin with id PLUGIN_ID has loaded and executed
```

The second example would load the plugin if it hasn't otherwise been loaded, but if it will never be loaded twice.

### Running code when a specific slide is displayed

You can do this via the `slidechange` hook:

```js
Inspire.hooks.add("slidechange", env => {
	if (Inspire.currentSlide.id === "slide-id") {
		// Code to run
	}
});
```

or, via an event:

```js
document.addEventListener("slidechange", evt => {
	if (Inspire.currentSlide.id === "slide-id") {
		// Code to run
	}
});
```

### Running code when a specific slide is displayed for the first time

You can do this via the `slidechange` hook:

```js
Inspire.hooks.add("slidechange", env => {
	if (Inspire.currentSlide.id === "slide-id" && env.firstTime) {
		// Code to run
	}
});
```

or, via an event:

```js
document.addEventListener("slidechange", evt => {
	if (Inspire.currentSlide.id === "slide-id" && evt.firstTime) {
		// Code to run
	}
});
```

or:

```js
$("#slide-id").addEventListener("slidechange", evt => {
	// Code to run
}, {once: true});
```

### Running code after a specific slide has been displayed

You can do this via the `slidechange` hook:

```js
Inspire.hooks.add("slidechange", env => {
	if (env.prevSlide.id === "slide-id") {
		// Code to run
	}
});
```

or, via an event:

```js
document.addEventListener("slidechange", evt => {
	if (evt.prevSlide.id === "slide-id") {
		// Code to run
	}
});
```
