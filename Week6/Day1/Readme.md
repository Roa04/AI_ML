# Week 6 — Day 1: Sprint 1 Kickoff — Neural Network Foundations & Baseline Model

**BinX Tech AI & ML Internship Program**

---

## 🎯 Objective

- Completing Sprint 1 planning and establishing a **baseline model** for the capstone project.
- Understanding the neuron as a weighted sum + bias + activation — a direct extension of the Week 2 dot product and Week 3 logistic regression.
- Describing the input/hidden/output layer structure and what makes a network "deep."

---

## 📘 Lesson Content
- **Why deep learning, and why now** — classical ML (Weeks 3–5) suits structured/tabular data; deep learning earns its complexity on unstructured, high-dimensional data.
- **The neuron** — `output = activation(w · x + b)`, the same math as logistic regression plus an explicit bias and activation function.
- **Layers & depth** — input layer → hidden layer(s) → output layer; "deep" means more than one hidden layer.
- **Weights & biases** — the learned parameters, set up here conceptually ahead of backpropagation (Day 3).

---

## 📂 File Structure
Week6/

└── Day1/

├── Sprint 1 Kickoff & Neural Network Foundations.ipynb

├── healthcare-dataset-stroke-data.csv

└── Readme.md

- **Sprint 1 Kickoff & Neural Network Foundations.ipynb** → Lesson content on neurons/layers + hands-on Sprint 1 kickoff lab
- **healthcare-dataset-stroke-data.csv** → Capstone project dataset (stroke-risk prediction, framed as imbalanced classification)
- **Readme.md** → Documentation of objectives, learning goals, and file organization

---

## 🧪 Hands-On Lab: Sprint 1 Kickoff & Baseline
1. Load the stroke-risk dataset and confirm the data dictionary.
2. Run a brief EDA to confirm class imbalance (~5% positive class).
3. Build a leak-free `Pipeline` (impute → scale/encode → model).
4. Train a **Logistic Regression baseline** with `class_weight="balanced"` on a stratified train/test split.
5. Evaluate with imbalance-aware metrics: precision, recall, F1-score, ROC-AUC.
6. Record the baseline in Markdown — the score every later model (including neural network approaches) must beat.

**Tools:** Scikit-learn (baseline pipeline), Pandas, Seaborn/Matplotlib, Jupyter/Colab, Git & GitHub

---

## ✅ Key Takeaway
A single neuron is just logistic regression with an explicit bias and activation function — deep learning builds on math already covered, it doesn't replace it. On the project side, Sprint 1's Task 5 is now satisfied: a documented, imbalance-aware Logistic Regression baseline is committed and ready for mentor review, giving Sprint 2+ a concrete number to beat.
