Credit Risk Prediction Project

LightGBM, XGBoost, SHAP, LIME, and Fairness Assessment
(Dataset: cs-training.csv)

This project focuses on developing an explainable credit risk prediction system using the well-known “Give Me Some Credit” dataset from Kaggle. The objective is to identify customers who are likely to experience serious delinquency within the next two years. Along with building predictive models, the project also emphasizes model transparency and fairness.

The implementation includes the following components:

LightGBM as the primary classifier

XGBoost as a comparison model

SMOTE for handling class imbalance

SHAP for both global and individual-level explanations

LIME for additional local interpretability

A fairness analysis based on age groups

Automatic export of all results and artifacts into a single output folder

The solution satisfies the essential requirements of an explainable and auditable credit scoring pipeline.

Repository Structure
credit_project/
│── README.md
└── credit_project.py


All generated files are stored inside the output directory after running the script.

How to Run the Project
1. Install the Dependencies
pip install lightgbm xgboost shap lime imbalanced-learn joblib matplotlib pandas numpy scikit-learn

2. Prepare the Dataset

Download cs-training.csv and place it in the same directory as credit_project.py.

3. Run the Script
python3 credit_project.py


You can also specify custom input and output paths:

python3 credit_project.py --datafile cs-training.csv --outdir credit_output

Output Files

After the script finishes running, the output folder will contain the following resources:

Model Evaluation

metrics.txt
Contains AUC, precision, recall, F1 score, and the confusion matrix.

Saved Model Files

best_lgb.pkl

preprocessor.pkl

Explainability Resources

shap_summary.png

shap_feature_importance.csv

LIME explanation files for selected individuals

Fairness / Bias Analysis

bias_check.txt
Reports performance differences across multiple age groups.

Complete Archive

credit_output.zip

This file contains all generated artifacts packaged together for ease of submission.

Overview of the Modeling Workflow
Step	Description
Data Cleaning	Removal of ID fields, handling columns with substantial missing data
Preprocessing	Scaling and one-hot encoding
Class Balancing	Oversampling performed using SMOTE
Model Training	LightGBM tuned with RandomizedSearchCV; XGBoost used for comparison
Explainability	SHAP (global + local) and LIME for individual cases
Fairness Assessment	Evaluation of age-group bias
Final Model Performance

(Extracted from metrics.txt)

Metric	Score
AUC	0.8468
Precision	0.4750
Recall	0.2469
F1 Score	0.3249
Confusion Matrix	[[27448, 547], [1510, 495]]
Explainability Summary
Global SHAP Observations

Based on the SHAP summaries, the main drivers influencing predicted default risk are:

Revolving credit utilization

Count of 90-day late payments

Debt ratio

Monthly income

Frequency of 30–59 day delinquencies

Local Interpretations

Five individual cases (covering high-risk, low-risk, and borderline predictions) were analyzed using SHAP force plots and LIME.
These files are available in the output directory.

Fairness Assessment

A fairness check was carried out across four age brackets:

30 and below

31–45

46–60

Above 60

The resulting bias_check.txt file highlights differences in predicted default rates and provides a brief interpretation.

Notes

The project runs locally and does not require Google Colab.

The script follows a clean, modular structure for clarity and maintainability.

All key deliverables (models, figures, metrics, SHAP/LIME outputs, and fairness results) are automatically saved.

Suitable for academic coursework, explainable AI demonstrations, and practical credit risk modeling applications.
