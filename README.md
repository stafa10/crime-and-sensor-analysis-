# Data Analysis & Machine Learning Projects (Python)

Two Python/Jupyter projects: a machine learning model comparison, and a public data analysis dashboard.

## 1. Sensor State Classification (`sensor_analysis.ipynb`)

Cleans a 16-feature sensor dataset (`Data8076.csv`) and compares 5 classification
models to predict whether a sensor is ON or OFF:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Naive Bayes
- Random Forest
- Gradient Boosting

Models are trained on an 80/20 train/test split and compared by accuracy, with a
confusion matrix used to check whether the best-scoring model is actually learning
a real pattern rather than just guessing the majority class.

## 2. Irish Crime Statistics Dashboard (`crime_stats_analysis.ipynb`)

Downloads and explores 20+ years of official recorded crime data (2003–2025) from
the Central Statistics Office's public API (CSO PxStat table `CJQ06`), sourced from
An Garda Síochána's PULSE system:

- National totals by year
- Top offence categories overall
- Totals by Garda Division (all 28 divisions/counties)
- Year-by-year trend for a chosen offence category
- Interactive dropdown to look up any single county's raw data

## Setup

```
python -m venv .venv
.venv\Scripts\pip install pandas numpy matplotlib scikit-learn joblib ipykernel ipywidgets
```

Open either notebook in Jupyter/VS Code, select the `.venv` kernel, and run all cells.

`garda_recorded_crime.csv` is downloaded directly from the CSO API:
`https://ws.cso.ie/public/api.restful/PxStat.Data.Cube_API.ReadDataset/CJQ06/CSV/1.0/en`
