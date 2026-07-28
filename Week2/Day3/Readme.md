# Day 3 — Linear Algebra for ML

**Focus:** Representing data as vectors and matrices, computing dot products, and understanding matrix multiplication.

---

## Learning Objectives

- Represent data samples as vectors and datasets as matrices
- Compute a dot product and explain why it is central to model prediction
- Perform matrix multiplication and reason about resulting shapes

---

## Key Topics

- Why linear algebra is the language of ML
- Vectors: one sample's features
- Matrices: a full dataset (samples × features)
- The dot product and how models predict with it
- Matrix multiplication and the shape-matching rule

---

## Lesson Content

### 3.1 Why Linear Algebra Is the Language of ML

Every dataset in ML is a **matrix**: rows are samples, columns are features. Every model's parameters are **vectors or matrices**, and training is a sequence of matrix operations. You do not need to derive proofs, but you must understand what these objects are and how they combine — because that is literally what a model is doing internally.

### 3.2 Vectors

A **vector** is an ordered list of numbers — in ML, it usually represents one data sample's features, or one row of data. A customer described by age, income, and tenure is a 3-dimensional vector.

### 3.3 Matrices

A **matrix** is a 2D grid of numbers — a full dataset, where each row is a sample vector and each column is a feature. Its shape is `(rows, columns) = (samples, features)`.

### 3.4 The Dot Product

The **dot product** multiplies two vectors element-by-element and sums the result, producing a single number. This is the single most important operation in ML: a linear model's prediction is exactly the dot product of a feature vector and a weight vector, plus a bias. This is precisely how linear and logistic regression (Week 3) compute their output: **prediction = dot product of features and weights + bias**. Understanding the dot product is understanding how these models actually predict.

### 3.5 Matrix Multiplication

**Matrix multiplication** applies the dot product across whole matrices at once, letting a model make predictions for every sample in a dataset in a single operation. The rule: an `(m × n)` matrix times an `(n × p)` matrix gives an `(m × p)` matrix — the **inner dimensions must match**. This is why shape mismatches are the most common error in ML code, and why understanding shapes is essential.