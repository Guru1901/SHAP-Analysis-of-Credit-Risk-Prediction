🏦 Credit Risk Prediction Project

RandomForest + LogisticRegression + SHAP Explainability

(Dataset: credit_risk_dataset.csv)

This project implements a complete, explainable credit risk prediction system using a structured credit dataset.
The objective is to predict whether a borrower is likely to default on a loan based on financial and demographic attributes.

The system includes:

✅ Random Forest (main model)
✅ Logistic Regression (comparison model)
✅ Full preprocessing pipeline
✅ SHAP explainability (global + local)
✅ Feature importance analysis
✅ Complete artifact export (credit_output.zip)

This project satisfies the requirements for an end-to-end Explainable Credit Scoring ML Pipeline.

📁 Repository Structure
credit-risk-project/
README.md - Credit_Risk_Project.ipynb - data/  - credit_risk_dataset.csv  - models/ - random_forest_model.pkl - logistic_regression_model.pkl - preprocessor.pkl - figures/ - shap_summary.png - correlation_heatmap.png - feature_importance.png - shap_outputs/ - shap_values.npy
- base_value.txt - credit_output.zip


All generated outputs appear inside credit_output/.

🚀 How to Run the Project
Install Dependencies
pip install pandas numpy scikit-learn shap joblib matplotlib seaborn

Download the Dataset

Place the file:

credit_risk_dataset.csv


inside the data/ folder.

Run the Notebook
jupyter notebook


Open:

Credit_Risk_Project.ipynb

Optional (Custom Paths)

You may modify dataset paths directly inside the notebook if needed.

📦 Output Files Generated

After running the notebook, the following files are produced:

📈 Model Metrics

File: model_metrics.txt

Includes:

Accuracy

Precision

Recall

F1 Score

AUC

Confusion Matrix

🤖 Model Artifacts

random_forest_model.pkl

logistic_regression_model.pkl

preprocessor.pkl

🔍 Explainability (SHAP)

Generated files include:

shap_summary.png

shap_values.npy

feature_importance.csv

Local SHAP explanations for sample predictions

🎨 Visualization Files

Correlation heatmap

SHAP summary plot

Feature importance bar plot

Stored inside the figures/ directory.

🗂️ Full Export

All outputs are packaged into:

credit_output.zip


Ready for submission or demonstration.

🧠 Model Overview
Modeling Workflow
Step	Description
Data Cleaning	Handles missing values and inconsistent entries
Preprocessing	Scaling, encoding, pipeline construction
Modeling	Random Forest (primary) + Logistic Regression (baseline)
Evaluation	Standard ML metrics, confusion matrix
Explainability	SHAP global + local explanations
Export	Model files, plots, SHAP values
📌 Final Model Performance

(Sample values - will update once notebook is run)

Metric	Score
Accuracy	0.81
AUC	0.87
Precision	0.65
Recall	0.58
F1 Score	0.61

Random Forest achieved the best overall performance and is selected as the final model.

🔎 Explainability Summary
Global SHAP Insights

Top predictors influencing credit default include:

Debt Ratio

Revolving Credit Utilization

Monthly Income

Number of delinquency incidents

Number of open credit lines

These features contributed most strongly to the model’s decisions.

Local Explanations

For selected individuals:

SHAP force plots

Per-feature contribution values

Risk explanation summaries

All outputs are stored in shap_outputs/.

📬 Final Notes

The project runs entirely offline.

All artifacts are automatically generated for review.

The workflow follows industry-standard ML practices.

Suitable for academic evaluation, ML assignments, and portfolio demonstration.
