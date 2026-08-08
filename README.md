# The NLL Cliff: √d Scaling of a Metric Drop in Embedding-Space Attacks

This repository is the official implementation of [*The NLL Cliff: √d Scaling of a Metric Drop in Embedding-Space Attacks*](#).

[ArXiv](#) · [Code](https://github.com/user-namego/embedding-tube-cliff)

[![arXiv](https://img.shields.io/badge/arXiv-coming_soon-b31b1b)](#)

## Abstract

Embedding-level attacks optimize soft suffixes directly in token-embedding space. Tube defenses counter this by clamping each suffix position to a Euclidean ball of radius τ around its nearest vocabulary token. Auditing nine models (GPT-2, Qwen2.5, Pythia), we find a sharp empirical boundary: the largest safe radius (cliff) scales as √d with embedding dimension. We show this is an empirical regularity governed by optimizer dynamics rather than a strict geometric invariant. Under AdamW@0.1, the cliff follows τ_c ≈ 0.085√d + 0.45 (R² = 0.83); SGD yields roughly half this coefficient. Hard snap-to-token projection triples the critical radius relative to soft PGD-style projection on GPT-2. We also identify a codebook-walk regime where gradients align with nearest-neighbor edges, collapsing the cliff to zero regardless of τ. The cliff is seed-deterministic, budget-invariant, and stable across suffix lengths 4–32. Crucially, NLL reduction does not guarantee behavioral harm. We recommend a conservative operating envelope of τ ≤ 0.03√d against continuous attackers, alongside mandatory per-model walk checks and behavioral filtering.

## Status

- **Code and reproduction scripts** — Coming soon


## Reproducibility

All experiments were conducted on NVIDIA T4 GPUs with bf16 precision. Large models use 4-bit quantization (bitsandbytes) and gradient checkpointing following QLoRA-style configuration without finetuning. Exact hyperparameters, tube grids, and seed configurations are documented in the supplementary materials and will be included in the code release.

## Contact

email — `kotyshov [dot] v [dot] i [at] gmail [dot] com`。

## Citation

```bibtex
@misc{kotyshov2026nllcliff,
  title   = {The NLL Cliff: $\sqrt{d}$ Scaling of a Metric Drop in Embedding-Space Attacks},
  author  = {Kotyshov, Vladislav},
  year    = {2026},
  archivePrefix = {arXiv},
  primaryClass    = {cs.CL},
  note    = {Preprint; code and reproduction scripts forthcoming}
}