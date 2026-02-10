# Survey Results Analysis (Stack Overflow Developer Survey)

Exploratory analysis of the **Stack Overflow Developer Survey** dataset, with a focus on **annual compensation** (`ConvertedCompYearly`) and how it relates to factors like **country, education, and experience**.

Repository contents:
- `Survey_results_analysis.ipynb`

---

## Overview

The notebook covers:

- Dataset overview (shape, column types, summary stats)
- Missing values inspection
- Outlier handling (filters salaries to `< 300,000 USD` to reduce distortion)
- Salary distribution visualizations (histogram / boxplots)
- Salary comparisons by:
  - Country
  - Education level
  - Developer role (`DevType`)
  - Remote work type (`RemoteWork`)
- Feature engineering:
  - Salary categories (low / medium / high)
  - `IsHighIncome` indicator (salary > 100,000 USD)
  - Education encoded to numeric (`EduLevelNumeric`)
  - Experience parsing (converting `YearsCode` to numeric)
  - Optional age conversion (`AgeNumeric`)
- Correlation heatmap for numeric features
- Baseline classification model:
  - Logistic Regression predicting `IsHighIncome` using:
    - `YearsCode`
    - `EduLevelNumeric`
  - Evaluation with confusion matrix + classification report

---

## Libraries used

- **pandas**
- **numpy**
- **matplotlib**
- **seaborn**
- **scikit-learn**

---

## Data

The notebook uses the Stack Overflow survey file:
- `survey_results_public.csv`

Make sure the dataset year/columns match what the notebook expects (especially `ConvertedCompYearly`, `YearsCode`, `EdLevel`, etc.).

---

## Notes

- Compensation values are filtered to reduce the influence of extreme outliers on plots/correlations.
- Several survey fields are stored as text ranges; the notebook converts key fields (e.g., experience and age) into numeric values when needed.
- Many columns contain missing values; analyses focus on rows where relevant data exists.
