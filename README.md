# Windy Gridworld Environment with Monte Carlo Control

This repository contains the implementation of a Windy Gridworld environment and the application of the Monte Carlo Control algorithm for reinforcement learning. The Windy Gridworld is a standard environment used in reinforcement learning to test various algorithms. The environment includes a grid with a specified wind effect that influences the agent's movement. The goal is to learn an optimal policy that navigates the agent from a start position to a goal position efficiently, despite the wind's influence.

## Environment: WindyGridWorld

The `WindyGridWorld` class defines the environment. It is characterized by:

- A grid shape, by default 7x10.
- A start position and a goal position.
- A wind effect specified for each column in the grid, influencing the agent's movement vertically.

Actions available to the agent are:
- Right
- Left
- Up
- Down

The wind effect is applied vertically (upward) as the agent moves, altering its intended path.

## Monte Carlo Control

The `MonteCarloControl` class implements the Monte Carlo method for learning an optimal policy over a specified number of episodes. It employs exploration-exploitation balancing through an epsilon-greedy strategy. The algorithm updates the action-value function based on the cumulative rewards received, adjusting the policy towards more rewarding actions over time.

### Key Parameters:
- `episodes`: The number of episodes to run the Monte Carlo simulation.
- `epsilon`: The probability of choosing an exploration action, to balance between exploration and exploitation.
- `gamma`: The discount factor for future rewards.

## Visualization

The implementation includes visualization of:
- State values as a heatmap, showing the maximum Q-value at each state.
- Q-values for each state-action pair, allowing for insight into the action-value function learned by the Monte Carlo Control algorithm.

## Usage

To use this code, ensure you have `numpy` and `matplotlib` installed for numerical operations and visualizations, respectively.

1. Create an instance of the `WindyGridWorld` environment.
2. Initialize the `MonteCarloControl` with the environment.
3. Run the Monte Carlo Control algorithm to learn Q-values.
4. Visualize the state values and Q-values for insight into the learned policy and value function.

This implementation serves as an educational tool for understanding the basics of reinforcement learning in a discrete state and action space environment, showcasing the Monte Carlo Control algorithm's application.
