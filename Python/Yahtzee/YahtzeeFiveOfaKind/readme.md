# 🎲 Yahtzee (5 of a Kind) — Monte Carlo Probability Simulation in Python

## 📌 Overview

This project explores a classic question from the game **Yahtzee**:

**What is the probability of rolling a 5 of a kind (“Yahtzee”) within a single turn of three rolls?**

Instead of solving this purely through mathematical formulas, I use **Python simulations** to model thousands of Yahtzee turns and estimate the probability empirically. This approach is known as a **Monte Carlo Simulation**, where randomness is used to approximate real-world outcomes.

Beyond the math, this project also highlights something important:  
**data analysis and probability don’t always have to be serious or business-focused.** They can also be applied to games, curiosity-driven questions, and everyday randomness in a way that makes analytical thinking more intuitive, visual, and enjoyable.

**View the full analysis:**  [yahtzeeRoll.ipynb](./yahtzeeRoll.ipynb)

**Static HTML version (no scrolling lag):** [yahtzeeRoll.html](./yahtzeeRoll.html)

---

## Objective

- Simulate a full Yahtzee turn (up to 3 rolls of 5 dice)
- Apply a simple decision strategy (keep the most frequent number)
- Estimate the probability of achieving Yahtzee
- Visualize outcomes and convergence behavior
- Demonstrate Monte Carlo simulation in a clear, interpretable way

---

## Key Concepts

### Monte Carlo Simulation
A method that uses repeated random sampling to estimate probabilities.  
The name comes from the **Monte Carlo Casino in Monaco**, reflecting its reliance on randomness and chance.

### Probability Estimation
Instead of calculating exact probabilities analytically, we simulate many outcomes and use:
- Success rate = successful outcomes / total simulations

### Strategy-Based Simulation
This model does not just roll dice randomly—it simulates a **basic player strategy**:
- Keep the number that appears most frequently
- Re-roll remaining dice
- Repeat for up to three rolls

---

## Tools & Libraries

- Python 3
- `random` — simulate dice rolls
- `numpy` — numerical calculations
- `matplotlib` — data visualization

---

## What the Simulation Shows

The project generates insights such as:

- Probability of rolling a Yahtzee in one turn (~4–5%)
- How results stabilize over time (convergence behavior)
- Distribution of starting hands (how often you begin close to success)
- Impact of early roll strength on final outcomes

---

## Visualizations Included

- Distribution of dice rolls (fairness check)
- Starting match strength (how good first rolls are)
- Success vs failure outcomes
- Monte Carlo convergence curve
- Probability by starting roll quality

These visuals help turn abstract probability into something **intuitive and observable**.

---

## Why This Project Matters

While Yahtzee is just a game, the same techniques used here apply to real-world problems such as:

- Risk modeling
- Forecasting uncertain outcomes
- Decision-making under uncertainty
- Simulation-based business analysis

At the same time, this project reinforces an important idea:

> Data analysis isn’t only about business dashboards or financial models — it can also be a creative way to explore games, curiosity, and randomness in the world around us.
