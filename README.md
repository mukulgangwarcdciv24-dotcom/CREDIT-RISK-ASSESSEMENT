# Credit Risk Assessment Using Ensemble Learning

## Overview

This project builds an end-to-end Credit Risk Assessment System that predicts the probability of loan default using multiple machine learning models.

Beyond binary classification, the system generates:

- Default Probability
- Risk Score (0–100)
- Risk Category (Low / Medium / High Risk)

The project combines predictive modeling with explainability through SHAP (SHapley Additive Explanations), making the results suitable for practical credit-risk analysis and lending decision support.

---

## Business Problem

Financial institutions face significant losses due to borrower defaults.

The objective of this project is to:

- Predict whether a borrower is likely to default.
- Identify key factors influencing default risk.
- Create an interpretable risk-scoring framework.
- Assist lenders in portfolio monitoring and risk-based decision making.

---

## Dataset

The dataset contains borrower-level credit information including:

- Credit Policy Status
- Loan Purpose
- Interest Rate
- Installment Amount
- Annual Income
- Debt-to-Income Ratio (DTI)
- FICO Score
- Revolving Balance
- Revolving Utilization
- Recent Credit Inquiries
- Delinquencies
- Public Records

### Target Variable

`not.fully.paid`

- 0 → Loan Repaid
- 1 → Loan Defaulted

Dataset Size:

- 9,578 observations
- 14 features

Default Rate:

- Approximately 16%

---

## Project Workflow

### 1. Data Understanding

- Dataset inspection
- Missing value analysis
- Statistical summaries
- Class distribution analysis

### 2. Data Preprocessing

- Label Encoding for categorical variables
- Feature preparation
- Train-Test Split (70/30 Stratified)

### 3. Exploratory Data Analysis

Visualizations include:

- FICO Score Distribution
- Loan Purpose Analysis
- Interest Rate vs FICO Relationship
- Correlation Heatmap

### 4. Machine Learning Models

The following models were trained and evaluated:

1. Decision Tree (Grid Search Tuned)
2. Bagging Classifier
3. AdaBoost
4. Random Forest
5. Gradient Boosting
6. XGBoost

---

## Evaluation Metrics

Models were compared using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

### Best Performing Model

**Bagging Classifier**

ROC-AUC: **0.6684**

The Bagging model achieved the highest ROC-AUC score and demonstrated the strongest discriminative performance on the test dataset.

---

## Explainability with SHAP

Although Bagging delivered the best predictive performance, XGBoost was selected for explainability analysis because of its strong integration with SHAP.

SHAP was used to:

- Understand feature impact
- Explain individual predictions
- Identify key risk drivers

Key Risk Drivers:

- Credit Policy Status
- Interest Rate
- Loan Purpose
- FICO Score
- Recent Credit Inquiries
- Revolving Balance
- Revolving Utilization

---

## Credit Risk Scoring System

The project converts predicted default probabilities into a business-friendly risk score.

### Risk Score Formula

Risk Score = Default Probability × 100

### Risk Categories

| Risk Score | Category |
|------------|----------|
| 0 – 30 | Low Risk |
| 31 – 70 | Medium Risk |
| 71 – 100 | High Risk |

This framework allows:

- Portfolio Segmentation
- Risk Monitoring
- Lending Decision Support
- Credit Policy Evaluation

---

## Results Summary

| Model | ROC-AUC |
|--------|----------|
| Bagging | 0.6684 |
| AdaBoost | 0.6604 |
| Gradient Boosting | 0.6564 |
| Random Forest | 0.6481 |
| Decision Tree | 0.6459 |
| XGBoost | 0.6282 |

Bagging achieved the best overall ROC-AUC score and was selected as the strongest predictive model.

---

## Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- XGBoost
- SHAP

---

## Business Insights

The analysis reveals that:

- Lower FICO scores are associated with higher default risk.
- Higher interest rates indicate riskier borrowers.
- Higher debt burden increases default probability.
- Frequent credit inquiries may signal financial distress.
- Income acts as a protective factor against default.

These findings align with established credit-risk principles used across the banking and lending industry.

---

## Future Improvements

Potential enhancements include:

- LightGBM implementation
- Hyperparameter optimization
- Probability calibration
- Expected Loss (EL) estimation
- Probability of Default (PD) modeling
- Portfolio-level credit risk analytics

---

## Conclusion

This project demonstrates a complete machine learning workflow for credit risk assessment, combining predictive modeling, explainability, and risk scoring.

The final solution provides both accurate default prediction and actionable business insights, making it suitable for real-world lending and risk-management applications.
