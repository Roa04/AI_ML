# Math Foundations & EDA: Doomscrolling and Sleep Quality

## Project Overview

This project explores the relationship between late-night doomscrolling and sleep quality, serving as the central deliverable for **Week 2** of the BinX Tech AI & Machine Learning Internship Program. It bridges the gap from mathematical foundations (statistics, probability, and linear algebra) to a full Exploratory Data Analysis (EDA) on a real-world dataset.

The primary goal is to answer the question: **Does doomscrolling really wreck your sleep?**

## The Data & The Analysis

The project analyzes a dataset of 1,000 respondents, examining their digital habits and sleep metrics. The EDA process is structured into key areas:

1.  **Descriptive Statistics:**
    - Calculated mean, median, mode, standard deviation, and IQR for core variables like `sleep_hours_per_night`, `bedtime_screen_time_minutes`, and `anxiety_score`.
    - Analyzed the effect of outliers on these statistical measures.

2.  **Probability & Inference:**
    - Applied conditional probability to demonstrate that the likelihood of reporting "Poor" sleep quality is significantly higher for self-identified doomscrollers.
    - This foundational probabilistic analysis suggests a strong association between the habit and sleep disruption.

3.  **Linear Algebra for Prediction:**
    - Demonstrated the core linear algebra operation behind machine learning predictions.
    - A simple linear model (`y = x @ w`) was built to generate a "sleep score" prediction from `bedtime_screen_time` and `caffeine_intake`, showing how ML models perform predictions under the hood.

4.  **Exploratory Data Analysis (EDA):**
    - **Univariate Analysis:** Examined the distribution of all key variables using histograms and box plots to understand their shape, central tendency, and identify outliers.
    - **Bivariate & Correlation Analysis:** Used scatter plots, grouped box plots, and a comprehensive correlation heatmap to find strong, interpretable relationships between digital habits, psychological metrics, and sleep quality. Key findings include:
        - Strong correlation between screen time and sleep latency.
        - Strong correlation between phone checks and night wakeups.
        - Clear links between anxiety/stress levels and poor sleep outcomes.

## Key Findings

- **Doomscrolling and Screen Time:** Higher late-night screen time and more doomscrolling sessions are strongly correlated with reduced sleep hours and increased sleep latency.
- **Psychological Impact:** Higher anxiety and stress scores are directly linked to lower sleep quality scores and more night wakeups.
- **The "Screen Time Ratio":** The proportion of daily screen time that occurs at night was found to be a significant feature, suggesting that timing is just as important as total duration.
- **Outliers are Real:** Many outliers (e.g., >150 minutes of bedtime screen time) represent extreme but highly real user behaviors. A decision was made to keep them in the analysis to maintain data integrity.
- **The Core Relationship:** The conditional probability analysis confirms that doomscrollers are more than three times as likely to report poor sleep quality compared to non-doomscrollers.

## Technologies Used

The project is implemented in Python, utilizing a standard data science stack:

- **`pandas`**: For data manipulation and analysis.
- **`numpy`**: For numerical computations and linear algebra operations.
- **`matplotlib`** & **`seaborn`**: For creating static, high-quality visualizations for the EDA.
- **Jupyter Notebook**: For presenting a narrated, executable analysis.
