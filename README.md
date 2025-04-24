# Chrome Dino-Game Solver

_Made by Satvik, Harsh, Aryaman Pravesh, and Bharadwaj for the "Introduction to Machine Learning" course_

<p align="center">
  <img width="auto" height="500px" src="presentation_visuals/dino_game_example.gif"/>
</p>

This project implements an AI bot that learns to play Chrome's _No-Internet Dinosaur Game_ using two distinct approaches: a heuristic rule-based bot and a deep reinforcement learning bot.

---

## Overview of Models

### 1. Heuristic Bot
- Uses predefined rules based on obstacle distance and speed.
- Decides to jump when an obstacle is within a threshold distance.
- Thresholds are optimized using grid search to achieve high performance.

### 2. Deep Q-Learning Bot (DQN)
- Implements a Deep Q-Network to learn game dynamics through trial and error.
- Uses a neural network to estimate Q-values for actions based on the current state.
- Trains through experience replay and periodically updates a target network for stability.
- Learns to avoid obstacles by maximizing cumulative rewards over time.

---

## Repo Structure

- `dino_solve_jump_threshold.py`: Heuristic bot implementation with grid search optimization.
- `dino_solver_deepQ.py`: Deep Q-Learning bot with neural network and training loop.
- `generate_data.py`: Optional script to generate synthetic pretraining data.
- `threshold_plots/`: Heatmaps showing heuristic performance with different thresholds.

---

## Notes

- The bots interact with the game using Selenium and ChromeDriver.
- The DQN is implemented using TensorFlow/Keras.
- While the heuristic bot can achieve very high scores quickly, the DQN requires longer training but offers more adaptability.

