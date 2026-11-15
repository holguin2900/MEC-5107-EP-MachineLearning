# MEC 5107 EP – Machine Learning

Course notebooks and project work for **MEC 5107 EP – Machine Learning** (École polytechnique).

The tutorials apply machine-learning methods to energy and climate data, such as electricity demand, wind capacity factors and ERA5 reanalysis fields. The course project asks: *"Could the 2026 super El Niño have been predicted?"*

---

## Repository structure

```
.
├── tutorials/
│   ├── 01_tutorial_introduction.ipynb
│   ├── 02_tutorial_supervised_learning_problem_ols.ipynb
│   ├── 04_tutorial_overfitting_underfitting_bias_variance.ipynb
│   ├── 05_tutorial_regularization_selection_evaluation.ipynb
│   ├── 06_tutorial_classification_generative.ipynb
│   ├── 07_tutorial_classification_discriminative.ipynb
│   ├── 08_tutorial_unsupervised_learning_pca.ipynb
│   ├── 09_tutorial_ensemble_methods_demand_prediction.ipynb
│   ├── 09_tutorial_ensemble_methods_windcf_prediction.ipynb
│   └── 10_tutorial_neural_networks.ipynb
├── project/
│   └── project_super_elnino.ipynb
├── ml4climate/          # helper package used by the notebooks
├── data/                # datasets (not tracked, see below)
├── requirements.txt
└── README.md
```

## Tutorials

| # | Notebook | Topics |
|---|----------|--------|
| 01 | Introduction | Python basics: NumPy, pandas, Matplotlib, first steps with scikit-learn |
| 02 | Supervised learning & OLS | Supervised learning problem, ordinary least squares |
| 04 | Overfitting / underfitting | Bias–variance trade-off, model complexity |
| 05 | Regularization, selection & evaluation | Ridge / Lasso, cross-validation, model selection |
| 06 | Generative classification | Generative classifiers |
| 07 | Discriminative classification | Discriminative classifiers |
| 08 | Unsupervised learning | Principal Component Analysis (PCA) |
| 09 | Ensemble methods | Demand and wind capacity factor prediction with ensemble methods |
| 10 | Neural networks | Multilayer perceptrons with scikit-learn |

## Course project: *Could the 2026 super El Niño have been predicted?*

The project uses ERA5 data averaged over the **Niño 3.4 box** to build and evaluate statistical forecasts of the 2026 El Niño event.

Ground rules we follow:
- **No future information:** predictors use only data available on the forecast issue date.
- **Strict temporal split:** models are trained only on data from before the test period.
- Methods are limited to those covered in the course tutorials.

**Deadlines:** notebook due 13 December 2026, presentation on 14 December 2026.

## Getting started

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install -r requirements.txt
jupyter lab
```

Main dependencies (`requirements.txt`):

```
numpy
pandas
xarray
netCDF4
matplotlib
scikit-learn
jupyterlab
```

### Data

Datasets (CSV and NetCDF files) are **not tracked** in this repository because of their size. Place them in the `data/` folder, which the notebooks read through `data_dir = Path('data')`.

Suggested `.gitignore` entries:

```
data/
*.nc
.ipynb_checkpoints/
__pycache__/
```

## Credits & license

The tutorial notebooks were created by **Bruno Deremble** and **Alexis Tantet** for the [E4C Interdisciplinary Center – Education](https://gitlab.in2p3.fr/energy4climate/public/education) (LMD, IPSL, École polytechnique, Sorbonne Université, ENS, CNRS).

The original material is licensed under [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0/). Any modified versions in this repository are shared under the same license.

## Authors

- David Holguín Gómez
- *(add team members)*
