# Week 6 — Day 5: Tuning, Evaluation & Sprint Review

**BinX Tech AI & ML Internship Program**

---

## 🎯 Objective
- Tune a neural network systematically, one variable at a time.
- Use EarlyStopping and checkpoints to train efficiently and keep the best model.
- Complete the Sprint 1 review and retrospective cycle.

---

## 📘 Lesson Content
- **Tuning priority** — learning rate, network width/depth, dropout rate, batch size; change one variable at a time and watch validation loss.
- **Callbacks** — `EarlyStopping` halts training once validation loss stops improving (prevents wasted epochs/overfitting); `ModelCheckpoint` saves the best model seen, not just the last epoch.
- **Sprint Review prep** — acceptance criteria: notebook runs error-free, code committed to the correct branch, PR approved by mentor, results documented in Markdown, metrics compared to baseline.
- **Sprint Review & Retrospective** — demo Sprint 1 work to the mentor; carry over unfinished backlog items with a documented reason; retrospective covers what went well, what to improve, and one concrete change for Sprint 2.

---

## 📂 File Structure
Week6/

└── Day5/

├── Tuning, Evaluation & Sprint Review.ipynb

├── healthcare-dataset-stroke-data.csv

└── Readme.md

- **Tuning, Evaluation & Sprint Review.ipynb** → Lesson content + one-variable-at-a-time tuning experiments (learning rate, dropout, batch size) with EarlyStopping, a full Sprint 1 evidence table, and the Sprint Review/Retrospective write-up
- **healthcare-dataset-stroke-data.csv** → Capstone project dataset (same file used since Week5/Day5)
- **Readme.md** → Documentation of objectives, learning goals, and file organization

---

## 🧪 Hands-On Lab: Sprint 1 Close-Out
1. Tune one hyperparameter at a time (learning rate, dropout, batch size) and record each run's validation/test score.
2. Add `EarlyStopping` and confirm it halts training at the right point, restoring the best weights.
3. Assemble the Sprint 1 evidence: baseline vs. neural network scores, architecture, and loss curves.
4. Ensure all Sprint 1 work is committed, PR merged after mentor approval, notebook documented.
5. Present the Sprint Review, then write the Retrospective with one concrete change for Sprint 2.

**Tools:** TensorFlow / Keras, Matplotlib, Git & GitHub, Draft project report

---

## ✅ Key Takeaway
Systematic, one-variable-at-a-time tuning plus EarlyStopping is how a network is improved responsibly, without wasting compute or fooling yourself into thinking noisier training curves are progress. Sprint 1 closes with an honest result: per your actual project numbers, the class-weighted Logistic Regression baseline (Recall 80.0%, ROC-AUC 0.840) outperformed both Keras variants and Random Forest — a legitimate finding that should shape Sprint 2's priorities (e.g. threshold tuning or resampling) rather than defaulting to a deeper network.
