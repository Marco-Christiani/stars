---
repo: oneoffcoder/py-pair
url: 'https://github.com/oneoffcoder/py-pair'
homepage: 'https://py-pair.readthedocs.io/'
starredAt: '2022-05-20T00:23:30Z'
createdAt: '2020-11-11T20:26:51Z'
updatedAt: '2024-09-26T08:37:28Z'
language: Python
license: Apache-2.0
branch: main
stars: 21
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:35:29.732Z'
description: Pairwise association measures of statistical variable types
tags:
  - apache-spark
  - association
  - asymmetric
  - binary-variable
  - biserial
  - categorical-variable
  - causation
  - concordance
  - confusion-matrix
  - contingency-table
  - continuous-variable
  - correlation
  - interval-variable
  - nominal-variable
  - ordinal-variable
  - ranking
  - ratio-variable
  - symmetric
---

![pypair logo](https://py-pair.readthedocs.io/_images/logo.png)

# PyPair

PyPair is a statistical library to compute pairwise association between any two variables. In general, statistical variable types are viewed as `categorical` or `continuous`. Categorical variables have no inherit order to their values, while continuous variables do. This API has `over 130 association measures` implemented for any combination of categorical and/or continuous variables. 

To install.

```bash
pip install pypair
```

Additional links.

- [Documentation](https://py-pair.readthedocs.io/)
- [PyPi](https://pypi.org/project/pypair/) 
- [Gitter](https://gitter.im/dataflava/py-pair)

Here's a short and sweet snippet for using the API against a dataframe that stores strictly binary data. The Pandas `DataFrame.corr()` method no longer processes non-numeric fields!

```python
from pypair.association import binary_binary
from pypair.util import corr

jaccard = lambda a, b: binary_binary(a, b, measure='jaccard')
tanimoto = lambda a, b: binary_binary(a, b, measure='tanimoto_i')

df = get_a_pandas_binary_dataframe()

jaccard_corr = corr(df, jaccard)
tanimoto_corr = corr(df, tanimoto)

print(jaccard_corr)
print('-' * 15)
print(tanimoto_corr)
```

Another way to get started with PyPair is to use the `convenience` methods whose names indicate the variable pair types.

```python
from pypair.association import binary_binary, categorical_categorical, \
    binary_continuous, concordance, categorical_continuous, continuous_continuous, confusion, agreement

# assume a and b are the appropriate iterables of values for 2 variables
jaccard = binary_binary(a, b, measure='jaccard')
acc = confusion(a, b, measure='acc')
phi = categorical_categorical(a, b, measure='phi')
kappa = agreement(a, b, measure='cohen_k')
biserial = binary_continuous(a, b, measure='biserial')
tau = concordance(a, b, measure='kendall_tau')
eta = categorical_continuous(a, b, measure='eta')
pearson = continuous_continuous(a, b, measure='pearson')
```

# Software Copyright

```
Copyright 2020 One-Off Coder

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

# Book Copyright

Copyright 2020 One-Off Coder

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/) by [One-Off Coder](https://www.oneoffcoder.com).

![Creative Commons Attribution 4.0 International License](https://i.creativecommons.org/l/by/4.0/88x31.png "Creative Commons Attribution 4.0 International License")

# Art Copyright

Copyright 2020 Daytchia Vang

# Citation

```
@misc{oneoffcoder_pypair_2020,
title={PyPair, A Statistical API for Bivariate Association Measures},
url={https://github.com/oneoffcoder/py-pair},
author={Jee Vang},
year={2020},
month={Nov}}
```

# Sponsor, Love

- [Patreon](https://www.patreon.com/vangj)
- [GitHub](https://github.com/sponsors/vangj)
