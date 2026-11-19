# Elevvo Machine Learning Internship

Four machine learning tasks completed for the **Elevvo Pathways ML Internship** (1-month track).
Each task is a self-contained Jupyter notebook with data cleaning, visualization, modeling, evaluation, bonus experiments and written conclusions. Outputs use a terminal-style design (boxed tables via `rich`, dark monospace charts).

| # | Task | Level | Techniques | Key result |
|---|------|-------|-----------|-----------|
| 1 | [Student Score Prediction](Task%201%20-%20Student%20Score%20Prediction/Task1_Student_Score_Prediction.ipynb) | 1 | Linear & polynomial regression, feature selection | Study hours alone: R² 0.247 · all features: **R² 0.825** |
| 2 | [Customer Segmentation](Task%202%20-%20Customer%20Segmentation/Task2_Customer_Segmentation.ipynb) | 1 | Scaling, K-Means, elbow & silhouette, DBSCAN | **5 customer segments** (silhouette 0.555) |
| 3 | [Forest Cover Type Classification](Task%203%20-%20Forest%20Cover%20Type%20Classification/Task3_Forest_Cover_Type.ipynb) | 2 | Random Forest, XGBoost, hyperparameter tuning | **XGBoost 92.8% accuracy** (7 classes) |
| 4 | [Loan Approval Prediction](Task%204%20-%20Loan%20Approval%20Prediction/Task4_Loan_Approval_Prediction.ipynb) | 2 | Imputation, one-hot encoding, SMOTE, class weights | Decision tree + SMOTE: **F1 0.964** on rejected loans |

## Highlights

- **Task 1:** attendance predicts exam scores better than study hours; polynomial terms add nothing because the relationship is linear.
- **Task 2:** two groups earn the same high income but spend very differently, so income alone doesn't predict spending.
- **Task 3:** XGBoost beats a tuned Random Forest; soil type, elevation and wilderness area drive the predictions.
- **Task 4:** the credit score (CIBIL) accounts for 86% of the decision; class weights and SMOTE raise recall on rejected loans.

## Datasets

| Task | Dataset | In this repo |
|------|---------|--------------|
| 1 | [Student Performance Factors](https://www.kaggle.com/datasets/lainguyn123/student-performance-factors) (Kaggle) | yes |
| 2 | [Mall Customer Segmentation](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) (Kaggle) | yes |
| 3 | [Covertype](https://archive.ics.uci.edu/dataset/31/covertype) (UCI) | no, downloaded automatically by `sklearn.datasets.fetch_covtype` |
| 4 | [Loan Approval Prediction](https://www.kaggle.com/datasets/architsharma01/loan-approval-prediction-dataset) (Kaggle) | yes |

## How to run

```bash
pip install -r requirements.txt
jupyter notebook
```

Open any task folder and run the notebook from top to bottom; each notebook reads its dataset from its own folder.
In Google Colab, upload the notebook together with its CSV file and run `!pip install rich imbalanced-learn` first.

## Tools

Python · pandas · NumPy · Matplotlib · scikit-learn · XGBoost · imbalanced-learn · rich
