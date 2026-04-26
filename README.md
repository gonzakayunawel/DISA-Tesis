# Asymmetric Urban Logistics in Chile under External Shocks

This repository contains the code and documentation for the doctoral research project: **"Asymmetric Chilean Urban Logistics under External Shocks: A Quantitative Approach for Evidence-Based Public Policy."**

Developed as part of the **PhD in Advanced Systems Engineering (DISA)** at Universidad Andrés Bello (UNAB).

## Project Overview

The Chilean e-commerce logistics market is characterized by a structural asymmetry: a few integrated oligopolistic operators control the majority of volume, while a fragmented network of small and medium-sized (SME) last-mile operators handles final delivery. This project aims to model how regulatory and price shocks (e.g., fuel prices, labor laws, emission standards) are transmitted through this hierarchical structure.

### Research Goals
- **Transmission Modeling:** Quantify the transmission of shocks from the oligopolistic level to last-mile operators.
- **Strategic Behavior:** Model regime switching (collusive vs. competitive) within the logistics oligopoly.
- **Policy Simulation:** Develop a simulation tool for counterfactual policy evaluation using Scientific Machine Learning (SciML).

## Technical Stack

- **Language:** Python 3.14+ (managed via [uv](https://github.com/astral-sh/uv))
- **Documentation:** [Quarto](https://quarto.org/) for technical reports and thesis drafting.
- **Scientific Computing:**
  - **PyTorch/CUDA:** High-performance numerical modeling.
  - **SciML:** Physics-Informed Neural Operators (PINO) for approximating complex system dynamics.
  - **LaTeX/XeLaTeX:** Professional academic document rendering.

## Project Structure

```text
├── propuesta-inicial/   # Doctoral proposal documents (QMD, BIB)
├── main.py              # Main project entry point
├── pyproject.toml       # Python dependencies and metadata
├── uv.lock              # Deterministic dependency lockfile
└── GEMINI.md            # Agent-specific context for developers
```

## Getting Started

### Prerequisites

Ensure you have `uv` installed. If not, you can install it via:
```bash
curl -LsSf https://astral-sh/uv/install.sh | sh
```

### Installation

Clone the repository and sync the environment:
```bash
git clone https://github.com/gonzakayunawel/disa-tesis.git
cd disa-tesis
uv sync
```

### Usage

**Render the Doctoral Proposal:**
To generate the PDF version of the research proposal:
```bash
quarto render propuesta-inicial/idea_doctoral.qmd --to pdf
```

**Run Python Scripts:**
```bash
uv run main.py
```

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## Author

**Gonzalo Cayunao Eruces**  
PhD Researcher at DISA, Universidad Andrés Bello.  
Facultad de Ingeniería, UNAB.
