# GAIL - USV Path Planning with RL and Imitation Learning

Path planning framework for unmanned surface vessels (USVs) using Generative Adversarial Imitation Learning (GAIL) and Proximal Policy Optimization (PPO). Learns navigation policies from expert demonstrations while handling ocean currents, obstacles, and dynamic environments.

## Architecture

- **Environment** (`env.py`) - Custom USV simulation with ocean dynamics, obstacle fields, current modeling, and goal-directed navigation rewards
- **PPO Agent** (`ppo.py`) - Baseline PPO implementation for direct RL-based path planning
- **GAIL Training** - Actor-critic policy with discriminator network that learns from expert trajectories to produce smooth, efficient paths
- **Visualization** (`plot.py`) - Trajectory plotting with obstacle maps and path comparison across training methods

## Pre-trained Models

- `env1_gail_actor.ckpt` / `env1_gail_critic.ckpt` / `env1_gail_disc.ckpt` - GAIL policy trained on coastal patrol scenarios
- `env1_ppo.ckpt` - Baseline PPO policy for comparison

## Stack

Python / PyTorch / NumPy / Matplotlib

## Usage

```bash
python ppo.py          # Train PPO baseline
python plot.py         # Visualize learned trajectories
```
