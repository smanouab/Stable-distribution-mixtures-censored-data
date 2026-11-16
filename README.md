# Mélanges de lois α-stables en présence de données censurées

**A detailed R Markdown notebook for parameter estimation in mixtures of α-stable distributions with censored data.**

**Authors:** Solym Mawaki MANOU-ABI and Ibrahim SADOK

---

## Overview

This repository provides a detailed and reproducible computational framework for the estimation of finite mixtures of α-stable distributions in the presence of censored observations.

It accompanies the research article:

*Parameter Estimation for Mixtures of α-Stable Distributions in the Presence of Censored Data.*

The notebook presents the statistical methodology, computational algorithms, simulation studies, and real-data applications developed in the paper. Particular attention is given to parameter estimation under censoring, the numerical implementation of the proposed procedures, and the assessment of their statistical performance.

The repository is designed to facilitate the understanding, reproduction, and extension of the numerical experiments presented in the article.

## Repository structure

```text
melanges-lois-alpha-stables-donnees-censurees/
│
├── README.md
├── main.Rmd
│
├── R/
│   ├── 00_functions.R
│   ├── 01_simulation.R
│   └── 02_applications.R
│
├── data/
│   └── ...
│
├── figures/
│   └── ...
│
├── tables/
│   └── ...
│
└── renv/
    └── ...
```

### Main components

| File | Description |
|---|---|
| `main.Rmd` | Detailed R Markdown notebook |
| `R/00_functions.R` | Statistical estimators, algorithms, and computational utilities |
| `R/01_simulation.R` | Monte Carlo simulation studies (A, B, and C) |
| `R/02_applications.R` | Real-data applications: Mayotte serial interval and enzyme data |
| `data/` | Data required for the applications |
| `figures/` | Generated graphical outputs |
| `tables/` | Generated tables, including LaTeX outputs |

## Methodology

The notebook is organized into several complementary sections:

1. Definition and simulation of α-stable distributions.
2. Finite mixtures of α-stable distributions.
3. Statistical formulation of the censoring mechanism.
4. Construction and implementation of parameter estimators.
5. Numerical optimization and estimation algorithms.
6. Diagnostic and validation procedures.
7. Monte Carlo simulation studies.
8. Applications to real datasets.

Each methodological component is accompanied by implementation details and numerical validation examples.

## Computational experiments

Two execution modes are available through the YAML parameters of the notebook.

| Mode | Description |
|---|---|
| `rapide` | Reduced number of Monte Carlo replications for testing and debugging |
| `complet` | Full simulation settings corresponding to the research article |

The execution mode can be specified in the YAML header:

```yaml
params:
  mode: "rapide"
  run_simulation: true
  run_applications: true
```

To run the complete experiments, use:

```yaml
params:
  mode: "complet"
  run_simulation: true
  run_applications: true
```

The complete mode may require several hours depending on the computational resources available.

## Requirements

The notebook requires:

- R (version 4.2 or later recommended).
- RStudio (recommended).
- R Markdown and knitr.
- The R packages required by the statistical procedures and numerical experiments.

Install the main notebook dependencies using:

```r
install.packages(c(
  "rmarkdown",
  "knitr",
  "ggplot2",
  "dplyr",
  "tidyr",
  "dplyr"
))
```

Additional dependencies may be required by the functions and applications.

## Running the notebook

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/melanges-lois-alpha-stables-donnees-censurees.git
```

Open the project in RStudio and install the required packages.

Run the notebook:

```r
rmarkdown::render("main.Rmd")
```

**Important:** The notebook should be executed from the root directory of the article, which contains `main.tex`, when used alongside the article's LaTeX source files. This ensures that generated figures and tables are saved in the expected locations.

## Reproducibility

The computational framework is designed to support reproducible research.

The notebook includes:

- Explicit parameter settings for numerical experiments.
- Validation tests for the main computational functions.
- Configurable simulation settings.
- Automatic generation of figures and tables.
- A clear separation between statistical methods, simulations, and applications.

For reproducibility, users are encouraged to record their R version, package versions, random seeds, and computational environment.

## Authors

**Solym Mawaki MANOU-ABI**  
Laboratoire de Mathématiques et Applications (UMR CNRS 7348)  
École  d'Ingénieurs ENSAR, Université de Poitiers, France

**Ibrahim SADOK**

## Citation

If you use this code or the associated computational framework in your research, please cite the corresponding research article:

```bibtex
@article{manouabi_sadok_alpha_stable_mixtures,
  title  = {Parameter Estimation for Mixtures of Alpha-Stable
            Distributions in the Presence of Censored Data},
  author = {Manou-Abi, Solym Mawaki and Sadok, Ibrahim},
  year   = {Preprint 2026}
}
```

Please replace `YEAR` with the publication year and update the bibliographic information once the article is published.

## License

The licensing terms will be specified upon release of the repository.

---

**Keywords:** α-stable distributions; finite mixture models; censored data; parameter estimation; heavy-tailed distributions; Monte Carlo simulations; statistical inference; reproducible research.
