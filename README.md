# Cliff Walking Lab

This is a reinforcement learning project that implements and compares Policy Iteration and Value Iteration algorithms for solving the Cliff Walking problem.

## Description

The Cliff Walking environment is a classic reinforcement learning problem where an agent must navigate from the start position to the goal while avoiding falling off a cliff. This project implements two dynamic programming methods to solve this problem:

- **Policy Iteration**: Iteratively evaluates and improves the policy
- **Value Iteration**: Directly optimizes the value function

## Features

- Implementation of Policy Iteration algorithm
- Implementation of Value Iteration algorithm
- Visual demonstrations of both methods
- Comparative analysis of results
- Agent behavior analysis showing conservative initial strategies that evolve to optimal cliff-edge navigation

## Installation

```bash
# Clone the repository
git clone https://github.com/wannabeyourfriend/RL-DP-Cliff-walking.git
cd RL-DP-Cliff-walking

# No additional dependencies required - uses only Python standard library
```

## Usage

### Policy Iteration

Run the Policy Iteration algorithm:
```bash
python main.py --method policy
```

### Value Iteration

Run the Value Iteration algorithm:
```bash
python main.py --method value
```

## Results

### Policy Iteration
- **Demo**: [policy_iteration.gif](https://github.com/wannabeyourfriend/RL-DP-Cliff-walking/blob/main/result/policy_iteration.gif)
- **Results**: [result.png](https://github.com/wannabeyourfriend/RL-DP-Cliff-walking/blob/main/result/result.png)

### Value Iteration
- **Demo**: [value_iteration.gif](https://github.com/wannabeyourfriend/RL-DP-Cliff-walking/blob/main/result/value_iteration.gif)

### Analysis
- **Comparison**: [results-contrast.png](https://github.com/wannabeyourfriend/RL-DP-Cliff-walking/blob/main/result/results-contrast.png)

The agent initially adopts conservative strategies, staying away from the cliff. As exploration continues, the agent discovers the cliff and develops more aggressive but higher-reward strategies, moving along the cliff's edge.

## File Structure

- `main.py` - Main execution script
- `policy_iteration.py` - Policy Iteration implementation
- `value_iteration.py` - Value Iteration implementation
- `env_cliff_walking.py` - Cliff Walking environment definition
- `result/` - Output directory for generated visualizations

## Algorithm Details

### Policy Iteration
1. **Policy Evaluation**: Evaluate the current policy by computing state-value functions
2. **Policy Improvement**: Update the policy using the computed value functions
3. **Convergence**: Repeat until policy stabilizes

### Value Iteration
1. **Value Update**: Iteratively update value functions using Bellman equations
2. **Policy Extraction**: Extract optimal policy from converged value functions
3. **Single Pass**: Typically converges faster than policy iteration

## Acknowledgements

This project is inspired by and based on the work from:
- [Hands-on RL by Boyu AI](https://github.com/boyu-ai/Hands-on-RL)

## License

This project is open source and available under the MIT License.
