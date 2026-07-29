# Day 4 — EDA Part 1: Distributions & Outliers

## Overview

This repository contains two Jupyter notebooks that demonstrate Exploratory Data Analysis (EDA) techniques for understanding data distributions, detecting outliers, and preparing datasets for machine learning modeling. The notebooks cover univariate analysis using histograms, box plots, count plots, KDE plots, and the IQR method for outlier detection.

---

## Files in This Repository

### 1. `eda_day4.ipynb`

**Dataset:** Diamonds Dataset (Seaborn built-in dataset)

This notebook serves as the primary instructional material for Day 4 EDA concepts. It walks through:

- The importance of EDA as a prerequisite for modeling
- Seaborn visualization techniques
- Univariate analysis with histograms, box plots, count plots, and KDE plots
- IQR method for outlier detection

**Key Skills Demonstrated:**
- Loading and exploring the diamonds dataset
- Creating histograms to visualize numeric distributions (carat, price, depth)
- Using box plots to identify medians, quartiles, and outliers
- Creating count plots for categorical variables
- Implementing IQR calculations to flag outliers in the price column
- Documenting findings and making decisions about outlier handling

---

### 2. `Hands_on_lab_d4w2.ipynb`

**Dataset:** Tips Dataset (Seaborn built-in dataset)

This hands-on lab provides practical application of EDA techniques on a real dataset. The notebook follows a structured workflow:

#### Step 1: Histograms for Numeric Variables
- Created histograms for total_bill, tip, and size
- Observations: Right-skewed distributions with long tails

#### Step 2: Box Plots for Outlier Detection
- Visual identification of outliers using box plots
- All three numeric variables showed outliers beyond the upper whisker

#### Step 3: IQR Method Implementation
- Applied the 1.5×IQR rule to flag outliers

**Outlier Results:**

| Column | Outliers Count | Values | Decision |
|--------|---------------|--------|----------|
| total_bill | 9 | $40–51 | Kept — large but plausible bills |
| tip | 9 | $5.92–$10.00 | Kept — consistent with large bills |
| size | 9 | Parties of 5+ | Kept — valid group sizes |

**Decision:** No rows removed. All flagged values are legitimate data points, not errors.

#### Step 4: Count Plots for Categorical Variables
- Analyzed sex, smoker, day, and time distributions

**Class Imbalance Identified:**

| Variable | Distribution | Imbalance Level |
|----------|--------------|-----------------|
| day | Sat: 87, Sun: 76, Thur: 62, Fri: 19 | Significant |
| time | Dinner: 176, Lunch: 68 | Moderate |
| sex | Male: 157, Female: 87 | Mild |
| smoker | No: 151, Yes: 93 | Mild |

**Recommendation:** Stratify on day for train/test splits to avoid test sets with too few Friday records.

#### Step 5: Documentation
Comprehensive markdown cells explaining:
- Distribution shapes and their implications
- Outlier detection results and handling decisions
- Class imbalance observations and recommendations

---

## Learning Objectives Achieved

### 1. Explain Why EDA Is Required Before Modeling
- EDA reveals data structure, distributions, relationships, and problems
- Catches data issues that would corrupt downstream results
- "A model can only be as good as the understanding behind it"

### 2. Perform Univariate Analysis Using Seaborn Visualizations

| Plot Type | Seaborn Function | Reveals |
|-----------|------------------|---------|
| Histogram | `sns.histplot()` | Shape of numeric variable distribution |
| Box Plot | `sns.boxplot()` | Median, quartiles, and outliers |
| Count Plot | `sns.countplot()` | Frequency of each category in a categorical variable |
| KDE Plot | `sns.kdeplot()` | Smoothed estimate of distribution shape |

### 3. Detect Outliers Using the IQR Method
- Calculate Q1, Q3, and IQR
- Define upper and lower bounds using the 1.5×IQR rule
- Flag and evaluate outliers
- Make informed decisions (keep, cap, or remove)

> **Key Principle:** "An outlier is a question, not a verdict. Investigate whether it is a real value or an error before deciding to keep, cap, or remove it. Never delete outliers silently."

---

## Key Takeaways

1. **EDA is not optional** — It's the most critical step before modeling
2. **Multiple visualization types** reveal different aspects of data:
   - Histograms show overall distribution shape
   - Box plots highlight outliers and quartiles
   - Count plots reveal categorical imbalances
   - KDE plots provide smooth density estimates
3. **Outliers require investigation** — Not all outliers are errors
4. **Class imbalance matters** — Especially for rare categories
5. **Never delete outliers silently** — Always document decisions

---

## Tools Used

| Tool | Purpose |
|------|---------|
| **Seaborn** | Statistical data visualization |
| **Pandas** | Data manipulation and analysis |
| **Matplotlib** | Plotting and visualization |
| **Jupyter Notebook** | Interactive development environment |


---

## Summary

| Aspect | Diamonds Dataset | Tips Dataset |
|--------|------------------|--------------|
| **Variables Analyzed** | carat, price, depth, table | total_bill, tip, size |
| **Outliers Detected** | 3,540 in price column | 9 per numeric column |
| **Outlier Decision** | Investigate individually | All kept (legitimate values) |
| **Class Imbalance** | Noted in categorical cuts | Most severe in day |
| **Recommended Action** | Investigate outliers before modeling | Stratify on day for splitting |

---

**Learning Objectives:**
- Explain why EDA is a required first step before modeling
- Perform univariate analysis using Seaborn histograms, box plots, and count plots
- Detect outliers using the IQR method and decide how to handle them