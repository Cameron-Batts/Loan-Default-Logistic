# Loan Default Prediction via Logistic Regression

## Project Overview
This project explores loan default prediction using logistic regression in R. The analysis focuses on identifying financial and demographic factors associated with borrower default risk and evaluating model performance using classification metrics.

The project includes:
- exploratory data analysis (EDA)
- feature evaluation
- missing value handling
- logistic regression modeling
- cutoff threshold analysis
- confusion matrix evaluation

---

## Project Objectives
- Analyze borrower characteristics and loan performance
- Identify variables associated with loan default risk
- Build and evaluate logistic regression classification models
- Compare model performance across multiple cutoff thresholds
- Understand tradeoffs between accuracy, sensitivity, and specificity

---

## Tools & Technologies
- R
- tidyverse
- ggplot2
- caret
- gmodels
- e1071
- Logistic Regression

---

## Repository Structure

```text
Loan_Default_Logistic/
│
├── Data/
├── Images/
├── Notebooks/
├── Reports/
└── README.md
```

---

## Key Variables Analyzed
- Loan Amount
- Interest Rate
- Credit Grade
- Employment Years
- Home Ownership Status
- Annual Income
- Borrower Age
- Loan Default Indicator

---

## Exploratory Data Analysis

The analysis examined relationships between:
- income and age
- employment and income
- employment and age
- credit grade and default frequency

Visualizations highlighted:
- strong separation in default rates across credit grades
- concentration of defaults among lower credit ratings
- skewed distributions in income and delay-related variables
- several extreme outliers in income and age

---

## Data Preparation
Steps performed during preprocessing included:
- removal of major outliers
- handling missing values
- creation of missing-value indicator variables
- train/test data split
- feature evaluation for model inclusion

---

## Modeling Approach

Three logistic regression models were evaluated:
1. Full logistic regression model
2. Top 5 predictor model
3. Reduced top 3 predictor model

The strongest predictors included:
- credit grade
- interest rate
- annual income

---

## Model Evaluation

Model performance was evaluated using:
- confusion matrices
- accuracy
- sensitivity
- specificity
- balanced accuracy
- AIC comparison

The project also explored how adjusting classification cutoffs impacted:
- false positives
- false negatives
- default detection performance

---

## Key Findings
- Credit grade was one of the strongest predictors of default risk
- Higher interest rates were associated with increased default probability
- Higher annual income reduced default likelihood
- Accuracy alone was misleading because of class imbalance
- Lowering classification cutoffs improved detection of high-risk loans

---

## Supporting Files
This repository includes:
- R notebooks
- exploratory visualizations
- statistical outputs
- regression summaries
- classification performance evaluations

---

## Author
Cameron Batts

GitHub: https://github.com/Cameron-Batts
Portfolio: https://cameronbatts.github.io
