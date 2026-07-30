# Day 5 — EDA Part 2: Correlation & Data Storytelling

## Overview

This repository contains two Jupyter notebooks that demonstrate bivariate analysis, correlation analysis, and data storytelling techniques as a continuation of Day 4's univariate EDA work. The notebooks cover scatter plots, grouped box plots, correlation heatmaps, pairplots, and assembling a fully narrated EDA notebook.

---

## Files in This Repository

### 1. `EDA_Part_2.ipynb`

**Dataset:** Healthcare Stroke Dataset (`healthcare-dataset-stroke-data.csv`)

This notebook serves as the primary instructional material for Day 5 EDA concepts. It walks through:

- Loading the dataset and checking for missing values with `df.isnull().sum()`
- Imputing missing `bmi` values with the column mean
- Bivariate analysis using scatter plots and grouped box plots
- Correlation matrix computation and heatmap visualization
- A markdown note distinguishing correlation from causation
- Two `sns.pairplot()` calls to scan relationships across the dataset

**Key Skills Demonstrated:**
- Loading and cleaning the stroke dataset
- Creating a scatter plot of `age` vs `bmi`
- Creating a grouped box plot of `avg_glucose_level` by `gender`
- Computing `df.corr(numeric_only=True)` and rendering it with `sns.heatmap(annot=True, cmap="coolwarm")`
- Running `sns.pairplot()` with `hue="age"` and again with `hue="stroke"`

---

### 2. `Full_EDA.ipynb`

**Dataset:** Sleep & Doomscrolling Habits Dataset (`sleep_doomscrolling_habits.csv`)

This hands-on lab provides practical application of bivariate and correlation analysis on a real dataset. The notebook follows the lab's structured steps, then repeats the full pipeline a second time as an "assembled" narrated notebook.

#### Step 1: Scatter Plots and Grouped Box Plots
- Built a 2×3 grid of scatter plots for six selected variable pairs (e.g. `total_daily_screen_time_hours` vs `sleep_hours_per_night`, `anxiety_score` vs `sleep_quality_score`)
- Built a 3×2 grid of grouped box plots (e.g. `sleep_hours_per_night` by `sleep_quality_category`, `anxiety_score` by `doomscroller` status)

#### Step 2: Correlation Matrix and Heatmap
- Computed the full correlation matrix with `df.corr(numeric_only=True)`
- Rendered it as a large annotated heatmap (`figsize=(20, 16)`, `cmap='coolwarm'`)

#### Step 3: Strongest Relationships
- Unstacked the correlation matrix, filtered out self-correlations, and extracted the top 5 strongest pairwise correlations
- Documented implications in markdown, including a recommendation to combine highly correlated features (e.g. `bedtime_screen_time_minutes` and `doomscroll_sessions_per_night`, r ≈ 0.79) to avoid multicollinearity in a future model

#### Step 4: Assembled EDA Notebook
- Re-ran the entire pipeline from scratch: dataset summary, `df.info()`/`df.describe()`, missing-value check and imputation, numeric distribution grid, categorical distribution grid, IQR-based outlier scan, bivariate scatter/box grids, correlation heatmap, and top-5-correlation extraction
- Closed with an "Overall Summary & Next Steps" markdown section covering data quality, distribution shape, and modeling recommendations

#### Step 5: Documentation
Markdown cells throughout explaining:
- Distribution skew and its modeling implications
- Outlier detection findings and interpretation
- Correlation strength and what it implies for feature engineering

---

## Learning Objectives Achieved

### 1. Perform Bivariate Analysis with Scatter Plots and Grouped Box Plots

| Plot Type | Seaborn Function | Reveals |
|-----------|------------------|---------|
| Scatter Plot | `sns.scatterplot()` | Relationship between two numeric variables |
| Grouped Box Plot | `sns.boxplot()` | How a numeric variable differs across categories |

### 2. Compute and Interpret a Correlation Matrix and Heatmap
- Calculate pairwise correlation with `df.corr(numeric_only=True)`
- Visualize with `sns.heatmap(annot=True, cmap="coolwarm")`
- Understand the -1 to +1 scale and what each end represents

> **Key Principle:** Correlation is not causation — two variables moving together does not mean one causes the other. EDA identifies relationships; it never proves cause.

### 3. Assemble a Complete, Narrated EDA Notebook on a Real Dataset
- Combine descriptive statistics, univariate distributions, outlier handling, bivariate relationships, and correlation analysis into one notebook
- Wrap each stage in markdown narrative explaining what was found and what it implies for modeling

---

## Key Takeaways

1. **Bivariate analysis surfaces relationships** that univariate analysis on its own cannot show
2. **Correlation heatmaps** are one of the most information-dense charts in EDA — but require correct handling of `hue` and grouping variables to be meaningful
3. **Pairplots** are a fast way to scan an entire dataset's relationships before deciding where to look closer
4. **A full EDA notebook** should read as a narrative, not just a sequence of plots
5. **Repetition across notebook sections should be intentional** — rerunning the same pipeline without building on prior steps adds length without adding insight

---

## Tools Used

| Tool | Purpose |
|------|---------|
| **Seaborn** | Statistical data visualization |
| **Pandas** | Data manipulation and analysis |
| **Matplotlib** | Plotting and visualization |
| **Jupyter Notebook** | Interactive development environment |
| **Git & GitHub** | Version control and submission |

---

## Summary

| Aspect | Stroke Dataset (`EDA_Part_2.ipynb`) | Sleep/Doomscrolling Dataset (`Full_EDA.ipynb`) |
|--------|--------------------------------------|--------------------------------------------------|
| **Bivariate Plots** | 1 scatter plot, 1 grouped box plot | 6 scatter plots, 5 grouped box plots |
| **Correlation Heatmap** | Yes, single pass | Yes, computed twice (lab pass + assembled pass) |
| **Pairplot** | Yes — `hue="age"` and `hue="stroke"` | Not used |
| **Outlier Detection** | Not performed in this notebook | IQR method across 18 numeric columns |
| **Structure** | Linear lesson walkthrough | Lab steps followed by a full duplicate "assembled" run |

---

**Learning Objectives:**
- Perform bivariate analysis with scatter plots and grouped box plots
- Compute and interpret a correlation matrix and heatmap
- Assemble a complete, narrated EDA notebook on a real dataset