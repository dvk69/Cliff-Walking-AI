# Cliff Walking: SARSA vs. Q-Learning

A reinforcement-learning study of the classic cliff-walking problem. The project implements the environment and both learning methods from scratch, then compares the routes learned by an on-policy agent (SARSA) and an off-policy agent (Q-learning).

## Problem setup

The environment is a 4 × 12 grid:

- The agent starts at the lower-left cell.
- The goal is the lower-right cell.
- Moving onto a normal cell produces a reward of `-1`.
- Falling from the cliff produces a reward of `-100` and ends the episode.
- Actions are selected with an epsilon-greedy policy during training.

## What the experiment compares

| Method | Learning style | Behavior observed in the saved notebook run |
|---|---|---|
| Q-learning | Off-policy | Learns the shorter route along the row immediately above the cliff |
| SARSA | On-policy | Learns a longer route with more distance from the cliff |

Both agents are trained for 500 episodes with an exploration rate of 0.1 and a learning rate of 0.1. The final routes are generated with exploration disabled.

## Repository contents

- `6612_CliffWalking_FinalProject.ipynb` — environment, agents, training and route comparison
- `6612_Final_Project_Cliff_Walking_.pptx` — project presentation
- `Cliff Walking Readme.md` — original project notes

## Run the notebook

### Requirements

- Python 3
- NumPy
- Jupyter Notebook or JupyterLab

```bash
pip install numpy jupyter
jupyter notebook 6612_CliffWalking_FinalProject.ipynb
```

Run the notebook from top to bottom to build the grid, train both agents and print their learned routes.

## Notes on reproducibility

The notebook does not set a random seed, so the number of cliff falls and the exact training trace can vary between runs. The saved outputs document one completed experiment.

## Possible extensions

- Track reward per episode and plot learning curves
- Run multiple random seeds and report mean performance
- Add a decaying exploration schedule
- Compare convergence speed and cumulative online reward
- Separate the environment and agent classes into reusable Python modules

## Purpose

This is an educational implementation intended to demonstrate the practical difference between on-policy and off-policy temporal-difference learning.
