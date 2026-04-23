
# Python Feature Engineering & Preprocessing Decision Engine (Linear Regression Focus)
<img width="250" height="250" alt="regression" src="https://github.com/user-attachments/assets/35bf0bbf-59bd-431d-a55b-13d171d058fd" />

## Overview

This project implements a **structured feature engineering and preprocessing decision engine** designed to evaluate dataset quality before model training. It analyzes both numeric and categorical features and produces:

- Feature-level risk assessments  
- Predictive signal estimates  
- Encoding and imputation recommendations  
- A composite ranking of feature usefulness  
- An automated action label (KEEP / TRANSFORM / DROP / REVIEW)  
- A full Excel report with multiple analytical views  

The system is currently demonstrated using the **Ames Housing dataset (House Prices)** from `sklearn.datasets.fetch_openml`.

**View the full analysis:**  [LinRegPreProcess.ipynb](./LinRegEDA.ipynb)

**Static HTML version (no scrolling lag):** [LinRegPreProcess.html](https://justjbnc1.github.io/My_Portfolio/Python/ML_LinReg/EDA/LinRegEDA.html)

**View Output File:** [preprocessing_output4.xlsx](https://justjbnc1.github.io/My_Portfolio/Python/ML_LinReg/EDA/preprocessing_output4.xlsx)

---

## Business Problem

In real-world machine learning workflows, especially for regression problems, model performance is often degraded not by the algorithm itself, but by:

- Poor handling of missing data  
- Inappropriate encoding of categorical variables  
- Hidden data quality issues (skew, sparsity, outliers)  
- Over-reliance on raw correlations without structural understanding  
- Lack of interpretable feature selection logic  

### Core Issue

Traditional workflows typically answer:

> “Can we train a model on this dataset?”

But they fail to answer:

> “Which features are actually safe, stable, and worth modeling—and which will degrade performance or introduce noise?”

---

## Solution

This project introduces a **pre-modeling diagnostic system** that evaluates features before any model training occurs.

It transforms raw features into structured intelligence through:

### 1. Feature Risk Modeling
Each feature is assigned a **FeatureRiskScore** based on:

- Missing value proportion  
- Imputation method complexity  
- Encoding strategy (categorical features)  
- Signal distortion risk  
- Relationship strength with target  

### 2. Predictive Signal Estimation
- Numeric: Pearson correlation with target  
- Categorical: proxy correlation via factorized encoding  

This estimates how much predictive value a feature contributes.

### 3. Composite Score (Signal vs Risk Balance)

:contentReference[oaicite:0]{index=0}

Where:
- |r| = absolute correlation (or proxy correlation)
- Rₙ = normalized FeatureRiskScore

This provides a single interpretable measure of:

> “Is this feature more useful than it is risky?”

### 4. Automated Feature Action System

Each feature is assigned a decision label:

- **KEEP** → strong signal, low risk  
- **TRANSFORM** → useful but unstable (needs preprocessing refinement)  
- **DROP** → low value, high risk  
- **REVIEW** → ambiguous or borderline cases  

### 5. Categorical Intelligence Layer

For categorical variables, the system evaluates:

- Encoding strategy suitability (one-hot, binary, target encoding)  
- Category sparsity (RareRatio)  
- Encoding-induced distortion risk (SignalRisk)  

## Output Structure

The script generates a single Excel file:

### 📄 Sheets included:

- **Numeric Summary**
- **Categorical Summary**
- **Feature Ranking**

Each feature includes:
- Risk score
- Composite score
- Action label
- Supporting diagnostic metrics

---

## Why This Project Matters

This system addresses a key gap in ML workflows:

> Feature engineering is usually reactive and manual. This system makes it **systematic, explainable, and automated.**

It helps:

- Data scientists prioritize feature work
- Reduce noise before model training
- Improve model stability and interpretability
- Standardize preprocessing decisions across datasets

---

## Ideal Use Cases

- Early-stage machine learning exploration  
- Feature selection for regression models  
- Dataset quality audits  
- Educational understanding of preprocessing impact  
- Model readiness assessment before training  

---

## Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- OpenPyXL (Excel export)
