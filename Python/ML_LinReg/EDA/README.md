# Linear Regression Preprocessing Recommendation Engine (Version 2)

This project implements a structured, analysis-only preprocessing system designed to support linear regression modeling.

Instead of directly transforming or modifying the dataset, the system evaluates each feature and generates clear, evidence-based recommendations for how the data *should be prepared* in a downstream machine learning pipeline.

The focus is on transparency, interpretability, and reproducibility of preprocessing decisions.

**View the full analysis:**  
[Open LinRegPreProcess.ipynb](./LinRegEDA.ipynb)

**Static HTML version (no scrolling lag):** 
[Open LinRegPreProcess.html](https://justjbnc1.github.io/My_Portfolio/Python/ML_LinReg/EDA/LinRegEDA.html)

## What This Project Does

The pipeline performs a full feature-level and dataset-level evaluation, including:

- Missing data analysis and imputation strategy selection
- Numeric feature analysis (skew, outliers, correlation with target)
- Categorical feature analysis (cardinality, rare categories, encoding strategy)
- Imputation confidence and signal distortion risk scoring
- Unified feature risk ranking system
- Multicollinearity and redundancy detection
- Final dataset-level suitability assessment for linear regression

All results are generated as **recommendations only**, not applied transformations.

## Key Outputs

The script generates the following artifacts:

### Feature-Level Summaries
- `numeric_preprocessing_summary.csv`  
  Detailed analysis of numeric features including missingness, skew, outliers, and risk scoring.

- `categorical_preprocessing_summary.csv`  
  Analysis of categorical features including cardinality, rare categories, encoding strategy, and risk scoring.

### Unified Feature Ranking
- `feature_risk_ranking.csv`  
  A consolidated ranking of all features (numeric + categorical) based on overall risk score.

### Executive Dataset Assessment
- `executive_model_summary.txt`  
  A high-level evaluation of dataset suitability for linear regression, including:
  - Overall feature risk distribution
  - Signal strength indicators
  - Structural concerns (skew, missingness, instability)
  - Final modeling verdict:
    - SUITABLE
    - CONDITIONAL
    - NOT RECOMMENDED

## Design Philosophy

This project follows an **analysis-first preprocessing approach**, meaning:

- No data is modified silently
- Every transformation is recommended, not executed
- All decisions are explainable and traceable
- Outputs are designed to support human-driven pipeline construction

The goal is to provide a **defensible preprocessing layer** that can be used to build robust and interpretable machine learning pipelines, especially for linear regression models.

## Intended Use

This system is intended for:

- Data preprocessing strategy design
- Feature engineering planning
- Model readiness evaluation
- Educational demonstration of structured ML preprocessing
- Early-stage dataset audit before modeling
