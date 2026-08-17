# Week 5 — Day 2: DBSCAN & Hierarchical Clustering

## 📌 Objective
Compare three clustering methods — **K-Means**, **DBSCAN**, and **Hierarchical Clustering** — on the Mall Customers dataset.  
Understand their strengths, limitations, and recommend the best fit for customer segmentation.

---

## 📂 Dataset
- **Source:** Mall_Customers.csv  
- **Features used:** Age, Annual Income (k$), Spending Score (1–100)  
- **Preprocessing:** StandardScaler applied (mandatory for distance-based algorithms)

---

## 🧪 Steps & Observations

### Step 1 — DBSCAN
- **Parameters:** `eps`, `min_samples`  
- **Findings:**
  - Small `eps` → too much noise, fragmented clusters  
  - Large `eps` → clusters merge together  
  - At `eps=0.5, min_samples=5`: 6 clusters, ~30% points flagged as noise  
- **Observation:** DBSCAN highlights boundary customers but may over‑label them as noise.

---

### Step 2 — Hierarchical Clustering
- **Method:** Ward linkage, dendrogram visualization  
- **Cut strategy:** Using `maxclust=6` produced 6 clusters  
- **Observation:** Matches K-Means cluster count, assigns every customer (no noise).  
- **Advantage:** Shows nested relationships between clusters.

---

### Step 3 — K-Means Baseline
- **Chosen k:** 6 (from Day 1)  
- **Result:** 6 clusters, all customers assigned  
- **Observation:** Clear segmentation, stable structure.

---

### Step 4 — Side-by-Side Comparison
| Method        | Clusters | Noise Points | Notes |
|---------------|----------|--------------|-------|
| K-Means (k=6) | 6        | 0            | All customers assigned |
| DBSCAN        | 6        | 60 (~30%)    | Same structure, but boundary customers flagged as noise |
| Hierarchical  | 6        | 0            | Matches K-Means, shows nested structure |

---

## ✅ Recommendation
- **Best Fit:** **K-Means**  
- **Reasoning:**
  - Produces clear, round, similarly sized clusters.  
  - Assigns every customer to a segment (important for business use).  
  - Hierarchical clustering confirms the same 6‑cluster structure.  
  - DBSCAN is useful for spotting boundary customers but discards too many as noise.

---

## 📊 Final Summary
- **K-Means (k=6):** 6 clusters, all customers assigned.  
- **DBSCAN (eps=0.5, ms=5):** 6 clusters, ~30% noise.  
- **Hierarchical (Ward, k=6):** 6 clusters, all customers assigned.  

➡️ **Conclusion:** All three methods agree on 6 clusters.  
For customer segmentation, **K-Means** is the most practical choice.
