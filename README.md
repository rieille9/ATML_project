# 🎲 Snakes and Ladders – Reinforcement Learning Project

*Advanced Topics in Machine Learning – Spring 2025*  
*MSc in Business Analytics – University of Geneva*  
Grade: **21.5 / 20** (including bonus task)

---

## 📌 Overview

This project implements a **custom reinforcement learning environment** inspired by the board game *Snakes and Ladders*, where a single agent aims to reach the goal square while maximizing total reward.

Developed as part of a master-level course, the project models the game as a **Markov Decision Process (MDP)** and solves it using:
- **Dynamic Programming (DP)**: value iteration & policy evaluation  
- **Monte Carlo Simulation**  
- Bonus task: modifying the environment with an extra snake (28 → 14) and analyzing its impact

---

## 🧠 Problem Summary

- Board of 30 squares
- Player starts at square 1 with 0 points
- Each action has a cost and results in movement:
  - Pay 3 pts → move 1 square
  - Pay 1 pt → roll `{1, 2, 3}`
  - Pay 2 pts → roll `{4, 5, 6, 7}`
- Reaching square 30 → +10 pts, game ends  
- Overshooting → reset to square 1 with penalty  
- Snakes: 17→4, 20→6, 24→16  
- Ladders: 5→7, 9→27, 11→29  
- Discount factor: γ = 1

---

## 🚀 Key Features

- 🔁 **Game Environment Class**  
  - `.step(action)` → returns next state & reward  
  - `.reset()` → resets game

- 📊 **Policy Evaluation via DP**  
  - Policies tested:
    - “Step” (always move 1 step)
    - “Roll” (always roll small dice)
    - “Random” (mixed strategy)
  
- 🧭 **Optimal Policy Search**  
  - Value iteration for state-value and action-value functions

- 🎲 **Monte Carlo Simulation**  
  - Estimate value of initial state under each policy

- ✅ **Bonus Task**  
  - Added snake 28→14  
  - Adjusted algorithms and commented on policy changes

