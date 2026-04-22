# Efficient Attention Classification: A Lightweight XGBoost Approach to Facial Feature Extraction in E-Learning

This repository contains the LaTeX manuscript source for the research paper presented at the **15th Scientific Day of ITC** (Institute of Technology of Cambodia).

## Paper Overview

The COVID-19 pandemic shifted education online, but existing automated engagement detection systems rely on heavy deep-learning pipelines requiring GPU resources most schools cannot afford. This study introduces a lightweight, interpretable alternative:

- **Dataset:** [DAiSEE](https://ieeexplore.ieee.org/document/7780951) — a large-scale benchmark for affective-state recognition in e-learning
- **Features:** 78-dimensional vectors extracted via MediaPipe (blendshapes, head pose, eye gaze, composite expression features, facial dynamics)
- **Model:** XGBoost classifier (CPU-only, no GPU required)
- **Task:** Four affective states (boredom, engagement, confusion, frustration) at three ordinal levels (Low, Medium, High)
- **Key Results:** 65.26% mean accuracy, 59.62% weighted F1-score, with frustration detection reaching 80.25%

## Repository Structure

```
.
├── src/
│   ├── index.tex              # Main manuscript content (two-column body)
│   ├── _preamble.tex          # Document setup, packages, fonts, formatting
│   ├── _postamble.tex         # Document closure
│   ├── reference.bib          # Bibliography entries
│   ├── image/                 # Figures and plots
│   │   ├── training_curve.png
│   │   └── model-architecture.pdf
│   ├── Logo/                  # Institutional logos (ITC, RIC, etc.)
│   └── Fonts/                 # Khmer fonts (KhmerOSsiemreap, KhmerOSmuol)
├── Tectonic.toml              # Tectonic build configuration
├── build/                     # Build output directory (generated)
└── main.pdf                   # Compiled PDF output (generated)
```

## Build Requirements

- [Tectonic](https://tectonic-typesetting.github.io/) — A modern, self-contained TeX/LaTeX engine based on XeTeX

### Installing Tectonic

```bash
# macOS (Homebrew)
brew install tectonic

# Linux (cargo)
cargo install tectonic

# Or download a pre-built binary from:
# https://github.com/tectonic-typesetting/tectonic/releases
```

## Building the Manuscript

From the repository root, run:

```bash
# Build the PDF using Tectonic
# Option 1: Using the Tectonic.toml config

# Option 2: Direct compilation
tectonic -X compile src/_preamble.tex --outfmt pdf

# Or compile the full document
tectonic src/index.tex
```

The compiled PDF will be output to `build/manuscript/manuscript.pdf` (when using `tectonic -X build`) or `main.pdf`.

## Key Features of the Manuscript

- **Conference format:** Two-column layout with custom header for ITC Scientific Day
- **Multilingual support:** English with Khmer text support via XeLaTeX and custom Khmer fonts
- **Rich visualizations:** Model architecture diagrams, training curves, and result tables
- **Interpretability analysis:** SHAP values and permutation importance for feature analysis
- **Comprehensive evaluation:** Per-class precision, recall, F1-scores, and confusion matrices

## Citation

If you use this work, please cite:

```bibtex
@inproceedings{moul2025efficient,
  title={Efficient Attention Classification: A Lightweight XGBoost Approach to Facial Feature Extraction in E-Learning},
  author={Moul, Hengborann and Has, Sothea and Phauk, Sokkhey},
  booktitle={The 15th Scientific Day of ITC},
  year={2025},
  organization={Institute of Technology of Cambodia}
}
```

## Authors

- **Hengborann Moul** (Corresponding Author) — Graduate School, Institute of Technology of Cambodia  
  📧 hengborann_moul@gsc.itc.edu.kh
- **Dr. Sothea Has** — Department of Applied Mathematics and Statistics, Institute of Technology of Cambodia
- **Dr. Sokkhey Phauk** — Department of Applied Mathematics and Statistics, Institute of Technology of Cambodia

## License

This manuscript and its associated materials are provided for academic and research purposes. Please contact the corresponding author for reuse or distribution inquiries.

## Acknowledgments

This research was conducted at the **Institute of Technology of Cambodia (ITC)** and presented at the **15th Scientific Day of ITC** with the theme *"Bridging Engineering and Technology with Industry for Cambodia's Sustainable Growth."*

The work contributes toward **UN Sustainable Development Goal 4 (Quality Education)** by providing educators with a practical, explainable attention detection tool for data-driven teaching in resource-constrained online learning environments.
