---
repo: WestHealth/pyvis
url: 'https://github.com/WestHealth/pyvis'
homepage: 'http://pyvis.readthedocs.io/en/latest/'
starredAt: '2022-12-29T02:17:09Z'
createdAt: '2018-05-10T00:42:44Z'
updatedAt: '2025-12-28T23:08:05Z'
language: HTML
license: BSD-3-Clause
branch: master
stars: 1158
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:04.914Z'
description: Python package for creating and visualizing interactive network graphs.
tags:
  - network-visualization
  - networkx
  - python
---

## Pyvis - a Python library for visualizing networks

![](pyvis/source/tut.gif?raw=true)

## Description
Pyvis is built around [visjs](http://visjs.org/), a JavaScript visualization library.

## Documentation
Pyvis' full documentation can be found at http://pyvis.readthedocs.io/en/latest/
## Installation
You can install pyvis through pip:

```bash
pip install pyvis
```
Or if you have an archive of the project simply run the following from the top level directory:

```bash
python setup.py install
```

## Dependencies
[networkx](https://networkx.github.io/)

[jinja2](http://jinja.pocoo.org/)

[ipython](https://ipython.org/ipython-doc/2/install/install.html)

[jsonpickle](https://jsonpickle.github.io/)

### Test Dependencies
[selenium](https://www.selenium.dev/documentation/webdriver/)

[numpy](https://numpy.org/install/)
## Quick Start
The most basic use case of a pyvis instance is to create a Network object and invoke methods:

```python
from pyvis.network import Network

g = Network()
g.add_node(0)
g.add_node(1)
g.add_edge(0, 1)
g.show("basic.html")
```

## Interactive Notebook playground with examples
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/WestHealth/pyvis/master?filepath=notebooks%2Fexample.ipynb)
