# Drone-Hovering-using-RL
Drone Hovering using Reinforcement Learning (Monte Carlo, Q-Learning, SARSA, Double Q-Learning and Experience Replay)

## Overview
This project implements and compares multiple **model-free Reinforcement Learning (RL)** algorithms for autonomous drone hovering in the PyBullet-based HoverAviary environment.

The objective is to keep a quadrotor drone hovering at the target position **[0, 0, 1]** using discrete thrust actions.

## Algorithms Implemented

- Monte Carlo Control (First-Visit MC)
- Q-Learning
- SARSA
- Double Q-Learning
- Experience Replay

## Environment

- Simulator: gym-pybullet-drones
- Environment: HoverAviary
- State Space: Discretized (x, y, z) position
- Action Space:
  - -1 : Decrease thrust
  - 0  : Maintain thrust
  - +1 : Increase thrust

## RL Workflow

```text
State (x,y,z)
      |
      v
Discretization
      |
      v
RL Agent
(MC / Q-Learning / SARSA)
      |
      v
Action Selection
(-1,0,+1 thrust)
      |
      v
HoverAviary Environment
      |
      v
Reward
```
## Results

| Algorithm | Reward |
|------------|---------|
| Monte Carlo | 449.71 |
| Q-Learning | 331.10 |
| SARSA | 410.56 |
| Double Q-Learning | 430.09 |
| Experience Replay | 447.90 |

## Algorithm Comparison

| Algorithm | Type | Policy |
|------------|--------|---------|
| Monte Carlo | Model-Free | On-Policy |
| Q-Learning | TD Learning | Off-Policy |
| SARSA | TD Learning | On-Policy |
| Double Q-Learning | TD Learning | Off-Policy |
| Experience Replay | TD Learning | Off-Policy |

## Installation

```bash
conda create -n drone_rl python=3.10 -y
conda activate drone_rl

conda install -c conda-forge pybullet -y

pip install -r requirements.txt
```

## Run

```bash
python user_code.py
python evaluate_submission.py
python bonus_challenges.py
```

## Future Work

- Deep Q Networks (DQN)
- PPO
- SAC
- Prioritized Experience Replay
- Continuous Action Spaces
- Real Drone Deployment

## Author

Anupam Prakash
PhD Scholar, IIT Mandi
