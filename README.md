# Q-Learning vs SARSA: Reinforcement Learning Comparison

## Introduction
This repository offers a comparative study of **Q-learning (Off-Policy)** and **SARSA (On-Policy)**, two foundational algorithms in Reinforcement Learning (RL). 

Rather than just implementing code, this project visually demonstrates how an agent's policy updates fundamentally change its risk tolerance and pathfinding behavior under identical environmental conditions.

## Key Features
- **Algorithm Benchmarking**: Side-by-side comparison of Q-learning and SARSA in classic RL environments (e.g., OpenAI Gymnasium's Cliff Walking).
- **Risk-Aversion Analysis**:
  - **Q-learning**: Visualizes the aggressive pursuit of the theoretical optimal path (walking directly along the cliff edge).
  - **SARSA**: Visualizes a conservative, safer path choice to minimize penalties from random exploration errors.
- **Performance Visualization**: Automatically generates training metrics, including cumulative reward plots and convergence rates per episode.

## Getting Started

### 1. Prerequisites & Installation
This project requires Python 3.8 or higher.
```bash
git clone [https://github.com/your-username/q-learning-sarsa.git](https://github.com/your-username/q-learning-sarsa.git)
cd q-learning-sarsa
pip install -r requirements.txt

# Run both algorithms simultaneously and output the visual comparison
python main.py --compare

---

## The Core Essence & What Most Beginners Miss

### 1. The Core Difference (The Personality Analogy)
Both algorithms share the same goal: finding the best map (Q-table) to get the highest score. However, their core "personalities" are entirely different:
* **Q-learning (The Bold Explorer)**: It assumes it will act perfectly in the future. It targets the absolute shortest route, even if one wrong step means falling off a cliff. 
* **SARSA (The Realistic Pragmatist)**: It acknowledges its own flaws. It knows it might still make random mistakes (exploration) and take a wrong step, so it deliberately chooses a longer, safer route to stay clear of danger.

Reviewers look for this understanding. Framing your repository around **"Optimality (Off-policy) vs. Safety (On-policy)"** immediately makes it stand out.

### 2. Elevating the Project Credibility
Simply writing the mathematical formulas in code looks like a basic homework assignment. To look professional, you must specify the benchmark environment. Explicitly mentioning the **Cliff Walking** environment in your description proves you understand exactly *why* these two algorithms are being compared, as it is the golden standard for highlighting the Q-learning vs. SARSA behavioral split.

---

## Three Questions to Deepen Understanding

1. Once training is 100% complete and exploration stops, how exactly will the final paths chosen by Q-learning and SARSA differ in the Cliff Walking environment?
2. If the exploration rate (epsilon) is kept high and never decays, which of the two algorithms will suffer a worse cumulative reward during training, and why?
3. This project uses a *Tabular* approach, meaning it only works when states are distinct and finite. How would you scale these algorithms to handle infinite, continuous environments like autonomous driving or robotics?
