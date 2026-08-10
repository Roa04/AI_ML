# Week 4 — Day 2: Cross-Validation

**BinX Tech AI & ML Internship — Phase 2**

## 📂 Folder Structure
week4/
├── day1/
├── day2/
│   ├── hands_on_lab_day2.ipynb
│   ├── WA_Fn-UseC_-Telco-Customer-Churn.csv
│   └── Readme.md

- **hands_on_lab_day2.ipynb** → Jupyter notebook with the Day 2 lab code and explanations  
- **WA_Fn-UseC_-Telco-Customer-Churn.csv** → Dataset used for churn prediction  

---

## 📘 Dataset
- **Telco Customer Churn** dataset  
- Target: `Churn` (binary classification: 1 = churn, 0 = no churn)  
- Preprocessing:
  - `TotalCharges` converted to numeric, missing values filled with 0  
  - `customerID` dropped (identifier only)  
  - `Churn` mapped from Yes/No to 1/0  
  - One‑hot encoding applied to categorical features  

---

## 🧪 Lab Steps

### Step 1: 5‑Fold Cross‑Validation
- Model: **RandomForestClassifier (n_estimators=300)**  
- Evaluation metric: **F1‑score (churn class)**  
- Used **StratifiedKFold** to preserve class balance in each fold.  
- Each fold trained on 4/5 of the data and validated on 1/5.

### Step 2: Mean & Standard Deviation
- Reported the mean F1 across folds as the reliable performance estimate.  
- Reported the standard deviation to measure variability.  
- Visualized fold scores with a bar chart.

### Step 3: Compare to Day 1 Single Split
- Day 1 single validation split gave churn F1 ≈ **0.57**.  
- Day 2 5‑fold CV mean F1 ≈ **0.54 ± 0.025**.  
- Difference shows Day 1’s split was slightly optimistic; CV gives a more honest estimate.

### Step 4: Stratified Folds
- Confirmed stratification preserved the churn/no‑churn ratio (~74% vs. 26%) in each fold.  
- Explanation: Without stratification, some folds might have too few churners, leading to misleading F1 scores.

---

## 🔑 Key Takeaways
- **Cross‑validation** provides a more reliable estimate than a single split.  
- **Stratification** is essential for imbalanced datasets like churn prediction.  
- The **mean CV F1‑score** is the best indicator of real‑world performance.  
- Day 1’s single split overstated performance; Day 2’s CV corrected that bias.  

---

## ▶️ How to Run
1. Open `hands_on_lab_day2.ipynb` in Jupyter Notebook or VS Code.  
2. Run all cells sequentially.  
3. Inspect the printed F1 scores and the bar chart visualization.  
4. Compare CV results to Day 1 single‑split validation.  

---

## 📊 Results Summary
- **Day 1 single split F1 (churn):** ~0.57  
- **Day 2 5‑fold CV mean F1:** ~0.54 (±0.025)  
- Conclusion: Cross‑validation gives a more stable and realistic estimate of churn detection performance.

---

## 🛠️ Tools Used
- Scikit-learn (`cross_val_score`, `StratifiedKFold`, `RandomForestClassifier`)
- Pandas
- Matplotlib
- Jupyter Notebook