# Week 7 — Day 1: Sprint 2 Planning & Convolutional Neural Networks

**BinX Tech AI & ML Internship Program**

---

## 🎯 Objective
- Complete Sprint 2 planning and define the core-model backlog.
- Explain why dense networks fail on images.
- Explain convolution, filters, and feature maps, and why CNNs are efficient.

---

## 📘 Lesson Content
- **Sprint 2 planning** — goal (advance the core model past the Week 6 baseline), backlog, carrying forward the Sprint 1 retrospective action (prioritize imbalance handling).
- **Why dense networks fail on images** — millions of weights needed, and spatial structure is discarded entirely.
- **Convolution** — a small filter (kernel) slides across the image, computing a dot product at each position (the Week 2 dot product, applied locally and repeatedly); output is a feature map.
- **Parameter sharing & translation invariance** — a CNN reuses the same small filter everywhere, needing vastly fewer weights than a dense layer, and detects patterns regardless of position.
- **Feature hierarchy** — early layers detect edges, middle layers combine them into textures/shapes, deep layers recognize whole structures — learned from data, not hand-designed.

---

## 📂 File Structure
Week7/

└── Day1/

├── Sprint 2 Kickoff & Convolutional Neural Networks.ipynb

└── Readme.md

- **Sprint 2 Kickoff & Convolutional Neural Networks.ipynb** → Lesson content, Sprint 2 planning, dataset loading/class-balance check, a hand-computed convolution/feature-map demo, and the architecture decision record
- **Readme.md** → Documentation of objectives, learning goals, and file organization

---

## 🖼️ Project (Image Track)
**Dataset:** [Melanoma Skin Cancer Dataset — Benign vs. Malignant](https://www.kaggle.com/datasets/ailearner-researchlab/melanoma-skin-cancer-dataset-benign-vs-malignant) (dermoscopic images, binary classification)

Chosen because it's a real, clinically-relevant binary classification task — consistent with the health-data theme of the Sprint 1 (stroke prediction) work — and matches the program's own guidance: *"if the Phase 3 project is the Image Classifier, transfer learning is almost always the right approach."*

*Note: `DATA_DIR` in the notebook is a placeholder — update it to wherever you extract the Kaggle dataset (locally or after uploading/downloading via the Kaggle API in Colab).*

---

## 🧪 Hands-On Lab: Sprint 2 Kickoff & Convolution
1. Complete Sprint 2 planning and select the core-model backlog tasks.
2. Load the dataset and confirm class balance (benign vs. malignant).
3. Apply a hand-defined edge-detection filter to a sample image and visualize the resulting feature map.
4. Explain, in Markdown, why the same filter across the whole image needs far fewer weights than a dense layer (with the actual weight-count comparison computed).
5. Confirm the project's data type calls for a CNN, and record the decision.

**Tools:** TensorFlow/Keras, NumPy, Matplotlib, Jupyter/Colab, Git & GitHub

---

## ✅ Key Takeaway
A single 3×3 convolution filter needs about 116,000× fewer weights than a dense layer covering the same 128×128 image — parameter sharing is what makes CNNs computationally feasible on real image sizes, and translation invariance is what makes them effective regardless of where a pattern (like an irregular lesion border) appears in the frame. With the architecture decision recorded (CNN + transfer learning), Day 2 builds the actual network.
