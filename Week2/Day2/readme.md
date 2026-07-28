# Day 2: Probability & Randomness

**Focus:** Quantifying uncertainty and independence.

---

## Probability Basics

- **Range:** 0 (impossible) → 1 (certain)
- **Formula:** Favorable ÷ Total outcomes (if equally likely)
- **ML Context:** ML outputs probabilities (e.g., "85% chance of churn")

---

## Law of Large Numbers

> Simulated 10,000 coin flips → heads ≈ 0.5  
> With enough trials, observed frequency → true probability

---

## Normal Distribution

- Sampling 10,000 values (mean=0, std=1) → symmetric bell curve
- Many ML models assume normality → key EDA check