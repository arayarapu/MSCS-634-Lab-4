# MSCS-634 Lab 4 — Regression Analysis with Regularization Techniques

This repository contains a reproducible Jupyter Notebook 

## Files

- `MSCS634_Lab4_Regression_Regularization.ipynb` — the entire lab, with code, charts, metrics, and discussion.
- `screenshots/` — generated PNG plots (created when the notebook runs).
- `model_comparison.csv` — metrics exported when the notebook runs.
- `requirements.txt` — Python dependencies.

## Run on a Mac (Terminal)

```bash
cd ~/Downloads/MSCS634_Lab4
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m notebook
```

Open `MSCS634_Lab4_Regression_Regularization.ipynb` in the browser, update the student name, then use **Kernel > Restart Kernel and Run All Cells**.

The dataset is loaded from `sklearn.datasets.load_diabetes` and does not require a CSV or internet connection.

## Models and metrics

- Simple Linear Regression — one feature chosen using training correlation
- Multiple Linear Regression — 10 features
- Polynomial Regression — degrees 2 and 3, plus a one-feature complexity experiment
- Ridge Regression — degree-2 polynomial inputs and 5-fold CV alpha tuning
- Lasso Regression — degree-2 polynomial inputs and 5-fold CV alpha tuning

Each main model is evaluated using **MAE, MSE, RMSE, and R²** on training and test data; the notebook compares generalization gaps. All tuning occurs on the training split.