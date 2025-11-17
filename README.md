Credit Risk Prediction System

Machine Learning Model with Random Forest, Logistic Regression, and SHAP Explainability

Overview

This project develops a credit risk prediction system that classifies customers based on the likelihood of loan default. The solution includes data preprocessing, model training, evaluation, and explainability components. The objective is to provide a transparent and reliable scoring mechanism that supports data-driven credit decisioning.

The project includes:

Random Forest (primary model)

Logistic Regression (benchmark model)

Scikit-Learn preprocessing pipeline

Model evaluation using classification metrics

SHAP-based global and local interpretation

Export of trained models, plots, and reports

The system is designed as a complete, reproducible machine learning workflow.

Repository Structure
credit-risk-project/
│── README.md
│── requirements.txt
│── notebooks/
│     └── Credit_Risk_Project.ipynb
│── data/
│     └── credit_risk_dataset.csv
│── models/
│     ├── random_forest_model.pkl
│     ├── logistic_regression_model.pkl
│── figures/
│     ├── correlation_heatmap.png
│     ├── feature_importance.png
│     ├── shap_summary.png
│── shap_outputs/
│     ├── shap_values.npy
│     ├── base_value.txt
│── report/
│     ├── Credit_Risk_Report.pdf
│     └── Credit_Risk_Report.docx
└── credit_output.zip

Installation

Install required packages:

pip install -r requirements.txt


Or install manually:

pip install pandas numpy scikit-learn shap joblib matplotlib seaborn

Dataset

The project uses credit_risk_dataset.csv, which should be placed in:

data/credit_risk_dataset.csv


The dataset contains demographic attributes, financial variables, and historical delinquency indicators.

Running the Project

Launch Jupyter Notebook:

jupyter notebook


Open and execute:

notebooks/Credit_Risk_Project.ipynb


Running the notebook generates the following:

Processed dataset

Trained models

Evaluation metrics

SHAP-based explainability outputs

Figures and visual summaries

Output archive (credit_output.zip)

Outputs
Model Artifacts

random_forest_model.pkl

logistic_regression_model.pkl

preprocessor.pkl

Evaluation Metrics

Metrics include accuracy, AUC, precision, recall, F1-score, and confusion matrix, saved in:

model_metrics.txt

Explainability Outputs

SHAP summary plot

Feature importance ranking

Local instance-level explanations

SHAP values and base values

All explainability files are stored in:

shap_outputs/

Visualization Assets

Correlation heatmap

SHAP summary plot

Model feature importance

Stored in:

figures/

Export Package

A consolidated archive containing all results is generated as:

credit_output.zip

Workflow Summary

Data loading and validation

Preprocessing (scaling, encoding, missing value handling)

Model training (RandomForestClassifier, LogisticRegression)

Performance evaluation

Interpretation using SHAP

Exporting trained models and artifacts

Model Performance (Example)
Metric	Score
Accuracy	0.81
AUC	0.87
Precision	0.65
Recall	0.58
F1 Score	0.61

The Random Forest model delivered the strongest overall performance and is selected as the final model.

Explainability Summary

SHAP analysis highlights the key factors influencing model decisions. The most influential predictors include:

Debt Ratio

Revolving Credit Utilization

Monthly Income

Counts of prior delinquency

Number of open credit lines

Both global and local interpretations are provided to support model transparency and regulatory compliance.

Notes

This project is fully offline and self-contained.

All required assets for evaluation, grading, and portfolio demonstration are included.

The implementation follows standard machine learning development practices suitable for production-level modeling.
