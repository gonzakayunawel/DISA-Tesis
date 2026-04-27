# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Doctoral thesis repository for **Gonzalo Cayunao Erices** in the PhD in Advanced Systems Engineering (DISA) at Universidad Andrés Bello (UNAB). The research models asymmetric Chilean urban logistics (integrated oligopolies vs. atomized SME last-mile operators) under external shocks, using a hierarchical three-level framework: stochastic dynamic game (oligopolistic regime switching) → Stackelberg coupling → Mean Field Game (atomized last-mile operators). The goal is a counterfactual policy simulation tool powered by Physics-Informed Neural Operators (PINO).

## Commands

**Sync environment:**
```bash
uv sync
```

**Run Python entry point:**
```bash
uv run main.py
```

**Render a Quarto document to PDF (requires XeLaTeX):**
```bash
quarto render propuesta-inicial/propuesta_doctoral.qmd --to pdf
```

## Architecture

- `main.py` — placeholder entry point; the simulation/modeling code will grow here.
- `propuesta-inicial/` — initial doctoral proposal documents:
  - `propuesta_doctoral.qmd` / `doctoral_proposal.qmd` — Quarto source (Spanish/English); these are the canonical source of truth for research goals and mathematical formulation.
  - `references.bib` — shared BibTeX bibliography.
  - `*.pdf` — rendered outputs (gitignored).
- `pyproject.toml` + `uv.lock` — dependency management via `uv`. Current dependencies: `python>=3.14`, `quarto>=0.1.0`.

## Conventions

- Research documents (`.qmd`) are written in Spanish (`lang: es`). The PDF engine is **XeLaTeX** with Latin Modern fonts (`scrartcl` document class).
- Dependency management uses **uv** exclusively — do not use pip directly.
- PDFs are gitignored; always re-render from source `.qmd` files.
- Mathematical notation in documents: $\xi$ = external shocks vector, $s$ = regime (colusivo/competitivo), $m(x,t)$ = spatial density of delivery capacity, $V_i^{(s)}$ = value function at oligopolistic level.
