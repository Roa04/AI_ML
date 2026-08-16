# Week 5 — Day 1: Unsupervised Learning & K-Means Clustering

In Weeks 3–4, we focused on **supervised learning**, where models learn from labeled data to predict known outcomes.  
Now, in Week 5, we shift gears to **unsupervised learning** — exploring datasets without labels to uncover hidden patterns and natural groupings.  

This day’s lab uses the **Mall Customers dataset** to apply **K-Means clustering**, helping us discover customer segments that can guide business decisions such as marketing, loyalty programs, and re‑engagement strategies.

## 📌 Objective
Transition from supervised to unsupervised learning.  
Apply **K-Means clustering** to discover natural groupings in customer data, choose the right number of clusters using the **elbow method** and **silhouette score**, and interpret what each cluster represents in business terms.

### Learning Goals
- Understand the difference between supervised and unsupervised learning  
- Apply K-Means clustering to the Mall Customers dataset  
- Use the elbow method to shortlist candidate k values  
- Confirm the best k using silhouette score  
- Visualize and interpret customer segments for actionable insights  

---

## 📂 File Structure

Week5/

└── Day1/

├── Mall_Customers.csv

├── Unsupervised Learning & K-Means.ipynb

└── Readme.md



- **Mall_Customers.csv** → Dataset with customer demographics and spending behavior  
- **Unsupervised Learning & K-Means.ipynb** → Jupyter notebook with lesson content, hands‑on lab, and clustering workflow  
- **Readme.md** → Documentation of objectives, learning goals, and file organization  

---

## 🧪 Hands-On Lab Overview
1. Load and scale the dataset (Age, Annual Income, Spending Score).  
2. Apply the **Elbow Method** to identify candidate k values.  
3. Compute **Silhouette Scores** to confirm the best k.  
4. Fit final K-Means model with chosen k.  
5. Visualize clusters and interpret customer segments.  

---

## ✅ Key Takeaway
The combination of **elbow method** (visual heuristic) and **silhouette score** (quantitative check) ensures a balanced, data-driven choice of k.  
Clusters reveal actionable customer segments — e.g., high-income/high-spending customers for loyalty programs, or high-income/low-spending customers for re-engagement strategies.
