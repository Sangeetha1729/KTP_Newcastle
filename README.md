# Household Electricity Demand Forecasting
### OUB KTP Pre-Interview Technical Assessment

## Overview

This repository contains the code and report for a pre-interview technical assessment examining household electricity demand forecasting using smart meter data and residential survey characteristics.

The analysis investigates whether household survey variables improve forecasts of daily electricity consumption beyond temporal information alone, using data from 100 Irish households collected between July 2009 and December 2010.

## Repository Contents

| File | Description |
|------|-------------|
| `KTP_Newcastle.ipynb` | Annotated Jupyter notebook containing all data preprocessing, exploratory data analysis, and modelling code |
| `requirements.txt` | Python package dependencies |
| `eda_patterns.png` | EDA visualisations: consumption distribution, half-hourly load profile, and seasonal variation |
| `feature_importance.png` | Feature importance plot from the survey-enhanced Random Forest model |

## Key Findings

- Household survey characteristics substantially improve forecasting performance, reducing MAE by 44% and RMSE by 33% relative to a temporal-only baseline model
- Number of bedrooms, household occupancy, and appliance ownership were the strongest predictors of daily electricity demand
- Temporal features alone (month, day of week, season) explained only 3.6% of variance (R² = 0.036), confirming that between-household differences dominate consumption variation

## Requirements

pandas==2.3.0

numpy==2.2.5

matplotlib==3.10.1

scikit-learn==1.7.0

Install dependencies with:
```bash
pip install -r requirements.txt
```

## Dataset

The datasets used in this analysis are not included in this repository. The analysis was conducted on data provided as part of the technical assessment and cannot be redistributed. To reproduce the analysis, the following files are required in the same directory as the notebook:

- `separated_all_100.csv` — half-hourly electricity consumption time series for 100 households
- `survey_all_100.csv` — household survey responses
- `RESIDENTIAL SURVEY.doc` — survey questionnaire and variable descriptions

## Note on AI Assistance

AI tools were used to assist with code review, debugging, and editing, including linguistic suggestions for the written commentary. The analytical approach, interpretation, and conclusions are my own.
