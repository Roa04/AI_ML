# Week 4 — BinX Tech AI & ML Internship

**Dataset:** Telco Customer Churn  
**Task:** Binary Classification — will a customer leave? (Churn: Yes/No)

---

## 📂 File Structure


Week4/
├── day1/
│   ├── day1.ipynb
│   ├── README.md
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── day2/
│   ├── day2.ipynb
│   ├── README.md
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── day3/
│   ├── day3.ipynb
│   ├── README.md
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
├── day4/
│   ├── day4.ipynb
│   ├── README.md
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
└── day5/
    ├── day5.ipynb
    ├── README.md
    └── WA_Fn-UseC_-Telco-Customer-Churn.csv


---

## 🎯 Week Objective
Progressively build reliable churn prediction models by:
1. Establishing honest evaluation splits.  
2. Using cross‑validation for robust performance estimates.  
3. Diagnosing bias‑variance trade‑offs.  
4. Engineering features and tuning hyperparameters.  
5. Building leak‑free pipelines for end‑to‑end workflows.

---

## 📘 Day‑by‑Day Highlights

- **Day 1 — Train/Validation/Test Splits**  
  - Introduced 60/20/20 split to prevent leakage.  
  - Tuned Random Forest `n_estimators` using validation set.  
  - Final test accuracy ≈ 80%, ROC AUC ≈ 0.84.  

- **Day 2 — Cross‑Validation**  
  - Replaced single split with Stratified 5‑Fold CV.  
  - Mean churn F1 ≈ 0.54 ± 0.025 vs. Day 1’s optimistic 0.57.  
  - Stratification preserved class balance across folds.  

- **Day 3 — Bias‑Variance & Diagnosing Model Fit**  
  - Compared underfit (depth 1), overfit (unlimited), and tuned trees.  
  - Depth 5 gave best balance: Train F1 = 0.601, Val F1 = 0.582, Gap = 0.019.  
  - Demonstrated bias‑variance trade‑off clearly.  

- **Day 4 — Feature Engineering & Hyperparameter Tuning**  
  - Engineered `avg_spend_ratio`, `tenure_bucket`, `num_add_on_services`.  
  - GridSearchCV tuned Random Forest (`n_estimators`, `max_depth`, `min_samples_leaf`).  
  - Best params: `n_estimators=200`, `max_depth=None`, `min_samples_leaf=10`.  
  - Validation F1 improved to ≈ 0.633.  

- **Day 5 — Pipelines & Mini‑Project**  
  - Built leak‑free pipeline with ColumnTransformer + RandomForest.  
  - Tuned with GridSearchCV using pipeline syntax.  
  - Best params: `n_estimators=100`, `max_depth=10`, `min_samples_leaf=5`.  
  - CV F1 ≈ 0.636, Test F1 ≈ 0.635.  
  - Confirmed pipeline approach prevents leakage and matches capstone requirements.  

---

## ✅ Key Takeaways
- Honest evaluation requires strict separation of train/validation/test sets.  
- Cross‑validation provides more reliable performance estimates than single splits.  
- Bias‑variance trade‑off guides model complexity decisions.  
- Feature engineering and hyperparameter tuning together drive meaningful improvements.  
- Pipelines structurally eliminate leakage and are essential for production‑ready workflows.  

---

## 📌 Next Steps
- Extend pipeline to include additional models (e.g., Logistic Regression, Gradient Boosting).  
- Add evaluation metrics beyond F1 (precision, recall, ROC AUC).  
- Prepare pipeline structure for Phase 3 capstone project.  
