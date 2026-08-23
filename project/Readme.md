```
# 🧠 Stroke Prediction — Machine Learning Project

## 📖 Overview
This project is part of the **BinX Tech AI & ML Internship (Weeks 1–5)**.
It applies a complete machine learning workflow to the **Healthcare Stroke Prediction Dataset**, following the curriculum pipeline:

1. Environment & Dataset Setup
2. Data Preparation (missing values, duplicates, validation)
3. Exploratory Data Analysis (EDA)
4. Supervised Learning (Logistic Regression baseline, Random Forest comparison)
5. Model Evaluation (cross-validation, metrics, ROC-AUC, confusion matrix)
6. Feature Engineering & Leak-Free Pipeline
7. Hyperparameter Tuning (GridSearchCV)
8. Unsupervised Analysis (PCA, K-Means, DBSCAN, Hierarchical clustering, Isolation Forest)
9. Final Summary & Insights

---

## 📂 Project Structure
```
ai_ml/
└── project/
    ├── README.md              # Project documentation (this file)
    ├── data/
        └── healthcare-dataset-stroke-data.csv   # Dataset
    ├── project.ipynb             # Jupyter Notebook (main workflow)
    ├── requirements.txt          # Python dependencies
    └── outputs/                  # Generated plots & figures
        ├── 1-Target Class Distribution.png
        ├── 2-Distribution of Numerical Features.png
        ├── 3-Categorical Feature Counts.png
        ├── 4-Potential Outliers.png
        ├── 5-Numerical Features & Target.png
        ├── 6-Numeric Features Across Stroke Classes.png
        ├── 7-Model Evaluation.png
        ├── 8-Model Evaluation ROC Curve Stroke Prediction.png
        ├── 9-MK-Means Clusters Visualized via PCA.png
        ├── 10_kmeans_elbow_silhouette.png
        ├── 11_hierarchical_dendrogram.png
        ├── 12_pca_cumulative_variance.png
        ├── 13_pca_2d_kmeans.png
        ├── 14_pca_vs_tsne.png
        ├── 15_isolation_forest_tsne.png

````

---

## 📊 Dataset
- **File:** `healthcare-dataset-stroke-data.csv`
- **Target Variable:** `stroke` (1 = patient had a stroke, 0 = no stroke)
- **Features:** Demographic and clinical attributes (age, gender, hypertension, glucose level, BMI, smoking status, etc.)

---

## ⚙️ Requirements
Install dependencies using:
```bash
pip install -r requirements.txt
````

Main libraries:

-   NumPy, Pandas

-   Matplotlib, Seaborn

-   Scikit-learn, SciPy

## 🚀 Running the Project

1.  Open `project.ipynb` in Jupyter Notebook.

2.  Run all cells sequentially.

3.  Outputs (plots, evaluation figures) will be saved automatically in the `outputs/` folder.

## 📌 Key Findings

-   **Data Quality:** Only BMI had missing values (handled with median imputation).

-   **Target Imbalance:** Stroke cases ~5% → recall is prioritized over accuracy.

-   **Modeling:** Logistic Regression vs. Random Forest, evaluated with F1, precision, recall, ROC-AUC.

-   **Feature Engineering:** Added `glucose_per_age` feature, improving predictive signal.

-   **Pipeline & Tuning:** Leak-free preprocessing pipeline with `ColumnTransformer`; hyperparameter tuning improved F1.

-   **Unsupervised Analysis:**

    -   PCA + K-Means revealed clusters where older, high-glucose patients had higher stroke rates.

    -   DBSCAN flagged ~noise points as outliers.

    -   Hierarchical clustering suggested 2–3 nested patient groupings.

    -   Isolation Forest anomalies overlapped partially with stroke cases, highlighting unusual feature combinations.

## ⚠️ Disclaimer

This project is for **educational purposes only** and is **not intended for clinical diagnosis or medical decision-making**.