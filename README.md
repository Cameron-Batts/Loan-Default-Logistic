# Loan Default Prediction via Logistic Regression

![Loan Default Visualization](./Images/Grid.png)

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

# Project Objectives
- Analyze borrower characteristics and loan performance
- Identify variables associated with loan default risk
- Build and evaluate logistic regression classification models
- Compare model performance across multiple cutoff thresholds
- Understand tradeoffs between accuracy, sensitivity, and specificity

---

# Tools & Technologies
- R
- tidyverse
- ggplot2
- caret
- gmodels
- e1071
- Logistic Regression

---

# Repository Structure

```text
Loan_Default_Logistic/
│
├── Data/
│   └── LoanData.rds
│
├── Images/
│   └── Grid.png
│
├── Notebooks/
│
├── Reports/
│   └── Loan Default Prediction via Logistic Regression.pdf
│
└── README.md
```

---

# Key Variables Analyzed
- Loan Amount
- Interest Rate
- Credit Grade
- Employment Years
- Home Ownership Status
- Annual Income
- Borrower Age
- Loan Default Indicator

---

# Exploratory Data Analysis

The analysis examined relationships between:
- income and age
- employment and income
- employment and age
- credit grade and default frequency

Visualizations highlighted:
- separation in default behavior across borrower groups
- concentration of defaults among higher-risk profiles
- skewed distributions in income-related variables
- potential outliers impacting model performance

---

# Data Preparation

Steps performed during preprocessing included:
- removal of major outliers
- handling missing values
- creation of missing-value indicator variables
- train/test data split
- feature evaluation for model inclusion

---

# Modeling Approach

Three logistic regression models were evaluated:
1. Full logistic regression model
2. Reduced predictor model
3. Simplified classification model

Key predictive variables included:
- credit grade
- interest rate
- annual income
- employment years

The project also evaluated how probability cutoff thresholds impacted model classification performance. :contentReference[oaicite:0]{index=0}

---

# Model Evaluation

Model performance was evaluated using:
- confusion matrices
- accuracy
- sensitivity
- specificity
- balanced accuracy
- AIC comparison

The project explored the tradeoff between:
- maximizing accuracy
- improving default detection
- reducing false negatives
- maintaining balanced model performance

---

# Key Findings
- Credit grade was one of the strongest predictors of default risk.
- Higher interest rates were associated with increased default probability.
- Higher annual income generally reduced default likelihood.
- Accuracy alone was misleading because of class imbalance in the dataset.
- Lower classification thresholds improved the detection of high-risk loans.
- The Top 5 predictor logistic regression model produced the best AIC performance. :contentReference[oaicite:1]{index=1}

---

# Supporting Files

This repository includes:
- R notebooks
- exploratory visualizations
- regression outputs
- model evaluation summaries
- classification performance analysis

---

# Skills Demonstrated
- Logistic regression
- Classification modeling
- Exploratory data analysis
- Statistical analysis
- Data preprocessing
- Model evaluation
- R programming
- Data visualization
- Predictive analytics

---

# Data

This project uses loan performance and borrower characteristic data stored in RDS format.

The dataset includes:
- borrower financial information
- loan characteristics
- employment history
- credit grade classifications
- loan default outcomes

The data was used to build and evaluate predictive logistic regression classification models.

---

# Author

Cameron Batts

GitHub: https://github.com/Cameron-Batts

Portfolio: https://cameron-batts.github.io

