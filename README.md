# Survey Results Analysis (Stack Overflow Developer Survey)

Exploratory Data Analysis (EDA) and simple modeling on the **Stack Overflow Developer Survey** dataset, focused mainly on **annual compensation** (`ConvertedCompYearly`) and how it relates to factors like **country, education, and experience**.

This repository contains a Jupyter Notebook: `Survey_results_analysis.ipynb`.

---

## What’s inside

The notebook includes:

- **Dataset overview** (shape, column types, basic statistics)
- **Missing values** analysis
- **Outlier handling** (filters salaries to `< 300,000 USD` to reduce distortion)
- **Salary distribution** plots (histogram / boxplots)
- **Salary comparisons**:
  - by **country** (e.g., top countries by participation + salary comparisons)
  - by **education level**
  - by **developer role** (`DevType`)
  - by **remote work type** (`RemoteWork`)
- **Feature engineering**
  - salary categories (low / medium / high)
  - `IsHighIncome` flag (salary > 100,000 USD)
  - education encoded to numeric (`EduLevelNumeric`)
  - experience parsing (e.g., converting `YearsCode` text to numeric)
  - optional age conversion to numeric (`AgeNumeric`)
- **Correlation heatmap** for numeric features
- **Baseline classification model**
  - Logistic Regression to predict `IsHighIncome` using:
    - `YearsCode`
    - `EduLevelNumeric`
  - Evaluation via confusion matrix + classification report

---

## Data

The notebook expects the Stack Overflow survey file:

- `survey_results_public.csv`

Place it in the **project root** (same folder as the notebook), or update the path inside the notebook.

You can download the dataset from the official Stack Overflow Developer Survey page (choose the year you want and ensure the column names match the notebook).

---

## Requirements

- Python 3.9+ (recommended)
- Jupyter Notebook / JupyterLab

Python libraries used:
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
