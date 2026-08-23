# Week 5 — Day 4: t-SNE & Anomaly Detection

## Dataset
Healthcare Stroke Dataset — 5,110 patient records  
Rare outcome: 249 stroke cases (~4.9%)

---

## Objective
- Visualize high-dimensional patient data using **t-SNE** and compare it to **PCA**.  
- Apply **Isolation Forest** to detect anomalies in unlabeled data.  
- Connect flagged anomalies to rare stroke cases for interpretation.

---

## Lesson Content

### 4.1 — t-SNE for Visualization
- Preserves **local neighborhoods** (points close in high dimensions stay close in 2D).  
- Reveals clusters visually, even when not linearly separable.  
- Axes are **not interpretable** — use for visualization only.  

| | PCA | t-SNE |
|---|---|---|
| Preserves | Global variance | Local neighborhoods |
| Use | Compression + visualization | Visualization only |
| Speed | Fast | Slower |
| Axes | Interpretable | Not meaningful |

### 4.2 — Anomaly Detection
- Identifies points that deviate significantly from the norm.  
- Often unsupervised (rare anomalies, few labels).  
- Stroke dataset is a natural fit: imbalanced outcome (~4.9%).

### 4.3 — Isolation Forest
- Randomly partitions feature space; anomalies are isolated quickly.  
- `contamination` parameter sets expected anomaly fraction.  
- Related to DBSCAN noise detection (Day 2).

---

## Hands-On Lab Steps
1. Load & clean dataset (impute missing `bmi`, encode categoricals).  
2. Scale features.  
3. Apply **t-SNE** and plot clusters (colored by K-Means).  
4. Compare with **PCA** projection.  
5. Run **Isolation Forest** (`contamination=0.05`) and count anomalies.  
6. Visualize anomalies on t-SNE plot.  
7. Inspect flagged patients and hypothesize why they were isolated.  
8. Cross-check anomalies against true stroke labels.  

---

## Key Insights
- **t-SNE vs PCA:** PCA’s 2D projection smears clusters; t-SNE reveals distinct islands.  
- **Isolation Forest:** ~5% of patients flagged as anomalies, close to stroke prevalence.  
- **Cross-check:** Partial overlap with stroke cases — anomalies ≠ diagnosis.  
- **Takeaway:**  
  - t-SNE is for visualization only.  
  - Isolation Forest surfaces unusual feature combinations, not labels.  
  - Anomaly detection is a starting point for investigation, not a final tool.

---

## Optional Enrichment
- **t-SNE sensitivity:** Show how changing `perplexity` alters cluster layout.  
- **Anomaly scores:** Plot Isolation Forest score distribution.  
- **DBSCAN comparison:** Overlay DBSCAN noise points vs Isolation Forest anomalies.

---

## Final Summary
Day 4 demonstrates how **unsupervised methods** (t-SNE, Isolation Forest) help explore structure and outliers in complex, imbalanced datasets. They provide **visual and statistical clues**, but require careful interpretation and validation against real labels.
