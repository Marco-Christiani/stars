---
repo: nalepae/pandarallel
url: 'https://github.com/nalepae/pandarallel'
homepage: 'https://nalepae.github.io/pandarallel'
starredAt: '2022-10-26T14:59:33Z'
createdAt: '2019-03-10T11:58:29Z'
updatedAt: '2025-12-27T20:11:18Z'
language: Python
license: BSD-3-Clause
branch: master
stars: 3804
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:13.403Z'
description: "A simple and efficient tool to parallelize Pandas operations on all available\_CPUs"
tags:
  - pandas
  - parallel
  - python
---

# Pandaral·lel

[![PyPI version fury.io](https://badge.fury.io/py/pandarallel.svg)](https://pypi.python.org/pypi/pandarallel/)
[![PyPI license](https://img.shields.io/pypi/l/pandarallel.svg)](https://pypi.python.org/pypi/pandarallel/)
[![PyPI download month](https://img.shields.io/pypi/dm/pandarallel.svg)](https://pypi.python.org/pypi/pandarallel/)

| Without parallelization  | ![Without Pandarallel](https://github.com/nalepae/pandarallel/blob/master/docs/progress_apply.gif?raw=true)       |
| :----------------------: | ----------------------------------------------------------------------------------------------------------------- |
| **With parallelization** | ![With Pandarallel](https://github.com/nalepae/pandarallel/blob/master/docs/progress_parallel_apply.gif?raw=true) |

**Pandaral.lel** provides a simple way to parallelize your pandas operations on all your
CPUs by changing only one line of code. It also displays progress bars.

## **⚠️ Pandaral·lel is looking for a maintainer! ⚠️**

If you are interested, please contact me or open a GitHub issue.

## Maintainers
- [Manu NALEPA](https://github.com/nalepae)

## Former maintainers (thanks a lot for your work!)
- [till-m](https://github.com/till-m)

## Installation

```bash
pip install pandarallel [--upgrade] [--user]
```

## Quickstart

```python
from pandarallel import pandarallel

pandarallel.initialize(progress_bar=True)

# df.apply(func)
df.parallel_apply(func)
```

## Usage

Be sure to check out the [documentation](https://nalepae.github.io/pandarallel).

## Examples

An example of each available `pandas` API is available:

- For [Mac & Linux](https://github.com/nalepae/pandarallel/blob/master/docs/examples_mac_linux.ipynb)
- For [Windows](https://github.com/nalepae/pandarallel/blob/master/docs/examples_windows.ipynb)
