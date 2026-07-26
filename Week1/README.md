# Week 1 — Python & Data Science Foundations
**BinX Tech — AI & Machine Learning Internship Program**
Phase 1 · Week 1 of 10 · 40 hours · 5 training days

Setting up a professional Python data-science environment and building fluency in the four
libraries every AI/ML workflow is built on: **NumPy** (numerical arrays), **Pandas** (tabular
data), **Matplotlib** (visualization) — all inside the **Jupyter Notebook** workflow.

---

## Overview

| | |
|---|---|
| **Week** | Week 1 of 10 — Phase 1: Foundations |
| **Total hours** | 40 hrs (full-time) / 20 hrs (part-time, Weeks 1–2 combined) |
| **Format** | On-site / Remote / Hybrid — all work in Jupyter notebooks committed to GitHub |
| **Focus** | Python environment setup, NumPy arrays, Pandas DataFrames, Matplotlib plotting, Jupyter workflow |
| **Mentor supervision** | Daily check-in with assigned ML mentor; environment verified before hands-on work begins |

## Learning Objectives

- Set up a professional, reproducible Python data-science environment (venv/conda, pip, Jupyter) reused for the entire 400-hour program.
- Write clean, idiomatic Python: data types, control flow, functions, list comprehensions, and basic OOP.
- Create, index, slice, and vectorize computations over NumPy arrays instead of using slow Python loops.
- Load, inspect, clean, filter, and aggregate tabular data with Pandas DataFrames.
- Produce clear line, scatter, bar, and histogram plots with Matplotlib to explore and communicate data.
- Work fluently in the Jupyter Notebook environment and commit a well-structured notebook to GitHub.

## Daily Schedule

| Day | Hours | Topic Focus |
|---|---|---|
| Day 1 | 8 hrs | Environment setup (Python, venv/conda, pip, Jupyter, VS Code, Git); Jupyter workflow |
| Day 2 | 8 hrs | Python for data science: data types, control flow, functions, list comprehensions, OOP basics |
| Day 3 | 8 hrs | NumPy: array creation, indexing/slicing, broadcasting, vectorized operations |
| Day 4 | 8 hrs | Pandas: Series & DataFrames, loading data, inspection, selection, cleaning, groupby |
| Day 5 | 8 hrs | Matplotlib: line/scatter/bar/histogram plots, subplots, labeling; Week 1 mini-notebook |

---

## What To Do Each Day

### Day 1 — Environment Setup & the Jupyter Workflow
Set up a reproducible Python environment and get comfortable with the notebook workflow.
- Create and activate a virtual environment, then install `numpy`, `pandas`, `matplotlib`, `jupyter`.
- Launch Jupyter and create a notebook mixing at least one Markdown cell and one code cell.
- Run a code cell that prints the installed version of each library to confirm the setup.
- Freeze the environment to `requirements.txt`.
- Initialize a Git repository, commit the notebook and `requirements.txt`, and push to GitHub.

### Day 2 — Python for Data Science
Drill core Python fundamentals used constantly in data work.
- Write a function that takes a list of numbers and returns the mean, min, and max as a dictionary.
- Rewrite a given `for` loop that filters even numbers as a single list comprehension.
- Define a small class representing a data record with at least two attributes and one method.
- Document each cell with a Markdown explanation of what it does and why.

### Day 3 — NumPy: Numerical Computing
Get fluent with array creation, indexing, and vectorization.
- Create a 2D array of shape `(4, 4)` filled with values 1–16 and print its shape and dtype.
- Use slicing to extract the second column and the last row.
- Use a boolean mask to select all values greater than the array's mean.
- Add a 1D row array to every row of a 2D array using broadcasting, and verify the result manually.

### Day 4 — Pandas: Tabular Data
Load, clean, filter, and aggregate a real dataset.
- Load a provided CSV dataset into a DataFrame and report its shape, columns, and dtypes.
- Count missing values per column and handle them (fill or drop) with a documented justification.
- Filter the data to a meaningful subset (e.g. rows above a threshold) and describe what you find.
- Use `groupby` to compute an aggregate statistic per category and interpret the result in a Markdown cell.

### Day 5 — Matplotlib & Week 1 Mini-Notebook
Bring NumPy, Pandas, and Matplotlib together into one pipeline.
- Load and clean a provided dataset with Pandas (handling any missing values).
- Use NumPy to compute at least one derived numeric feature or summary statistic.
- Produce at least three labeled plots (including a histogram and a scatter plot) exploring the data.
- Write Markdown cells explaining what each visualization reveals about the data.
- Commit the finished notebook and its `requirements.txt` to GitHub with a clear commit message.

---

## Week 1 Deliverables

By the end of Week 1, submit the following to your mentor and this GitHub repository:

- [ ] A reproducible Python environment with a committed `requirements.txt`
- [ ] A Python fundamentals notebook (functions, list comprehensions, a small class) with Markdown documentation
- [ ] A NumPy notebook demonstrating array creation, slicing, boolean masking, and broadcasting
- [ ] A Pandas notebook loading, cleaning, filtering, and aggregating a real dataset
- [ ] The Week 1 integrated mini-notebook (NumPy + Pandas + Matplotlib) with at least three labeled plots
- [ ] All Week 1 notebooks committed to this repository with clear commit messages

## Suggested Repo Structure

```
Week1/
├── README.md
├── requirements.txt
├── Day1/
│   └── day1_environment_setup.ipynb
├── Day2/
│   └── day2_python_fundamentals.ipynb
├── Day3/
│   └── day3_numpy.ipynb
├── Day4/
│   └── day4_pandas.ipynb
└── Day5/
    └── day5_matplotlib_mini_notebook.ipynb
```

## Technical Stack

| | |
|---|---|
| Language | Python 3.10+ |
| Environment | venv / conda, pip, `requirements.txt` |
| Numerical computing | NumPy |
| Tabular data | Pandas |
| Visualization | Matplotlib |
| Workflow | Jupyter Notebook, VS Code, Git & GitHub, Google Colab |
