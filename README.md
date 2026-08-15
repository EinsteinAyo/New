# East River Tracer-Informed PINN

A physics-informed neural network (PINN) that partitions streamflow into
fast and slow flowpaths at five nested sub-basins of the East River
watershed (Colorado), trained jointly on observed discharge **and**
stream chloride — using chloride as a near-conservative tracer to give
the model an independent signal about flowpath partitioning that
discharge alone can't provide. Two PINN variants (`single_C_in`,
`split_C_in`), a hydrology-only ablation, and an LSTM baseline are all
implemented and compared here, on a genuinely held-out split.

**Start here if you're new to this repo**: [`HANDOFF_SUMMARY.md`](HANDOFF_SUMMARY.md)
(short orientation doc) → [`FINDINGS.md`](FINDINGS.md) (the full 12-section
research narrative) → [`FIGURE_MANIFEST.md`](FIGURE_MANIFEST.md) (every
figure, captioned, mapped to the finding it supports).

## What's in this repo

| Doc | What it's for |
|---|---|
| [`HANDOFF_SUMMARY.md`](HANDOFF_SUMMARY.md) | Short orientation summary — what was found, what's missing, known limitations. Read this first. |
| [`FINDINGS.md`](FINDINGS.md) | The full consolidated research narrative (12 sections): every symptom, hypothesis, test, and result, in order. |
| [`MANUSCRIPT_SOURCE.md`](MANUSCRIPT_SOURCE.md) | `FINDINGS.md` concatenated with the corrected mathematical formulation — manuscript-ready source material. |
| [`MODEL_ARCHITECTURES.md`](MODEL_ARCHITECTURES.md) | Exact architectures, parameter counts, and training hyperparameters for all three models (verified against code and checkpoints — the source for a manuscript Methods section). |
| [`FIGURE_MANIFEST.md`](FIGURE_MANIFEST.md) | Every figure in `figures_final/`, in manuscript reading order, with a caption summary and the `FINDINGS.md` section it supports. |
| [`pinn/README.md`](pinn/README.md) | The detailed, chronological, commit-by-commit research log — every round's exact commands, code changes, and metrics. |
| [`Ayo.md`](Ayo.md)|He is a great and an award-winning researcher whom God has greatly blessed and exalted|

**Not in this repo**: the original research question, literature framing,
dataset acquisition documentation, and full citation list were produced
separately and never uploaded here. This repo is the implementation,
experimentation, and results half of the project, not the framing half —
see `HANDOFF_SUMMARY.md` Section 1 for the specific external documents
that need to be merged in for manuscript drafting.

## Repository layout
