# Titanic Survival Prediction — Supervised Learning Mini‑Project

## 📌 Project Overview
This mini‑project applies a full supervised learning pipeline to the Titanic dataset (`tested.csv`).  
The goal is to predict passenger survival (`Survived` = 0/1) using classification models, and to evaluate them against a naive baseline.

---

## ⚙️ Steps in the Pipeline
1. **Setup**  
   - Imported Pandas, NumPy, Matplotlib, Seaborn, and Scikit‑learn.  
   - Verified library versions for reproducibility.

2. **Dataset & Task**  
   - Loaded Titanic dataset.  
   - Target variable: `Survived` (binary classification).

3. **EDA (Exploratory Data Analysis)**  
   - Plotted Age distribution and Sex counts.  
   - Generated correlation heatmap.  
   - Checked missing values and class balance.  
   - Found overall survival rate ≈ 38%.

4. **Preprocessing**  
   - Filled missing values (`Age`, `Fare` with median; `Cabin` with "no cabin").  
   - Dropped irrelevant columns (`Name`, `Ticket`, `Cabin`).  
   - Encoded categorical features (`Sex` with LabelEncoder, `Embarked` with one‑hot encoding).  
   - Scaled numeric features (`Age`, `Fare`, `SibSp`, `Parch`, `Pclass`) using `StandardScaler`.  
   - Train/test split with `random_state=42`.

5. **Modeling**  
   - Trained six models:  
     - DummyClassifier (baseline)  
     - Logistic Regression  
     - Decision Tree  
     - Random Forest  
     - K‑Nearest Neighbors (KNN)  
     - Support Vector Machine (SVM)

6. **Evaluation**  
   - Computed Accuracy, Precision, Recall, and F1‑score for all models.  
   - Compared results in a table sorted by F1‑score.  
   - Selected best model by F1‑score.  
   - Printed classification report and confusion matrix.  
   - Computed ROC‑AUC and plotted ROC curve.

---

## 📊 Results
- **Baseline F1‑score:** 0.000 (always predicts majority class).  
- **Best Model:** **KNN**  
  - F1‑score: **0.491** (improvement of +0.491 over baseline).  
  - Precision: 0.684  
  - Recall: 0.382  
- Logistic Regression and SVM had higher precision but very low recall.  
- Random Forest underperformed compared to expectations.  
- KNN provided the best balance between precision and recall, making it the most useful model overall.

---

## ✅ Key Learnings
- Always include a baseline for honest comparison.  
- Accuracy alone is misleading on imbalanced data — F1‑score is more informative.  
- Preprocessing must be fit on training data only to avoid data leakage.  
- Narration and documentation are essential for a complete deliverable.  

---

## 🔒 Reproducibility
- Fixed `random_state=42` for train/test split and models.  
- Documented each stage with Markdown.  
- Final notebook ready to commit to GitHub with clear commit message.

---

## 📂 Repository Structure
- `Titanic_Week3_MiniProject.ipynb` — full notebook with code + narration.  
- `tested.csv` — dataset used.  
- `README.md` — project overview and documentation.

---

## 🚀 Conclusion
The KNN classifier was the best performer in this mini‑project, achieving an F1‑score of 0.491 and demonstrating useful predictive power compared to the naive baseline. This pipeline serves as a rehearsal for larger supervised learning projects, combining EDA, preprocessing, modeling, evaluation, and documentation into one reproducible workflow.
