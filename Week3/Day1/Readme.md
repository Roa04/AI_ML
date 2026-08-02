# 📘 Week 3 - Day 1: Supervised Learning & Scikit-learn

Kicked off Phase 2 today — the first real step into machine learning after 
two weeks of Python practice and EDA basics. The focus was on grasping the 
theory before diving into actual models.

---

## 📚 Supervised Learning

The idea is simple: the model learns from **labeled data** — examples that 
already have the correct answers attached. Think of it like studying with 
an answer key. Once trained, the model can predict answers for new data it 
hasn’t seen before.

Two main types:
- 📈 **Regression** — predicts a continuous value (price, temperature, income)  
- 🏷️ **Classification** — predicts a category (spam/not spam, disease type, churn/stay)

---

## 🎯 Features and Target

- 🔹 **X** = input columns (features)  
- 🔹 **y** = the column we want to predict (target)  

The entire task of supervised learning is to uncover the relationship 
between `X` and `y`.

---

## 🤖 Scikit-learn Workflow

Every model in Scikit-learn follows the same 4-step workflow:

1. ⚙️ **Instantiate** — create the model  
2. 🏋️ **Fit** — train it on the training data  
3. 🔮 **Predict** — make predictions on new data  
4. 📊 **Score** — evaluate performance  

This consistency makes it easy to switch between models later.

---

## ✂️ Train/Test Split

Golden rule: **never test the model on the same data it trained on**.  
Otherwise, it can just memorize answers and look perfect without truly 
learning. Splitting the dataset (80% train / 20% test) gives a realistic 
measure of how the model performs on unseen data.

Used `random_state=42` to keep the split reproducible.

---

## 🧪 Hands-On Lab

Applied the workflow on the Iris dataset:

- 📥 Loaded the dataset  
- ✂️ Separated into X (features) and y (target)  
- 🔀 Performed an 80/20 train/test split  
- ✅ Checked the shapes to confirm consistency  
- 💭 Wrote down why the test set must remain hidden during training  

---

## 🌸 Dataset

**Iris Dataset** — flower measurements (sepal length, sepal width, petal 
length, petal width) with species labels (*setosa, versicolor, virginica*).  
Used here just to practice the ML workflow, no model training yet.

---

## 🛠️ Tools

- Python  
- Pandas  
- Scikit-learn  
- Jupyter Notebook  
