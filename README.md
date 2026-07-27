# Statistical Mechanics Notebooks

A collection of Python notebooks exploring concepts in statistical mechanics —
ensembles, partition functions, phase transitions, Monte Carlo methods, and
related topics.

## Setup

This project uses [uv](https://docs.astral.sh/uv/) for environment and
dependency management.

```bash
uv sync
uv run jupyter lab
```

## Structure

- `notebooks/` — numbered notebooks, roughly in reading order
- `src/statmech/` — shared helper code (samplers, plotting utilities, lattice
  classes, etc.) imported by the notebooks, so logic used in more than one
  place lives in one location instead of being copy-pasted

## Notes on git + notebooks

This repo uses [`nbstripout`](https://github.com/kynan/nbstripout) to strip
cell outputs before committing, so diffs stay readable. After cloning, run:

```bash
uv run nbstripout --install
```

Your local notebooks still show outputs when you run them — only the
committed version is stripped.