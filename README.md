# Comprehensive Analysis of Grid World Environment Using Monte Carlo Methods

## Introduction
This project provides a comparative analysis of four Monte Carlo methods applied to a Grid World environment. In this environment, an agent navigates a grid with actions (Up, Right, Left, Down) and faces rewards and penalties based on its actions. The study explores the effectiveness of these algorithms in both deterministic and stochastic settings.

## Problem Formulation
The Grid World environment is characterized as follows:
- **State-Space:** The environment consists of a grid where each cell represents a state. The agent receives rewards based on its actions and must avoid a dangerous state.
- **Action-Space:** The agent can move Up, Right, Left, or Down.
- **Reward Scheme:** 
  - Each step incurs a penalty of -0.1.
  - Reaching the goal state provides a reward of +1.
  - Entering the danger state results in a penalty of -1.

## Solution Overview
We implemented and compared four Monte Carlo algorithms:
- **Monte Carlo With Exploring Starts (On-policy):** Ensures all state-action pairs are visited by starting episodes from various states.
- **Monte Carlo Without Exploring Starts (On-policy):** Uses ε-greedy strategies to balance exploration and exploitation.
- **Monte Carlo Prediction (Off-policy):** Estimates value functions for a target policy using importance sampling.
- **Monte Carlo Control (Off-policy):** Learns optimal policies by adjusting returns to reflect the target policy through importance sampling.

## Evaluation Criteria
Performance was assessed based on:
- **Cumulative Rewards:** Total rewards accumulated over episodes, indicating overall effectiveness.
- **Total Samples to Reach Target Reward:** Measures efficiency in learning to achieve the target reward.
- **Training Time:** Computational time required for convergence.
- **State Values (V(s)):** Accuracy in estimating the value of states.
- **Policy (π(s)):** Effectiveness of the learned policy.

## Results and Discussion

### Deterministic Environment (Noise = 0)
- **Effect of Epsilon:** Higher epsilon values increased exploration, affecting cumulative rewards and training time differently across algorithms.
- **Effect of Gamma:** Influenced the algorithms' ability to manage long-term rewards and convergence.

### Stochastic Environment (Noise = 0.4)
- **Effect of Epsilon:** Increased noise affected all algorithms, with Off-Policy MC Control maintaining relatively stable performance compared to others.

### Comparison Across Environments
- **Deterministic:** Off-Policy MC Control generally performed better, providing higher rewards and faster convergence.
- **Stochastic:** Off-Policy MC Control remained effective despite increased noise, while other algorithms struggled more with uncertainty.

## Conclusion
The project highlights that Off-Policy MC Control is the most reliable across different environments, especially under noisy conditions. It balances exploration and exploitation effectively, making it a robust choice for reinforcement learning tasks.

## How to Run the Code
1. Clone the repository.
2. Install the necessary dependencies using `pip install -r requirements.txt`.
3. Run the Monte Carlo algorithms using the provided scripts.
4. Analyze the results through the output logs and visualizations.

## Authors
- **Amr Mostafa Ibrahim** (TA @ ITCS, Nile University, Cairo , Egypt)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
