---
repo: maxhumber/mummify
url: 'https://github.com/maxhumber/mummify'
homepage: 'https://maxhumber.github.io/mummify/'
starredAt: '2022-07-09T04:11:58Z'
createdAt: '2018-03-18T15:07:58Z'
updatedAt: '2025-11-06T03:08:00Z'
language: Python
license: MIT
branch: master
stars: 43
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:21.583Z'
description: Version Control for Machine Learning
tags:
  - git
  - machine-learning
  - version-control
---

<h3 align="center">
  <img src="https://raw.githubusercontent.com/maxhumber/mummify/master/assets/mummify.png" width="200px" alt="mummify">
</h3>
<p align="center">
  <a href="https://github.com/maxhumber/gazpacho/blob/master/setup.py"><img alt="Dependencies" src="https://img.shields.io/badge/dependencies-0-green"></a>
  <a href="https://travis-ci.org/maxhumber/mummify"><img alt="Travis" src="https://img.shields.io/travis/maxhumber/mummify.svg"></a>
  <a href="https://pypi.python.org/pypi/mummify"><img alt="PyPI" src="https://img.shields.io/pypi/v/mummify.svg"></a>
  <a href="https://pepy.tech/project/mummify"><img alt="Downloads" src="https://pepy.tech/badge/mummify"></a>  
</p>

### About

`mummify` is a version control tool for machine learning. It's simple, fast, and designed for model prototyping.

### Quickstart

<img src="https://raw.githubusercontent.com/maxhumber/mummify/master/assets/quickstart.gif" width="400px" alt="quickstart">

### Usage

Add `mummify.log(<string>)` to the bottom of a machine learning model:

```python
from sklearn.datasets import load_wine
from sklearn.neighbors import KNeighborsClassifier

import mummify

data = load_wine()
X, y = data.data, data.target

model = KNeighborsClassifier(n_neighbors=4)
model.fit(X, y)
accuracy = round(model.score(X, y), 4)

mummify.log(f'Accuracy: {accuracy}')
```

Run the model at the command line:

```sh
python model.py
```

Edit the model to implement another algorithm:

```python
...
model = LogisticRegression()
model.fit(X, y)
accuracy = round(model.score(X, y), 4)

mummify.log(f'Accuracy: {accuracy}')
```

Inspect model history at the command line with:

```sh
mummify history
```

And peek at the logged messages at the command line with:

```sh
cat mummify.log
```

Switch to an earlier version of the model:

```sh
mummify switch <id>
```

`mummify` will persist snapshots and the `mummify.log` file between switches.

### Installation

```sh
pip install mummify
```

### Contribute

For feature requests or bug reports, please use [Github Issues](https://github.com/maxhumber/chart/issues)
