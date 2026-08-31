# Week 7 — Day 2: Building CNNs & Transfer Learning

**BinX Tech AI & ML Internship Program**

---

## 🎯 Objective
- Build a full CNN with convolution, pooling, and dense layers.
- Apply data augmentation to reduce overfitting on image data.
- Use transfer learning with a pre-trained model to get strong results from little data.

---

## 📘 Lesson Content
- **Pooling** — max pooling shrinks feature maps, reducing computation and controlling overfitting while adding robustness to small shifts.
- **Full CNN architecture** — conv + pool blocks extract features, then flatten + dense layers classify (Week 6 pattern, applied on top of learned image features).
- **Data augmentation** — random flips/rotations/zooms artificially expand a small dataset, the standard first defense against overfitting in computer vision.
- **Transfer learning** — reuse a model (MobileNetV2) pre-trained on millions of images; freeze its feature-detecting layers and train only a new classification head — the most practical technique for strong results from limited data.

---

## 📂 File Structure
Week7/

└── Day2/

├── Building CNNs & Transfer Learning.ipynb

└── Readme.md

- **Building CNNs & Transfer Learning.ipynb** → Lesson content + full hands-on lab: from-scratch CNN, the same CNN with data augmentation, transfer learning with frozen MobileNetV2, and a three-way comparison table (accuracy, epochs, training time)
- **Readme.md** → Documentation of objectives, learning goals, and file organization

*Dataset reloaded via `kagglehub.dataset_download()`, same as Day 1 — 11,879 train images (split 80/20 into train/validation) and 2,000 test images, near-balanced Benign/Malignant.*

---

## 🧪 Hands-On Lab: Building and Transferring a CNN
1. Build and train a small CNN from scratch (3 conv+pool blocks) and record its test accuracy.
2. Add data augmentation (flip, rotation, zoom) and compare validation loss/accuracy curves to the scratch run.
3. Apply transfer learning with a frozen MobileNetV2 base and compare accuracy and training time to both prior runs.
4. Document which approach performed best and why.

**Tools:** TensorFlow/Keras, Pre-trained models (Keras Applications), Matplotlib, Jupyter/Colab (GPU)

---

## ✅ Key Takeaway

Three approaches tested head-to-head on the same 11,879-image melanoma dataset:

| Approach | Test Accuracy | Epochs | Train Time |
|---|---|---|---|
| From-Scratch CNN | 88.05% | 15 | 100.5s |
| From-Scratch CNN + Augmentation | 89.80% | 18 | 114.7s |
| Transfer Learning (MobileNetV2) | **90.85%** | **7** | **66.9s** |

Transfer learning was the clear winner — highest accuracy, fewest epochs, and fastest training time. Augmentation provided a real but smaller gain (1.75 pp) and visibly reduced overfitting in the validation loss curves, where the scratch CNN showed a sharp loss spike after epoch 13 that the augmented model avoided. MobileNetV2's ImageNet pretraining transferred usefully to dermoscopic images despite the domain gap, confirming transfer learning as the Sprint 2 core architecture.
