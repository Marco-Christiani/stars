---
repo: xarray-contrib/cf-xarray
url: 'https://github.com/xarray-contrib/cf-xarray'
homepage: 'https://cf-xarray.readthedocs.io/'
starredAt: '2025-05-29T16:49:11Z'
createdAt: '2020-05-27T17:16:39Z'
updatedAt: '2025-12-11T19:21:23Z'
language: Python
license: Apache-2.0
branch: main
stars: 176
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:29.450Z'
description: an accessor for xarray objects that interprets CF attributes
tags:
  - cf-conventions
  - metadata
  - xarray
---

.. image:: https://img.shields.io/static/v1.svg?logo=Jupyter&label=Pangeo+Binder&message=GCE+us-central1&color=blue&style=for-the-badge
    :target: https://binder.pangeo.io/v2/gh/xarray-contrib/cf-xarray/main?urlpath=lab
    :alt: Binder

.. image:: https://img.shields.io/readthedocs/cf-xarray/latest.svg?style=for-the-badge
    :target: https://cf-xarray.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation Status

.. image:: https://img.shields.io/github/actions/workflow/status/xarray-contrib/cf-xarray/ci.yaml?branch=main&logo=github&style=for-the-badge
    :target: https://github.com/xarray-contrib/cf-xarray/actions
    :alt: GitHub Workflow CI Status

.. image:: https://results.pre-commit.ci/badge/github/xarray-contrib/cf-xarray/main.svg
   :target: https://results.pre-commit.ci/latest/github/xarray-contrib/cf-xarray/main
   :alt: pre-commit.ci status

.. image:: https://codecov.io/gh/xarray-contrib/cf-xarray/branch/main/graph/badge.svg?token=hR3x9559bZ
   :target: https://codecov.io/gh/xarray-contrib/cf-xarray
   :alt: Code Coverage

.. image:: https://img.shields.io/pypi/v/cf-xarray.svg?style=for-the-badge
    :target: https://pypi.org/project/cf-xarray
    :alt: Python Package Index

.. image:: https://img.shields.io/conda/vn/conda-forge/cf_xarray.svg?style=for-the-badge
    :target: https://anaconda.org/conda-forge/cf_xarray
    :alt: Conda Version

.. image:: https://zenodo.org/badge/267381269.svg
   :target: https://zenodo.org/badge/latestdoi/267381269

.. image:: https://img.shields.io/badge/fair--software.eu-%E2%97%8F%20%20%E2%97%8F%20%20%E2%97%8F%20%20%E2%97%8F%20%20%E2%97%8B-yellow
   :target: https://fair-software.eu

cf-xarray
=========

A lightweight convenience wrapper for using CF attributes on xarray objects.

For example you can use ``.cf.mean("latitude")`` instead of ``.mean("lat")`` if appropriate attributes are set! This allows you to write code that does not require knowledge of specific dimension or coordinate names particular to a dataset.

See more in the `introductory notebook <https://cf-xarray.readthedocs.io/en/latest/examples/introduction.html>`_.

Try out our Earthcube 2021 Annual Meeting notebook `submission <https://binder.pangeo.io/v2/gh/malmans2/cf-xarray-earthcube/main?filepath=DC_01_cf-xarray.ipynb>`_.
