# Week 4 — Day 4: Feature Engineering & Hyperparameter Tuning

## 📌 Objective
Improve on Day 3’s best model (Decision Tree, depth=5, validation F1 = 0.582) by:
- Engineering new input features from the Telco Customer Churn dataset.
- Systematically tuning Random Forest hyperparameters using `GridSearchCV`.

---

## 🧩 Key Steps
1. **Feature Engineering**
   - `avg_spend_ratio`: ratio of historical average spend to current monthly charges.
   - `tenure_bucket`: binned tenure into lifecycle stages (0–1yr, 1–2yr, 2–4yr, 4yr+).
   - `num_add_on_services`: count of optional services subscribed.

2. **Hyperparameter Tuning**
   - Defined grid:  
     - `n_estimators`: [100, 200, 400]  
     - `max_depth`: [5, 10, 15, None]  
     - `min_samples_leaf`: [1, 5, 10]  
   - Used 5-fold cross-validation with `class_weight="balanced"`.

3. **Model Comparison**
   - Day 3 Decision Tree (depth=5): **Val F1 = 0.582**  
   - Untuned Random Forest (new features): overfit, weaker validation F1.  
   - Tuned Random Forest (new features): **Val F1 ≈ 0.633**  

4. **Insights**
   - Most impactful engineered feature: `avg_spend_ratio` (#2 overall importance).  
   - Most critical hyperparameter: `min_samples_leaf` (prevented overfitting).  
   - Lesson: **Better features + controlled complexity > raw model power.**

---

## 🛠️ Tools & Libraries Used
- **Python** (Jupyter Notebook)
- **Pandas** — data loading and preprocessing
- **NumPy** — numerical operations
- **Scikit-learn**  
  - `RandomForestClassifier` — model training  
  - `GridSearchCV` — hyperparameter tuning  
  - `train_test_split`, `cross_val_score` — splitting and evaluation  
  - `f1_score` — performance metric
- **Matplotlib** — visualization of model comparison

---

## 📊 Results
- Validation F1 improved from **0.582 → 0.633**.
- Feature engineering and hyperparameter tuning worked together to achieve generalization.
- Random Forest with tuned parameters outperformed both the Day 3 Decision Tree and the untuned baseline.

---

## 📂 File Structure

Week4/

├── Day1/

├── Day2/

├── Day3/

├── Day4/

│   ├── day4.ipynb       # Jupyter Notebook with code, experiments, and results

│   ├── readme.md        # Documentation 

│   └── dataset/         # Telco Customer Churn dataset (CSV)



## ✅ Conclusion
Day 4 demonstrates that **feature engineering and hyperparameter tuning together** can significantly improve model performance. The tuned Random Forest achieved a validation F1 of 0.633, showing clear progress over Day 3’s baseline.
