# 🚀 Day 3: Logistic Regression & Classification Metrics

This project is part of the **BinX Tech AI & ML Internship (Week 3)**.  
It demonstrates how to train and evaluate a **Logistic Regression classifier** on the Telco Customer Churn dataset, and why richer metrics beyond accuracy are essential for imbalanced data.

---

## 📚 Learning Objectives
- Train a logistic regression classifier and obtain class probabilities  
- Explain why accuracy alone is misleading on imbalanced data  
- Read a confusion matrix and compute precision, recall, F1, and AUC‑ROC  
- Decide whether precision or recall matters more for churn prediction  

---

## 📂 Dataset
The dataset used is the **Telco Customer Churn** dataset from Kaggle.
 It contains information about customers, their services, account information, and whether they churned.

---

## 🛠️ Tools Used
- **Scikit‑learn**  
- **Pandas**  
- **Matplotlib**
- **Seaborn** 

---

## 📂 Project Structure
Day3/
│
├── data/
│ └── WA_Fn-UseC_-Telco-Customer-Churn.csv # dataset
│
├── notebook/
│ └── day3 hands on lab.ipynb # Jupyter Notebook with code + markdown
│ └── Logistic Regression & Classification Metrics.ipynb
│
├── README.md # project documentation


---

## 🧪 Hands-On Lab Steps
1. **Train Model**  
   - Load and preprocess the Telco Customer Churn dataset.  
   - Split data into training and test sets (80/20).  
   - Scale features using `StandardScaler`.  
   - Fit a `LogisticRegression` classifier.  
   - Generate predictions and class probabilities.  

2. **Confusion Matrix**  
   - Evaluate predictions with TP, FP, FN, TN breakdown.  
   - Visualize with a heatmap.  

3. **Precision, Recall, F1**  
   - Compute metrics with `classification_report`.  
   - Interpret results for both churners and non‑churners.  

4. **Precision vs Recall Trade‑off**  
   - Decide which metric matters more for churn prediction.  
   - Final decision: prioritize **recall** to catch more churners.  

5. **AUC‑ROC**  
   - Plot ROC curve and compute AUC.  
   - AUC ≈ 0.86 → strong discriminative ability.  

---

## 📊 Results Summary
- **Accuracy:** 0.82 (misleading due to imbalance)  
- **Confusion Matrix:**  
  - TN = 934, FP = 102, FN = 151, TP = 222  
- **Precision (Churn):** 0.69  
- **Recall (Churn):** 0.60  
- **F1 (Churn):** 0.64  
- **AUC‑ROC:** 0.86  

---

## 📝 Key Takeaways
- Accuracy alone is not reliable for imbalanced datasets.  
- Confusion matrix reveals the types of errors made.  
- Precision and recall highlight trade‑offs in churn prediction.  
- Recall is prioritized to minimize missed churners.  
- AUC‑ROC provides a threshold‑independent measure of model quality.  

