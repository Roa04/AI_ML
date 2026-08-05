# 🚀 Day 4 — Trees, Forests, SVMs & k-NN

This repository contains two complementary notebooks for **Day 4** of the BinX Tech AI & ML Internship (Week 3).  
The first notebook covers the **lesson content** (theory + examples), while the second notebook is the **hands‑on lab** (practical model comparison).

---

## 📂 Repository Structure

Day4/
│
├── WA_Fn-UseC_-Telco-Customer-Churn.csv   # dataset file
├── Day4_LessonContent.ipynb               # theory: trees, forests, SVM, k-NN
├── Day4_HandsOnLab.ipynb                  # practical: model comparison
└── README.md                              # documentation


---

## 🎯 Learning Objectives
- Train and interpret **Decision Trees** and **Random Forests**, including feature importances  
- Train **SVM** and **k-NN** classifiers and explain how each makes decisions  
- Compare multiple classifiers fairly on the same train/test split and metric (F1-score)  

---

## 📚 Key Topics
- **Decision Trees:** interpretable rules, prone to overfitting  
- **Random Forests:** ensemble learning, strong default, feature importances  
- **Support Vector Machines (SVM):** margin maximization, kernel trick  
- **k-Nearest Neighbors (k-NN):** simple, distance-based voting  
- **Model Comparison:** no free lunch principle  

---

## 📖 Lesson Content Notebook
Covers the theory and examples for each classifier:
- **4.1 Decision Trees** — interpretable rules, risk of overfitting  
- **4.2 Random Forests** — ensemble of trees, reduces variance, reports feature importances  
- **4.3 SVM** — maximizes margin, kernel trick for non-linear boundaries  
- **4.4 k-NN** — predicts by majority vote of nearest neighbors  
- **4.5 Comparing Models** — train several models and compare fairly  

---

## 🧪 Hands-On Lab Notebook
### Steps
1. **Load & Preprocess Data** — clean missing values, encode categorical variables, scale features  
2. **Train Models** — Decision Tree, Random Forest, SVM, k-NN  
3. **Evaluate with F1-score** — compare all four models on the same test split  
4. **Feature Importance** — report Random Forest’s top features  
5. **Best Model** — identify and explain why it performed best  

### Results
- Decision Tree F1: **0.558**  
- Random Forest F1: **0.518**  
- SVM F1: **0.603**  
- k-NN F1: **0.546**  

**Best Model:** SVM (highest F1-score)  
**Interpretation:** SVM’s RBF kernel handled scaled features and non-linear boundaries better. Random Forest underperformed due to sparse one-hot features and lack of tuning.

---

## 🛠️ Tools Used
- **Scikit-learn** — tree, ensemble, svm, neighbors, metrics  
- **Pandas** — data loading and preprocessing  
- **StandardScaler** — feature scaling for SVM and k-NN  
- **Jupyter Notebook** — interactive coding and documentation  

---

## 📌 Key Takeaways
- Decision Trees are interpretable but prone to overfitting.  
- Random Forests are strong defaults and provide feature importances.  
- SVMs excel on scaled, high-dimensional data.  
- k-NN is simple but struggles with large datasets.  
- Comparing models fairly is essential — no free lunch principle.  
- In this lab, **SVM performed best** for churn prediction.  
