# Week 6 — Day 2: Activations, Forward Propagation & Loss

**BinX Tech AI & ML Internship Program**

---

## 🎯 Objective
- Explain why non-linear activations are essential.
- Choose the correct activation for hidden and output layers.
- Describe forward propagation and select the right loss function for a task.

---

## 📘 Lesson Content
- **Why activations matter** — without non-linearity, stacked layers collapse into one linear model; the activation function is what lets a network learn curved, complex patterns.
- **Common activations** — ReLU (hidden layers, default), Sigmoid (binary output), Softmax (multi-class output), Tanh (zero-centered hidden layers).
- **Forward propagation** — data flows input → hidden → output, with each layer computing `activation(dot(input, W) + b)`.
- **Loss functions** — MSE for regression, binary cross-entropy for binary classification, categorical cross-entropy for multi-class.
- **Applied to the capstone:** stroke prediction is binary classification → **sigmoid** output activation + **binary cross-entropy** loss, with **ReLU** in any hidden layers.

---

## 📂 File Structure
Week6/

└── Day2/

├── Activations, Forward Propagation & Loss.ipynb

└── Readme.md

- **Activations, Forward Propagation & Loss.ipynb** → Lesson content, activation plots, and a manual NumPy forward pass on a sample patient
- **Readme.md** → Documentation of objectives, learning goals, and file organization

*No new dataset is introduced today — the forward-pass example uses a single standardized sample drawn from the same capstone stroke dataset (Week5/Day5, reused in Week6/Day1).*

---

## 🧪 Hands-On Lab: Activations & the Forward Pass
1. Plot ReLU, sigmoid, and tanh over a range of inputs.
2. Decide and justify the correct output activation and loss function for the capstone task.
3. Compute one forward pass by hand/NumPy for a tiny 2-layer network on a sample input.
4. Document the choices and forward-pass result in Markdown.

**Tools:** NumPy, Matplotlib, Jupyter/Colab

---

## ✅ Key Takeaway
Activation functions are what let a neural network model non-linear relationships instead of collapsing into a single linear equation. For the capstone's binary stroke-prediction task, that means a sigmoid output paired with binary cross-entropy loss — the exact pairing a network needs before it can be trained via backpropagation on Day 3.
