
# Week 4 — Day 3: Bias-Variance & Diagnosing Model Fit


## 📌 Objective
Diagnose model fit by deliberately **underfitting** and **overfitting** a Decision Tree, then use the **bias-variance trade-off** to find a better balance.  
Compare training vs. validation F1-scores across different tree depths to understand how model complexity drives underfitting and overfitting, and why closing the train-validation gap alone does not guarantee a good model.

---



### 📂 File Structure

week4/day3/
│── Day3 week4.ipynb   # Jupyter notebook with code and analysis
│── dataset/           # Telco Customer Churn dataset (CSV)
│── README.md          # Documentation (this file)



---

## 📊 Dataset
- **Telco Customer Churn**
- Preprocessing:
  - `TotalCharges` cleaned (converted to numeric, blanks filled with 0)
  - `customerID` dropped
  - `Churn` mapped to binary (0 = No, 1 = Yes)
  - One-hot encoding applied to categorical features
  - Train/validation sets aligned to same columns

---

## ⚙️ Hands-On Lab Steps

### Step 1 — Overfit Model (Unlimited Depth)
- **Training F1:** 0.996  
- **Validation F1:** 0.481  
- **Gap:** 0.515  
- **Diagnosis:** High variance — memorized training data, poor generalization.

### Step 2 — Underfit Model (Depth = 1)
- **Training F1:** 0.000  
- **Validation F1:** 0.000  
- **Gap:** 0.000  
- **Diagnosis:** High bias — too simple, fails to capture churn patterns.

### Step 3 — Sweep Tree Depths (2–10)
- Validation F1 peaked at **0.582** (Depth = 5).  
- Gap ≈ **0.019** → Best balance between bias and variance.  
- Beyond depth 5, training rises but validation plateaus/drops → overfitting returns.

### Step 4 — Final Diagnosis
| Model        | Train F1 | Validation F1 | Gap   | Diagnosis        |
|--------------|----------|---------------|-------|-----------------|
| Underfit     | 0.000    | 0.000         | 0.000 | High Bias       |
| Overfit      | 0.996    | 0.481         | 0.515 | High Variance   |
| Depth 10     | 0.757    | 0.529         | 0.228 | Moderate Overfit|
| **Depth 5**  | **0.601**| **0.582**     | **0.019** | **Optimal Fit** |

---

## 📈 Key Insights
- **Bias-Variance Trade-off:**  
  - Depth 1 → High bias (underfitting)  
  - Unlimited depth → High variance (overfitting)  
  - Depth 5 → Optimal balance, best generalization

- **Gap alone isn’t enough:**  
  Smaller gap doesn’t guarantee a good model — both scores must be high.

- **Regularization parallel:**  
  - Decision Trees use `max_depth`  
  - Linear models use `alpha` (Ridge/Lasso) to control complexity

---

## ✅ Final Recommendation
- Best model: **Decision Tree with max_depth = 5**  
- Validation F1 = **0.582** (21% improvement over unrestricted tree)  
- Gap = **0.019** → Strong generalization  
- Next steps:  
  - Deploy depth-5 model  
  - Explore ensemble methods (Random Forest, Gradient Boosting)  
  - Tune hyperparameters (`min_samples_split`, `min_samples_leaf`)  
  - Monitor performance on new data
