# Elevvo Machine Learning Internship

Machine learning tasks completed for the required **Elevvo Pathways Machine Learning Engineer Internship** (1-month track).
Each task is a self-contained Jupyter notebook with data cleaning, visualization, modeling, evaluation, bonus experiments and written conclusions. Every task folder has its own README with the task requirements, a requirements checklist, the results and the conclusion.

| # | Task | Level | Techniques | Key result |
|---|------|-------|-----------|-----------|
| 2 | [Customer Segmentation](Task%202%20-%20Customer%20Segmentation) | 1 | Scaling, K-Means, elbow & silhouette, DBSCAN | **5 customer segments** (silhouette 0.555) |
| 3 | [Forest Cover Type Classification](Task%203%20-%20Forest%20Cover%20Type%20Classification) | 2 | Random Forest, XGBoost, hyperparameter tuning | **XGBoost 92.8% accuracy** (7 classes) |
| 6 | [Music Genre Classification](Task%206%20-%20Music%20Genre%20Classification) | 3 | MFCC audio features, SVM, Random Forest, MLP, song-level split | **77.5% song accuracy** (10 genres) |
| 7 | [Sales Forecasting](Task%207%20-%20Sales%20Forecasting) | 3 | Lag & rolling features, seasonal decomposition, time-series CV | Random Forest: **3.9% WMAPE** on the last 20 weeks |

## Highlights

- **Task 2:** two groups earn the same high income but spend very differently, so income alone doesn't predict spending.
- **Task 3:** XGBoost beats a tuned Random Forest; soil type, elevation and wilderness area drive the predictions.
- **Task 6:** splitting by song avoids data leakage (a random clip split would report a misleading 91%); voting over a song's clips lifts accuracy from 70.8% to 77.5%.
- **Task 7:** last year's sales for the same week plus the recent 4-week average drive the forecast; the models beat naive baselines, and the holiday season is the hardest period to predict.

## Datasets

| Task | Dataset | In this repo |
|------|---------|--------------|
| 2 | [Mall Customer Segmentation](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) (Kaggle) | yes |
| 3 | [Covertype](https://archive.ics.uci.edu/dataset/31/covertype) (UCI) | no, downloaded automatically by `sklearn.datasets.fetch_covtype` |
| 6 | [GTZAN](https://www.kaggle.com/datasets/andradaolteanu/gtzan-dataset-music-genre-classification) (Kaggle), pre-extracted feature CSVs | yes (audio files not included) |
| 7 | [Walmart Sales Forecast](https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast) (Kaggle) | yes |

## How to run

```bash
pip install -r requirements.txt
jupyter notebook
```

Open any task folder and run the notebook from top to bottom; each notebook reads its dataset from its own folder.
In Google Colab, upload the notebook together with its CSV files and run `!pip install rich` first.

## Tools

Python · pandas · NumPy · Matplotlib · scikit-learn · XGBoost · statsmodels · rich

## Author

**John Daniel L. Ubungen**
Machine Learning Engineer Intern · Elevvo Pathways

GitHub: [@JD-Code05](https://github.com/JD-Code05)
