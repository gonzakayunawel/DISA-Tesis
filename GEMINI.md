# Project Overview: DISA Tesis - Asymmetric Urban Logistics in Chile

This project is a hybrid research and software repository for the doctoral thesis of **Gonzalo Cayunao Eruces** in the **Doctorado en Ingeniería de Sistemas Avanzados (DISA)** at Universidad Andrés Bello (UNAB).

The core research focuses on modeling **asymmetric urban logistics** in the Chilean market (oligopolies vs. atomized last-mile operators) under external shocks (e.g., fuel prices, regulatory changes). It aims to provide a quantitative framework for evidence-based public policy using Scientific Machine Learning (SciML) and game theory.

## Main Technologies
- **Python >= 3.14**: Development of numerical models and simulations.
- **Quarto**: Document authoring and conversion (QMD to PDF/LaTeX).
- **uv**: Project management and dependency resolution.
- **Scientific Stack**: 
    - **PyTorch/CUDA**: High-performance computing and neural operators.
    - **Scientific Machine Learning (SciML)**: Physics-Informed Neural Operators (PINO).
    - **LaTeX**: High-quality document rendering (via XeLaTeX).

## Project Structure
- `main.py`: Main Python entry point (currently a placeholder).
- `propuesta-inicial/`: Initial doctoral proposal documents.
    - `idea_doctoral.qmd`: Quarto source for the research proposal.
    - `references.bib`: BibTeX bibliography file.
- `pyproject.toml` & `uv.lock`: Dependency management and project metadata.

## Building and Running

### Document Generation
To render the research proposal to PDF:
```bash
quarto render propuesta-inicial/idea_doctoral.qmd --to pdf
```

### Python Development
To run the main script using the managed environment:
```bash
uv run main.py
```
To synchronize the development environment:
```bash
uv sync
```

## Development Conventions
- **Language**: Research documents (`.qmd`) are primarily written in Spanish (`lang: es`).
- **Research Methodology**: Follows the PRISMA protocol for bibliometric audits and hierarchical modeling (Oligopolistic switching regimes -> Stackelberg coupling -> Mean Field interaction).
- **Modeling**: Prioritizes numerical approximation via PINO to allow for real-time counterfactual policy evaluation.

## Key Files
- `propuesta-inicial/idea_doctoral.qmd`: The primary source of truth for research goals and mathematical formulation.
- `pyproject.toml`: Defines the project's Python dependencies and tool configurations.
