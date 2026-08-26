# Week 6 — Day 4: Building & Training a Network in Keras

**BinX Tech AI & ML Internship Program**

---

## 🎯 Objective
- Build a neural network with the Keras Sequential API.
- Compile, train, and evaluate the network, and read its training history.
- Apply batch normalization and dropout to stabilize training and reduce overfitting.

---

## 📘 Lesson Content
- **TensorFlow/Keras** — the standard high-level framework; you describe architecture layer by layer,
 Keras handles forward prop, backprop, and optimization automatically (the Days 2–3 mechanics, applied).
- **Sequential API & Dense layers** — layers stacked in order; `Dense` connects every input to every neuron.
- **Compile / fit / evaluate workflow** — mirrors the Scikit-learn API from Week 3: `compile()` sets optimizer/loss/metrics, `fit()` trains, `evaluate()` scores on the test set.
- **Reading training history** — the `history` object's per-epoch loss/metric curves are how overfitting/underfitting is diagnosed (Week 4 reasoning, applied to deep learning).
- **Batch normalization & dropout** — BatchNorm stabilizes/speeds up training by normalizing layer inputs; Dropout randomly disables neurons each step as a regularizer (the deep-learning analogue of Week 4 regularization).

---

## 📂 File Structure
Week6/

└── Day4/

├── Building & Training a Network in Keras.ipynb

├── healthcare-dataset-stroke-data.csv

└── Readme.md

- **Building & Training a Network in Keras.ipynb** → Lesson content + full hands-on lab: preprocessing, a baseline Keras network, 
a BatchNorm+Dropout variant, training-history diagnostics, and test-set evaluation compared against the Day 1 baseline
- **healthcare-dataset-stroke-data.csv** → Capstone project dataset (same file used since Week5/Day5 and Week6/Day1)
- **Readme.md** → Documentation of objectives, learning goals, and file organization

---

## 🧪 Hands-On Lab: Training a Neural Network
1. Build a Keras `Sequential` network for the stroke-prediction task (sigmoid output, binary cross-entropy loss).
2. Compile with Adam, train with a validation split for ≥30 epochs.
3. Plot training vs. validation loss/accuracy from `history` and diagnose the fit.
4. Add BatchNormalization + Dropout and compare loss curves to the first run.
5. Evaluate on the test set (precision, recall, F1, ROC-AUC) and compare to the Day 1 Logistic Regression baseline.

**Tools:** TensorFlow / Keras, Matplotlib, Jupyter/Colab (GPU)

---

## ✅ Key Takeaway
Keras automates the training loop from Day 3 
(forward → loss → backprop → update) behind `compile()`/`fit()`/`evaluate()`,
 letting the focus stay on architecture and regularization decisions rather than gradient math.
  BatchNorm and Dropout are the deep-learning equivalents of Week 4's regularization toolkit.

**Result:** on this dataset, the Day 1 Logistic Regression baseline (recall 0.800, ROC-AUC 0.844) 
outperformed both Keras variants — v1 (recall 0.400, ROC-AUC 0.765) and v2 with BatchNorm+Dropout (recall 0.700, ROC-AUC 0.793).
 BatchNorm+Dropout clearly improved the neural network over the plain version, but neither beat the simpler baseline. This is a legitimate,
  documented Sprint 1 finding: added architectural complexity isn't automatically added value on a modestly-sized,
   mostly-tabular dataset — exactly the kind of result Day 5's tuning experiments and Sprint Review are built to surface and act on.
