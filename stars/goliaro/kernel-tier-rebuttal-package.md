---
repo: goliaro/kernel-tier-rebuttal-package
url: 'https://github.com/goliaro/kernel-tier-rebuttal-package'
homepage: null
starredAt: '2026-11-19T07:47:11Z'
createdAt: '2026-11-13T22:28:57Z'
updatedAt: '2026-11-19T07:47:11Z'
language: Python
license: NA
branch: main
stars: 1
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-11-22T02:19:12.080Z'
description: null
tags: []
---

# FastKernels rebuttal: kernel-tier experiments

Needs: 8x B200 and the FastKernels Python env with fastkernels installed from branch
`kernel-tier-compile` (in your checkout: `git checkout kernel-tier-compile && git pull && pip install -e .`).
Candidates are JIT-compiled with `$CUDA_HOME/bin/nvcc`: use the CUDA toolkit matching torch's
(`python -c 'import torch; print(torch.version.cuda)'`); some candidates do not build with an older nvcc.

```bash
export OUT=$PWD/results               # optional; default: results/ in this folder
bash 0_reproduce.sh                   # paper reproduction (eager, 5 shapes)
bash 1_shapes.sh                      # Exp 1: 10 / 25 shapes
bash 2_compile.sh                     # Exp 2: compile + CUDA graphs
# Exp 3 runs on the e2e runtime: in your checkout, git checkout paper-e2e && pip install -e .
bash 3_quality.sh                     # Exp 3: downstream quality (GSM8K, COCO AP, CLIPScore)
tar czf results.tgz results/          # send this back
```

Run in tmux. Each script can be rerun to resume. If a run killed mid-build later hangs with no output,
delete the stale `lock` files under `*/candidates/.torch_extensions/` and `~/.cache/torch_extensions/`.
Please run `0_reproduce.sh` first and send its
results before starting the others, so we can check the setup.

## Contents

- `drkernel/`, `claude/`, `kda/`, `ako/`, `codex/`: candidate sources. `candidates/independent` = all
  candidates (benched `--standalone`); `composed` = independent winners together; `sequential` =
  sequential winners.
- `captures/b200/`: the captured shapes the paper used, downloaded by the scripts on first run from
  `sfc-gh-goliaro/fastkernels-results` (pinned commit; needs read access to that repo).
- `deployment_failures.csv`: kernels dropped during end-to-end deployment (set, model, kernel, reason).
- `quality_runs.txt`, `quality.py`: Exp 3 runs (exact deployed kernel subsets) and their evaluators.
- `original_{kernel,case,level}_results.csv`: the paper's kernel-tier results.
- `manifest.json`, `checksums.json`: provenance and known original-source issues.
