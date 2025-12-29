---
repo: hackalog/data_folklore
url: 'https://github.com/hackalog/data_folklore'
homepage: null
starredAt: '2022-07-27T21:14:00Z'
createdAt: '2018-10-19T21:47:35Z'
updatedAt: '2022-07-27T21:14:00Z'
language: Python
license: MIT
branch: master
stars: 1
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:19.785Z'
description: >-
  There's "Data Science," and then there's Data Folklore. This is a repo for the
  latter.
tags: []
---

data_folklore
==============================

There's "Data Science," and then there's Data Folklore. This is a repo for the latter.

GETTING STARTED
---------------

* Create and switch to the  virtual environment:
```
cd data_folklore
make create_environment
conda activate data_folklore
make requirements
```
* Explore the notebooks in the `notebooks` directory

Project Organization
------------
* `LICENSE`
* `Makefile`
    * top-level makefile. Type `make` for a list of valid commands
* `README.md`
    * this file
* `data`
    * Data directory. often symlinked to a filesystem with lots of space
    * `data/raw`
        * Raw (immutable) hash-verified downloads
    * `data/interim`
        * Extracted and interim data representations
    * `data/processed`
        * The final, canonical data sets for modeling.
* `docs`
    * A default Sphinx project; see sphinx-doc.org for details
* `models`
    * Trained and serialized models, model predictions, or model summaries
    * `models/trained`
        * Trained models
    * `models/output`
        * predictions and transformations from the trained models
* `notebooks`
    *  Jupyter notebooks. Naming convention is a number (for ordering),
    the creator's initials, and a short `-` delimited description,
    e.g. `1.0-jqp-initial-data-exploration`.
* `references`
    * Data dictionaries, manuals, and all other explanatory materials.
* `reports`
    * Generated analysis as HTML, PDF, LaTeX, etc.
    * `reports/figures`
        * Generated graphics and figures to be used in reporting
    * `reports/tables`
        * Generated data tables to be used in reporting
    * `reports/summary`
        * Generated summary information to be used in reporting
* `requirements.txt`
    * (if using pip+virtualenv) The requirements file for reproducing the
    analysis environment, e.g. generated with `pip freeze > requirements.txt`
* `environment.yml`
    * (if using conda) The YAML file for reproducing the analysis environment
* `setup.py`
    * Turns contents of `folklore` into a
    pip-installable python module  (`pip install -e .`) so it can be
    imported in python code
* `folklore`
    * Source code for use in this project.
    * `folklore/__init__.py`
        * Makes folklore a Python module
    * `folklore/data`
        * Scripts to fetch or generate data. In particular:
        * `folklore/data/make_dataset.py`
            * Run with `python -m folklore.data.make_dataset fetch`
            or  `python -m folklore.data.make_dataset process`
    * `folklore/analysis`
        * Scripts to turn datasets into output products
    * `folklore/models`
        * Scripts to train models and then use trained models to make predictions.
        e.g. `predict_model.py`, `train_model.py`
* `tox.ini`
    * tox file with settings for running tox; see tox.testrun.org


--------

<p><small>This project was built using <a target="_blank" href="https://github.com/hackalog/cookiecutter-easydata">cookiecutter-easydata</a>, an experimental fork of [cookiecutter-data-science](https://github.com/drivendata/cookiecutter-data-science) aimed at making your data science workflow reproducible.</small></p>
