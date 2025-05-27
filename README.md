# 🧬 Equitable Diabetes Diagnosis: Tackling Ethnic and Gender Disparities

This repository contains the source code, processed data, and additional figures used in the scientific paper submitted to SBBD 2025. The focus is on **assessing and mitigating bias in diabetes diagnosis prediction models**, with particular attention to the sensitive attributes **ethnicity** and **gender**.

## 📝 Overview

Machine Learning (ML) has been widely adopted in disease diagnosis but may unintentionally reproduce social inequalities by embedding biases related to sensitive attributes. This project evaluates the performance and fairness of a Logistic Regression model trained on data from the 2015 BRFSS (Behavioral Risk Factor Surveillance System). Two bias mitigation techniques are applied: **Reweighting** (pre-processing) and **Prejudice Remover** (in-processing), targeting ethnic disparities in type 2 diabetes diagnosis.

## 📊 Dataset

- **Source**: [BRFSS 2015 - CDC](https://www.cdc.gov/brfss/)
- **Instances after cleaning**: 251,467
- **Selected attributes**: 24 (including BMI, high blood pressure, cholesterol, physical activity, income, education, ethnicity, gender, etc.)
- **Protected attributes evaluated**: `Ethnicity` (White vs. Non-White) and `Gender` (Male vs. Female)
- **Target**: Binary classification — 1 = Diabetes or Prediabetes, 0 = No diabetes or only during pregnancy

## ⚙️ Techniques

- **Model**: Logistic Regression with 5-fold cross-validation and 70-30 hold-out split
- **Performance metrics**: Accuracy, Precision, Recall, F1-score, AUC-ROC
- **Fairness metrics**:
  - Statistical Parity Difference (SPD)
  - Equal Opportunity Difference (EOD)
  - Average Odds Difference (AOD)
- **Bias mitigation**:
  - `Reweighting` (pre-processing)
  - `Prejudice Remover` (in-processing)



