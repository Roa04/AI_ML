# Week 5 — Day 5: Phase 3 Project Selection & Sprint 1 Planning

**BinX Tech AI & ML Internship Program**

---

## 🎯 Objective
Close out Phase 2 by:
- Selecting a Phase 3 capstone project.
- Restating its **Definition of Done** (professional baseline).
- Producing a mentor-approved **Sprint 1 plan** (backlog, effort estimates, sprint goal, acceptance criteria).
- Setting up the GitHub repository and workflow before Phase 3 begins in Week 6.

---

## 📘 Lesson Content

### 5.1 Entering Phase 3
Phase 3 is the applied core of the program: each intern builds one complete AI/ML project end-to-end across four sprints (Weeks 6–9).  
Day 5 closes Phase 2 by selecting the project and planning Sprint 1.

### 5.2 Capstone Project Options
- Customer Churn Prediction  
- House Price Prediction  
- Sentiment Analysis Tool  
- Image Classifier  
- Recommendation System  
- **Fraud Detection Model** (imbalanced classification, precision-recall trade-offs, SHAP explanations)

### 5.3 Definition of Done (Professional Baseline)
Every capstone must deliver:
- A clean, documented Jupyter Notebook (EDA → preprocessing → modeling → evaluation).  
- A trained model with reported metrics: precision, recall, F1-score, ROC-AUC.  
- An unsupervised analysis section (clustering and/or PCA).  
- GitHub repo with README, `requirements.txt`, and saved model artifacts.  
- A short technical write-up explaining approach, trade-offs, and results.  
- Notebook runs top-to-bottom without errors.

### 5.4 Sprint 1 Planning
Sprint 1 focuses on dataset preparation, EDA, and a baseline model.  
Sprint goal: *“Understand the data and establish a baseline model to beat.”*

### 5.5 Backlog & Acceptance Criteria
Each task must have clear acceptance criteria: notebook runs cleanly, code committed to feature branch, PR opened for mentor review, results documented in Markdown, metrics logged.

---

## 🧩 Hands-On Lab: Project Kickoff & Sprint 1 Plan

### Step 1: Project Selection
**Chosen project:** Fraud Detection Model (reframed as stroke-risk prediction).  
**Rationale:** The healthcare stroke dataset has ~5% positive cases, mirroring fraud detection’s imbalanced classification challenge.

### Step 2: Problem Statement & Definition of Done
**Problem Statement:**  
Predict whether a patient is at risk of stroke using demographic and clinical data. Handle class imbalance explicitly, prioritizing recall over raw accuracy.

**Definition of Done:**  
- Notebook pipeline with imbalance-aware metrics.  
- Unsupervised analysis section.  
- GitHub repo with README, requirements, artifacts.  
- Technical write-up.  
- End-to-end reproducibility.

### Step 3: Sprint 1 Backlog

| # | Task | Effort | Acceptance Criteria |
|---|------|--------|---------------------|
| 1 | Dataset selection & framing | 0.5d | Dataset confirmed, target documented, data dictionary present. |
| 2 | Data preparation | 1d | Missing values handled, duplicates checked, invalid values validated, clean DataFrame committed. |
| 3 | Exploratory Data Analysis | 1.5d | Class balance visualized, distributions/outliers plotted, categorical counts, correlation heatmap, bivariate plots, findings summarized. |
| 4 | Preprocessing pipeline | 0.5d | Categorical encoded, numeric scaled, no leakage, documented. |
| 5 | Baseline model | 1d | Logistic Regression with `class_weight="balanced"`, stratified split, confusion matrix, precision/recall/F1/ROC-AUC logged, compared to naive baseline. |
| 6 | Sprint 1 retrospective | 0.5d | Markdown reflection on baseline results and Sprint 2 target. |

**Total effort:** ~5 days

### Step 4: Mentor Sign-Off
- [ ] Project scope approved  
- [ ] Sprint 1 goal and backlog approved  
- [ ] Cleared to begin Phase 3 (Week 6)  

### Step 5: GitHub Repository Setup
- Repo created (`stroke-risk-prediction`).  
- README skeleton committed.  
- `main` branch protected; feature-branch workflow (`sprint1-cleaning`, `sprint1-eda`, `sprint1-baseline`).  
- `requirements.txt` initialised.  
- `data/` and `outputs/` folders created.  
- `stroke_prediction.ipynb` committed as main notebook.

---

## ✅ Final Summary
- **Project selected:** Fraud Detection Model (stroke-risk prediction).  
- **Definition of Done:** Full pipeline notebook, imbalance-aware metrics, unsupervised analysis, clean repo, technical write-up.  
- **Sprint 1 goal:** Understand dataset + establish baseline model.  
- **Gate:** Mentor approval required before Phase 3 begins.

