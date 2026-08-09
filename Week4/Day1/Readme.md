
# Week 4 — Day 1: Train / Validation / Test Splits
**BinX Tech AI & ML Internship — Phase 2**

## 🎯 Objective
The goal of Day 1 is to:
- Understand the importance of a **three‑way split (train, validation, test)**.
- Train a baseline classification model.
- Tune **one hyperparameter** using the validation set only.
- Evaluate the final model on the test set exactly once for an unbiased score.
- Explain why tuning against the test set causes data leakage.

---

## 📘 Key Topics
- **Train/Validation/Test Split (60/20/20)**  
  - Train: model learns patterns.  
  - Validation: tuning decisions.  
  - Test: sealed until the end for honest evaluation.  

- **Baseline Model**  
  - Random Forest classifier trained with default parameters.  
  - Compared train vs validation accuracy to detect overfitting.  

- **Hyperparameter Tuning**  
  - Adjusted `n_estimators` using validation set only.  
  - Best validation accuracy achieved at 300 trees.  

- **Final Evaluation**  
  - Test accuracy reported once.  
  - ROC curve & AUC (≈ 0.84).  
  - Confusion matrix showing false positives/negatives.  
  - Classification report with precision, recall, F1.  

- **Reflection**  
  - Why tuning on the test set leaks information.  
  - How the three‑way split ensures unbiased performance estimates.

---

## 📂 Project Structure
```plaintext
Week4-Day1/
│
├── README.md 
├── hands_on_lab.ipynb
│
|__ WA_Fn-UseC_-Telco-Customer-Churn.csv   # Dataset (Telco Customer Churn)
---

## 📊 Results
- **Validation accuracy peak**: ~300 trees  
- **Test accuracy**: ~80–82%  
- **AUC**: 0.84  
- **Churn recall**: ~0.47 (model misses more than half of churners due to imbalance)

---

## 🚀 Takeaways
- The three‑way split prevents test set leakage.  
- Validation set is the safe sandbox for tuning.  
- Accuracy alone is misleading — ROC, confusion matrix, and classification report give deeper insight.  
- Imbalanced datasets bias models toward the majority class; later weeks cover balancing techniques.



