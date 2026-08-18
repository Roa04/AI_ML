# Week 5 — Day 3: Dimensionality Reduction with PCA

**Dataset:** Mall Customers (same as Days 1–2)
**Task:** Apply PCA to reduce dimensions, analyze explained variance, and visualize clusters in reduced space.

---

## Objective

Understand why high-dimensional data is harder to work with, learn what PCA does and how to read explained variance, and apply it to reduce and visualize the Mall Customers dataset.

---

## Lesson Content

### 3.1 — The Curse of Dimensionality
- Data becomes sparse in high-dimensional space.
- Models overfit more easily with many features.
- Visualization is impossible beyond three dimensions.
- Dimensionality reduction compresses features into fewer dimensions while keeping as much information as possible.

---

### 3.2 — What PCA Does
- PCA finds new axes (**principal components**) that capture the greatest variance.
- PC1 captures the most variance, PC2 the next most, and so on.
- By keeping only the first few components, you reduce dimensions while retaining most of the information.
- Each component is a linear combination of the original features.

```python
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler

X_scaled = StandardScaler().fit_transform(X)
pca = PCA(n_components=2)
X_pca = pca.fit_transform(X_scaled)
```

---

### 3.3 — Explained Variance
- The **explained variance ratio** shows how much of the dataset’s information each component captures.
- Summing these values tells you how much total variance is retained.
- Always scale features before PCA to avoid misleading results.

```python
print(pca.explained_variance_ratio_)
print(pca.explained_variance_ratio_.sum())
```

---

### 3.4 — When to Use PCA
| Use PCA when | Avoid PCA when |
|--------------|----------------|
| Features are correlated or redundant | Features are already few and independent |
| You need a 2D/3D visualization | Interpretability of individual features matters |
| Model is slow or overfitting | Dataset is small — variance estimates may be unstable |

---

## Hands-On Lab: Reducing Dimensions with PCA

### Steps
1. Load and prepare the dataset.
2. Scale features with `StandardScaler`.
3. Apply PCA to reduce to 2 components.
4. Analyze variance retained.
5. Find minimum components for ~95% variance.
6. Plot cumulative explained variance.
7. Visualize in 2D, coloring by K-Means clusters (Day 1).
8. Document what PCA preserved and what it cost.

---

### Key Observations
- **2 components retain 77.1% variance** (PC1 = 44.1%, PC2 = 33.0%).
- **All 3 components are needed** to reach ~95% variance.
- With only 3 independent features (Age, Income, Spending Score), PCA cannot compress without losing information.
- The 2D PCA plot still shows clear cluster separation, confirming that most cluster-relevant information lives in the first two components.

---

## PCA Results & Trade-Offs

**Preserved:**
- 77.1% of variance in 2D reduction.
- Clear separation of customer clusters.
- Main axes: income and age/spending trade-off.

**Cost:**
- 22.9% variance lost in 2D reduction.
- Lost variation separates customers with similar income/spending but different ages.
- Original feature names replaced by PC1/PC2 combinations.

---

## Final Takeaway
- PCA provided a practical way to visualize the Mall Customers dataset in 2D.
- No compression is possible without losing variance — all 3 components are required for ~95% retention.
- This limitation comes from having only 3 independent features.
- PCA’s compression benefits are most visible on **high-dimensional, correlated datasets** (e.g., images, text embeddings), where a small fraction of components can capture most of the variance.