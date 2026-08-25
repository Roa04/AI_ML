# Week 6 — Day 3: Backpropagation, Gradient Descent & Optimizers

**BinX Tech AI & ML Internship Program**

---

## 🎯 Objective
- Describe the four-step training loop of a neural network.
- Explain gradient descent and the role of the learning rate.
- Explain backpropagation conceptually and name common optimizers, epochs, and batches.

---

## 📘 Lesson Content
- **Training loop** — forward pass → compute loss → backpropagation → update weights, repeated across batches and epochs.
- **Gradient descent** — moves each weight opposite the gradient (downhill on the loss surface) to reduce loss.
- **Learning rate** — the step size; too high overshoots/diverges, too low trains slowly, just right decreases steadily.
- **Backpropagation** — computes gradients backward through the network via the chain rule, "assigning blame" to each weight; done automatically by frameworks (TensorFlow `GradientTape`, PyTorch `autograd`).
- **Optimizers, epochs, batches** — Adam is the strong default optimizer; an epoch is one full pass through the training data; a batch is a subset processed before each weight update.

---

## 📂 File Structure
Week6/

└── Day3/

├── Backpropagation, Gradient Descent & Optimizers.ipynb

└── Readme.md

- **Backpropagation, Gradient Descent & Optimizers.ipynb** → Lesson content, four-step training loop diagram, 1D gradient descent experiment at three learning rates, and a written explanation of backpropagation/the chain rule
- **Readme.md** → Documentation of objectives, learning goals, and file organization

*No new dataset today — the learning-rate experiment uses a toy 1D loss surface, `L(w) = (w - 3)^2`, to isolate and visualize the learning rate's effect without the overhead of a full network.*

---

## 🧪 Hands-On Lab: Understanding Training + Mentor Review
1. Describe the four-step training loop in a Markdown cell.
2. Run gradient descent at three learning rates (too high, too low, good) and plot the loss curves.
3. Explain, in your own words, what backpropagation computes and why the chain rule is involved.
4. **Mentor Code & Notebook Review** — submit the capstone notebook via GitHub pull request for mid-sprint mentor feedback.

**Tools:** NumPy, Matplotlib, Jupyter/Colab, GitHub (pull request for mentor review)

---

## ✅ Key Takeaway
Backpropagation and gradient descent are how a network turns a high loss into low loss over time — backprop assigns blame to each weight via the chain rule, and gradient descent uses that blame to nudge weights downhill on the loss surface. The learning rate is the dial that determines whether that descent is unstable, too slow, or efficient — the first hyperparameter to check when a training run misbehaves. Today's mentor review is the Sprint 1 mid-point checkpoint, confirming the baseline and conceptual foundation are solid before building the actual Keras network on Day 4.
