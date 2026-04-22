# Feature Preprocessing Recommendation Engine

This project implements a structured, analysis-only preprocessing system for tabular machine learning datasets.

Rather than modifying data directly, the system evaluates each feature and produces explicit, evidence-based recommendations for how it should be handled in a downstream modeling pipeline. The design prioritizes transparency, reproducibility, and interpretable decision-making.

The framework is especially useful for early-stage dataset auditing and feature engineering design.

**View the full analysis:**  [Open LinRegPreProcess.ipynb](./LinRegEDA.ipynb)

**Static HTML version (no scrolling lag):** [Open LinRegPreProcess.html](https://justjbnc1.github.io/My_Portfolio/Python/ML_LinReg/EDA/LinRegEDA.html)

**View Output File:** [Open preprocessing_output4.xlsx](https://justjbnc1.github.io/My_Portfolio/Python/ML_LinReg/EDA/preprocessing_output4.xlsx)

## What This Project Does

This pipeline performs a comprehensive feature-level evaluation across both numeric and categorical variables.

It includes:

- Missing data analysis and imputation strategy selection  
- Numeric feature evaluation (distribution behavior, skew, correlation with target)  
- Categorical feature evaluation (cardinality, rare categories, encoding strategy)  
- Imputation confidence and signal distortion risk scoring  
- Unified feature risk scoring system  
- Composite feature value scoring (predictive value vs. risk)  
- Rule-based action labeling (KEEP, TRANSFORM, DROP, REVIEW)  
- Final ranked feature prioritization for modeling decisions  

All outputs are **recommendations only** and no transformations are applied directly to the dataset.

## Key Outputs

The script generates structured outputs to support feature selection and preprocessing design.

### Feature-Level Summaries

- **numeric_preprocessing_summary.csv** *(or dataframe equivalent)*  
  Evaluation of numeric features including missingness, correlation with target, skew, imputation method, and risk scoring.

- **categorical_preprocessing_summary.csv** *(or dataframe equivalent)*  
  Evaluation of categorical features including cardinality, rare value structure, encoding strategy, and risk scoring.

### Unified Feature Ranking

- **feature_risk_ranking.csv**  
  Combined ranking of all features (numeric + categorical) based on composite score, balancing predictive value and risk.

### Exported Report

- **preprocessing_output.xlsx**  
  Multi-sheet export containing:
  - Numeric feature summary  
  - Categorical feature summary  
  - Unified feature ranking  

## Design Philosophy

This project follows an **analysis-first preprocessing paradigm**, meaning:

- No transformations are applied directly to the dataset  
- Every preprocessing decision is explicitly scored and justified  
- Outputs are structured as recommendations rather than actions  
- Feature behavior is quantified before any modeling decisions are made  
- All outputs are designed to be auditable and reproducible  

This approach ensures preprocessing is **transparent, defensible, and interpretable**, rather than implicit or automated.

## Intended Use Cases

This system is designed for:

- Feature engineering planning  
- Dataset quality auditing  
- Pre-modeling exploratory analysis  
- Preprocessing strategy design  
- Educational demonstrations of structured ML pipelines  
- Building interpretable linear or generalized regression pipelines  
