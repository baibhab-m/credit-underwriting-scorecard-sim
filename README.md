# Credit Underwriting Scorecard & Strategy Simulator

Maps to: Credit Risk intern role — review of AI/ML decision models and underwriting strategies, ad-hoc quantitative modeling.

## Dataset
Home Credit Default Risk (Kaggle) — primary. Optional fallback: Give Me Some Credit (Kaggle) or German Credit (UCI).

## Scope
- **WoE/IV binning** + **logistic regression scorecard** and a gradient boosting challenger (XGBoost/LightGBM).
- Compare using **AUC, KS, Gini**, and a **decile lift table**.
- **Model-risk-style review**: PSI (population stability) between train and out-of-time sample, **feature importance** with SHAP, calibration, and a **fairness/bias check** across age or gender.
- **Strategy simulator** (Streamlit): slide the score cut-off → approval rate, bad rate, expected loss; champion/challenger comparison.

## Structure
```
data/raw/              # application_train.csv, application_test.csv (gitignored)
notebooks/             # 01_binning_woe_iv.ipynb, 02_scorecard_logreg.ipynb, 03_xgb_challenger.ipynb, 04_model_review_psi_shap.ipynb, 05_fairness_check.ipynb
app/                   # streamlit_app.py  — cut-off slider, champion/challenger view
models/                # scorecard.pkl, xgb_challenger.pkl
reports/               # champion_challenger_comparison.csv, psi_report.csv, fairness_report.csv
docs/                  # model_review_memo.md
README.md              # this file
```

## Status
Scaffold only — content coming overnight. See commits for progress.

## Resume bullet
> Credit Scorecard and Underwriting Strategy Simulator | GitHub, Python | 2025
> Developed WoE logistic scorecard and XGBoost challenger on Home Credit data (AUC/KS/Gini, PSI, SHAP validation); built cut-off simulator showing approval rate vs. expected loss trade-offs for champion/challenger strategies.