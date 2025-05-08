# Collaboration and Competition Project: Tennis Environment

This repository implements a multi-agent reinforcement learning solution for the Tennis environment using the Multi-Agent Deep Deterministic Policy Gradient (MADDPG) algorithm. Two agents are trained to collaboratively keep a ball in play by controlling rackets in a Unity-based simulation.

## Project Environment Details

In the Tennis environment, two agents control rackets to hit a ball over a net, aiming to keep it in play as long as possible. Below are the key specifications:

- **State Space**: 
  - Each agent receives a 24-dimensional state vector.
  - Includes the position and velocity of the ball and the agent's own racket.
- **Action Space**: 
  - Each agent outputs a 2-dimensional continuous action.
  - Actions control movement toward/away from the net and jumping to hit the ball.
  - Action values are bounded between -1 and 1.
- **Reward Structure**: 
  - +0.1 when an agent hits the ball over the net.
  - -0.01 if the ball hits the ground or goes out of bounds.
- **Success Criterion**: 
  - The environment is considered solved when the average score over 100 consecutive episodes reaches at least +0.5.
  - The score per episode is the maximum of the two agents' individual scores.

## Installing Dependencies and Downloading Files

To set up the project, install the required dependencies and download the Tennis environment as follows:

### Prerequisites

- **Python**: Version 3.6 or higher.
- **Unity ML-Agents**: Required to interface with the Tennis environment.

### Installation Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/your-repo-name.git
   cd your-repo-name
   
2. **Install Python Packages**:
   - Use pip to install the necessary libraries
    ```bash
     pip install torch numpy matplotlib unityagents
    
3. **Download The Tennis Environment**:

  
4. **Optional: Protocol Buffers**:
   
