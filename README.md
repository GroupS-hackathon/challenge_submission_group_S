# COVID Vaccine Prediction — Group S
### Research Methods in Data Science | University of Hertfordshire
### Data Science Challenge Hackathon

---

## Overview

This repository contains the full work produced by **Group S** during the Data Science Challenge Hackathon. The goal was to build a machine learning pipeline to predict COVID-19 vaccine uptake from a survey dataset, submitted as part of the group project assessment.

Core modelling and EDA was completed during the hackathon session on **5th June 2026**. Explainable AI (SHAP analysis) and figure polishing were completed afterwards as permitted by the assignment brief.

---

## Contributors

| Name | GitHub |
|------|--------|
| Akhila Thurpati | [@Akhila152003](https://github.com/Akhila152003) |
| Bhavin Thakur | [@bhavinthakur29](https://github.com/bhavinthakur29) |
| Jyothi Kallubhavi | [@Kallubhavijyothi](https://github.com/Kallubhavijyothi) |
| Sriharshini Thatiparthi | [@sriharshini1603-sketch](https://github.com/sriharshini1603-sketch) |
| Upender Madha | [@upender8096](https://github.com/upender8096) |
| Venkat Bhargav Inkollu | [@InkolluvenkatBhargav](https://github.com/InkolluvenkatBhargav) |

---

## Repository Structure

```
├── challenge_submission_group_S.ipynb   # Main notebook (all code)
├── dataset_C_testing.csv                # Testing dataset
├── dataset_C_training.csv               # Training dataset
├── plots/                               # All saved visualisation outputs
│   ├── target_distribution.png
│   ├── target_balance.png
│   ├── missing_values.png
│   ├── correlation_heatmap.png
│   ├── top_correlations.png
│   ├── behaviour_vs_vaccination.png
│   ├── pca_projection.png
│   ├── best_model_performance.png
│   ├── permutation_importance.png
│   ├── model_comparison.png
│   ├── decision_threshold.png
│   ├── shap_bar.png
│   ├── shap_waterfall.png
│   └── learning_curve.png
├── submission_csv/                      # All CSV predictions for evaluation
│   ├── challenge_submission_group_S_order_1.csv
│   ├── challenge_submission_group_S_order_2.csv
│   ├── challenge_submission_group_S_order_3.csv
│   ├── challenge_submission_group_S_order_4.csv
│   ├── challenge_submission_group_S_order_5.csv
│   └── FINAL_Group_S_Submission.csv
└── README.md
```

---

## Dataset

> **Dataset:** Hackathon Dataset C (`dataset_C_training.csv`, `dataset_C_testing.csv`)  
> Source: Hackathon Dataset C Information.pdf

The dataset contains **31 columns** — a unique respondent ID, 29 survey-based features covering behavioural habits, medical conditions, opinions on COVID risk and vaccine effectiveness, and demographic information, with `covid_vaccine` as the binary target variable.

---

## Notebook Structure

| Section | Description |
|---------|-------------|
| 1 | Imports & constants |
| 2 | Load data |
| 3 | Exploratory Data Analysis (EDA) |
| 4 | Preprocessing & Feature Engineering |
| 5 | Cross-Validation setup (StratifiedKFold) |
| 6 | ML Models — Logistic Regression, KNN, Random Forest, Neural Network, Gradient Boosting |
| 7 | Performance Metrics — confusion matrix, ROC curve, precision-recall curve |
| 8 | Explainable AI — Permutation Importance |
| 9 | Hyperparameter Tuning — GridSearchCV |
| 9.1 | Model Comparison — all 6 models across F1, ROC-AUC, Accuracy |
| 10 | Decision-Threshold Optimisation |
| 11 | XAI — SHAP Horizontal Bar Chart *(completed post-hackathon)* |
| 12 | XAI — SHAP Waterfall Plot *(completed post-hackathon)* |
| 13 | Learning Curve (Bias/Variance analysis) |
| 14 | Final Submissions — ranked by F1 score |
| 15 | Critical Analysis |

---

## Models Trained

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Random Forest
- Neural Network (MLP)
- Gradient Boosting (HistGradientBoosting)
- Tuned Gradient Boosting (GridSearchCV optimised)

---

## Key Results

| Model | ROC-AUC | Accuracy | F1 |
|-------|---------|----------|----|
| GradientBoosting | 0.8566 | 0.8130 | 0.6927 |
| TunedGradientBoosting | 0.8560 | 0.8110 | 0.6890 |
| LogisticRegression | 0.8340 | 0.7940 | 0.6450 |
| NeuralNetwork | 0.8200 | 0.7840 | 0.6330 |
| RandomForest | 0.8340 | 0.7840 | 0.6160 |
| KNN | 0.8060 | 0.7730 | 0.5680 |

> All scores are 5-fold stratified cross-validation results on the training set.  
> Submissions are ordered by F1 score as per evaluation criteria.

---

## Dependencies

All standard packages are pre-installed in Google Colab. The notebook auto-installs any missing packages on first run:

```
numpy, pandas, matplotlib, scikit-learn
lightgbm
shap
```

---

## How to Run

1. Clone this repository
2. Open `challenge_submission_group_S.ipynb` in Google Colab or Jupyter
3. Run all cells top to bottom
4. Predictions will be saved to `submission_csv/` and plots to `plots/`

---

## Collaboration

All code was developed collaboratively using a shared **Google Colab notebook** linked to this **GitHub organisation repository**. Commit history and Colab activity logs serve as evidence of individual contributions during the hackathon.

---

*University of Hertfordshire — Research Methods in Data Science — June 2026*
