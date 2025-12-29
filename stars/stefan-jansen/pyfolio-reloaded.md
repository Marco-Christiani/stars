---
repo: stefan-jansen/pyfolio-reloaded
url: 'https://github.com/stefan-jansen/pyfolio-reloaded'
homepage: 'https://pyfolio.ml4trading.io/'
starredAt: '2022-10-21T23:08:18Z'
createdAt: '2021-02-22T22:53:50Z'
updatedAt: '2025-12-29T07:12:07Z'
language: Jupyter Notebook
license: Apache-2.0
branch: main
stars: 566
isPublic: true
isTemplate: false
isArchived: false
isFork: true
hasReadMe: true
refreshedAt: '2025-12-29T17:35:13.830Z'
description: Portfolio and risk analytics in Python
tags: []
---

<p align="center">
<a href="https://pyfolio.ml4trading.io">
<img src="https://i.imgur.com/GD6TZ0D.png" width="35%">
</a>
</p>

![PyPI](https://img.shields.io/pypi/v/pyfolio-reloaded)
[![Tests](https://github.com/stefan-jansen/pyfolio-reloaded/actions/workflows/unit_tests.yml/badge.svg)](https://github.com/stefan-jansen/pyfolio-reloaded/actions/workflows/unit_tests.yml)
[![conda](https://github.com/stefan-jansen/pyfolio-reloaded/actions/workflows/conda_package.yml/badge.svg)](https://github.com/stefan-jansen/pyfolio-reloaded/actions/workflows/conda_package.yml)
[![PyPI](https://github.com/stefan-jansen/pyfolio-reloaded/actions/workflows/build_wheels.yml/badge.svg)](https://github.com/stefan-jansen/pyfolio-reloaded/actions/workflows/build_wheels.yml)
[![Coverage Status](https://coveralls.io/repos/github/stefan-jansen/pyfolio-reloaded/badge.svg?branch=main)](https://coveralls.io/github/stefan-jansen/pyfolio-reloaded?branch=main)
![GitHub issues](https://img.shields.io/github/issues/stefan-jansen/pyfolio-reloaded)
![Discourse users](https://img.shields.io/discourse/users?server=https%3A%2F%2Fexchange.ml4trading.io%2F)
![Twitter Follow](https://img.shields.io/twitter/follow/ml4trading?style=social)

pyfolio is a Python library for performance and risk analysis of financial portfolios that works well with the [Zipline](https://zipline.ml4trading.io/) open source backtesting library.

## Trading Strategy Analysis with pyfolio

At the core of pyfolio are various tear sheets that combine various individual plots and summary statistics to
provide a comprehensive view of the performance of a trading algorithm.

Here's an example of a simple tear sheet analyzing a strategy executed with the Zipline backtesting engine:

### Performance Metrics

The tear sheet presents performance and risk metrics for the strategy separately during the backtest and out-of-sample periods:

<p align="center">
<a href="#">
<img src="https://i.imgur.com/bfwMeIV.png" width="50%">
</a>
</p>

### Performance Plots

In addition, it visualizes how several risk and return metrics behave over time:

<p align="center">
<a href="#">
<img src="https://i.imgur.com/5Hyuet3.png" width="85%">
</a>
</p>

## Installation

To install pyfolio, run:

```bash
pip install pyfolio-reloaded
```
or

```bash
conda install -c ml4t pyfolio-reloaded
```

#### Development

For development, you may want to use a [virtual environment](https://docs.python-guide.org/en/latest/dev/virtualenvs/) to avoid dependency conflicts between pyfolio and other Python projects you have.

To get set up with a virtual env, run:
```bash
mkvirtualenv pyfolio
```

Next, clone this git repository and run `python -m pip install .[all]` and edit the library files directly.

## Usage

A good way to get started is to run the pyfolio examples in a
[Jupyter notebook](https://jupyter.org/). To do this, you first want to
start a Jupyter notebook server:

```bash
jupyter notebook
```

From the notebook list page, navigate to the pyfolio examples directory
and open a notebook. Execute the code in a notebook cell by clicking on it
and hitting Shift+Enter.


## Questions?

If you find a bug, feel free to [open an issue](https://github.com/stefan-jansen/pyfolio-reloaded/issues) in this repository.

You can also join our [community](https://exchange.ml4trading.io).

## Support

Please [open an issue](https://github.com/stefan-jansen/pyfolio-reloaded/issues/new) for support.

## Contributing

If you'd like to contribute, a great place to look is the [issues marked with help-wanted](https://github.com/stefan-jansen/pyfolio-reloaded/issues?q=is%3Aopen+is%3Aissue+label%3A%22help+wanted%22).

For a list of core developers and outside collaborators, see [the GitHub contributors list](https://github.com/stefan-jansen/pyfolio-reloaded/graphs/contributors).
