# BinX Tech AI & ML Internship — Week 3

## 📌 Overview
Week 3 focused on **Supervised Learning**.  
We built a full pipeline: **EDA → Preprocessing → Train/Test Split → Modeling → Evaluation**.  
Each day introduced new models, metrics, and best practices, culminating in a mini‑project on the Titanic dataset.

---

## 📅 Daily Breakdown

### Day 1 — Supervised Learning Basics
- Defined supervised learning: regression vs. classification.
- Learned the Scikit‑learn workflow: `fit → predict → score`.
- Introduced train/test split for honest evaluation.

### Day 2 — Regression Models
- Trained a **Linear Regression** model.
- Evaluated with regression metrics:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - R² (coefficient of determination)
- Compared against a naive baseline.

### Day 3 — Classification Metrics
- Trained a **Logistic Regression** classifier.
- Learned classification evaluation tools:
  - Confusion matrix
  - Precision, Recall, F1‑score
  - ROC curve and AUC
- Understood why accuracy alone is misleading on imbalanced data.

### Day 4 — Model Comparisons
- Compared multiple classifiers fairly:
  - Decision Tree
  - Random Forest
  - K‑Nearest Neighbors (KNN)
  - Support Vector Machine (SVM)
- Used the same train/test split and metrics for consistency.
- Observed trade‑offs between precision and recall.

### Day 5 — Mini‑Project: Titanic Survival Prediction
- Built a complete pipeline:
  - **EDA**: distributions, correlations, missing values.
  - **Preprocessing**: imputation, encoding, scaling (fit on train only).
  - **Modeling**: baseline + five classifiers.
  - **Evaluation**: accuracy, precision, recall, F1, ROC‑AUC.
- **Result:**  
  - Best model: **KNN** with F1‑score = 0.491.  
  - Baseline F1‑score = 0.000 → improvement of +0.491.  
  - KNN balanced precision (0.684) and recall (0.382) better than other models.  
  - Logistic Regression and SVM had higher precision but very low recall.  
  - Random Forest underperformed compared to expectations.

---

## ✅ Key Learnings
- Always include a **baseline** for honest comparison.  
- Decide metrics **before evaluation** (F1 for imbalanced classification).  
- Fit preprocessing steps on **training data only** to avoid data leakage.  
- Narration and documentation are essential — code alone is not a deliverable.  
- Random state (`random_state=42`) ensures reproducibility.

---

## 📂 Repository Structure
- `Week3/Day1` — supervised learning introduction.  
- `Week3/Day2` — linear regression + metrics.  
- `Week3/Day3` — logistic regression + classification metrics.  
- `Week3/Day4` — decision tree, random forest, KNN, SVM.  
- `Week3/Day5` — full pipeline project.   
- `README.md` — summary of Week 3.


---

## 🚀 Conclusion
Week 3 provided a complete rehearsal of the supervised learning workflow.  
By the end of the week, we could:
- Build end‑to‑end pipelines.  
- Evaluate models with the right metrics.  
- Justify model choices against baselines.  
- Document results clearly for reproducibility.

This foundation prepares us for larger capstone projects in later phases.
# BinX Tech AI & ML Internship — Week 3

## 📌 Overview
Week 3 focused on **Supervised Learning**.  
We built a full pipeline: **EDA → Preprocessing → Train/Test Split → Modeling → Evaluation**.  
Each day introduced new models, metrics, and best practices, culminating in a mini‑project on the Titanic dataset.

---

## 📅 Daily Breakdown

### Day 1 — Supervised Learning Basics
- Defined supervised learning: regression vs. classification.
- Learned the Scikit‑learn workflow: `fit → predict → score`.
- Introduced train/test split for honest evaluation.

### Day 2 — Regression Models
- Trained a **Linear Regression** model.
- Evaluated with regression metrics:
  - Mean Absolute Error (MAE)
  - Root Mean Squared Error (RMSE)
  - R² (coefficient of determination)
- Compared against a naive baseline.

### Day 3 — Classification Metrics
- Trained a **Logistic Regression** classifier.
- Learned classification evaluation tools:
  - Confusion matrix
  - Precision, Recall, F1‑score
  - ROC curve and AUC
- Understood why accuracy alone is misleading on imbalanced data.

### Day 4 — Model Comparisons
- Compared multiple classifiers fairly:
  - Decision Tree
  - Random Forest
  - K‑Nearest Neighbors (KNN)
  - Support Vector Machine (SVM)
- Used the same train/test split and metrics for consistency.
- Observed trade‑offs between precision and recall.

### Day 5 — Mini‑Project: Titanic Survival Prediction
- Built a complete pipeline:
  - **EDA**: distributions, correlations, missing values.
  - **Preprocessing**: imputation, encoding, scaling (fit on train only).
  - **Modeling**: baseline + five classifiers.
  - **Evaluation**: accuracy, precision, recall, F1, ROC‑AUC.
- **Result:**  
  - Best model: **KNN** with F1‑score = 0.491.  
  - Baseline F1‑score = 0.000 → improvement of +0.491.  
  - KNN balanced precision (0.684) and recall (0.382) better than other models.  
  - Logistic Regression and SVM had higher precision but very low recall.  
  - Random Forest underperformed compared to expectations.

---

## ✅ Key Learnings
- Always include a **baseline** for honest comparison.  
- Decide metrics **before evaluation** (F1 for imbalanced classification).  
- Fit preprocessing steps on **training data only** to avoid data leakage.  
- Narration and documentation are essential — code alone is not a deliverable.  
- Random state (`random_state=42`) ensures reproducibility.


---

## 🚀 Conclusion
Week 3 provided a complete rehearsal of the supervised learning workflow.  
By the end of the week, we could:
- Build end‑to‑end pipelines.  
- Evaluate models with the right metrics.  
- Justify model choices against baselines.  
- Document results clearly for reproducibility.

This foundation prepares us for larger capstone projects in later phases.
