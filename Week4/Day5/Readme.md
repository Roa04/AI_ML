# Week 4 — Day 5: Scikit-learn Pipelines & Tuned Mini-Project

**Dataset:** Telco Customer Churn  
**Task:** Binary Classification — will a customer leave? (Churn: Yes/No)

---

## 📂 File Structure
Week4/

├── day1/

├── day2/

├── day3/

├── day4/

└── day5/

├── day5.ipynb

├── README.md

└── WA_Fn-UseC_-Telco-Customer-Churn.csv


---

## 🎯 Objective
Build a **leak-free end-to-end pipeline** that chains preprocessing and modeling into one object, tune it with **GridSearchCV**, and evaluate it once on the held-out test set. This mirrors the workflow required for the Phase 3 capstone.

---

## 📘 Lesson Highlights
- **Pipelines Prevent Leakage** → preprocessing and modeling chained together ensure scalers/encoders are fit only on training folds.  
- **ColumnTransformer** → handles numeric and categorical features separately inside the pipeline.  
- **GridSearchCV** → tunes hyperparameters across the entire pipeline using `step__param` notation.  
- **Mini-Project** → engineered features + tuned pipeline evaluated on held-out test set.

---

## 🛠 Workflow
1. **Data Cleaning & Feature Engineering**
   - Converted `TotalCharges` to numeric, filled blanks with 0.  
   - Dropped `customerID`.  
   - Encoded `Churn` as 0/1.  
   - Engineered features: `avg_spend_ratio`, `tenure_bucket`, `num_add_on_services`.

2. **Train/Test Split**
   - 80/20 stratified split.  
   - Cross-validation performed only on `X_train`.

3. **Pipeline Construction**
   - Numeric features scaled with `StandardScaler`.  
   - Categorical features one-hot encoded with `OneHotEncoder(handle_unknown="ignore")`.  
   - RandomForestClassifier with `class_weight="balanced"` as the model.

4. **Hyperparameter Tuning**
   - GridSearchCV with 5-fold CV.  
   - Parameters tuned: `n_estimators`, `max_depth`, `min_samples_leaf`.

5. **Evaluation**
   - Best params: `n_estimators=100`, `max_depth=10`, `min_samples_leaf=5`.  
   - Best CV F1: **0.636**  
   - Test F1 (tuned pipeline): **0.635**  
   - Day 4 baseline val F1: **0.633**  
   - Day 3 best val F1: **0.582**

---

## ✅ Results & Key Takeaways
- The tuned pipeline slightly improved over Day 4’s baseline and significantly outperformed Day 3.  
- Pipelines structurally prevent data leakage by re-fitting preprocessing per fold.  
- This workflow is the exact structure required for the Phase 3 capstone project.

---
