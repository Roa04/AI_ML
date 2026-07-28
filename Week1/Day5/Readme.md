# Day 5: Probability Distributions & Independence

**Focus:** Exploring distributions, randomness, and independence in probability.

---

## Uniform Distribution

- All outcomes are equally likely
- Example: Coin flips, dice rolls
- Useful for simulations and baseline probability checks

---

## Law of Large Numbers

> Simulated 10,000 coin flips → heads ≈ 0.5  
> Shows that with enough trials, observed frequency converges to true probability

---

## Normal (Gaussian) Distribution

- Sampled 10,000 values (mean=0, std=1)
- Histogram: symmetric, bell-shaped, peak at mean, tapering tails
- Important because many ML models assume data is approximately normal
- EDA check: verifying normality helps validate model assumptions

---

## Independence of Events

- Modeled coin flip + card draw (King)
- Hand calc: P(heads ∧ King) = 1/26 ≈ 0.0385
- Simulation (100k trials) ≈ 0.0384 → matches
- Conditional probability: P(heads | King) = 0.5 = P(heads)
- Independence confirmed → card result gives no info about coin outcome

---

## Key Takeaway

Distributions describe how data behaves, simulations confirm theoretical probabilities, and independence means one event doesn't affect another. These are foundational checks before applying ML models.