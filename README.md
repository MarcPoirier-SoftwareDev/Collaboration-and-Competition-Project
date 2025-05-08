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
  - Obtain the Tennis environment for your operating system from the [Unity ML-Agents GitHub releases](https://github.com/Unity-Technologies/ml-agents/releases).
  - Supported platforms:
    - Linux: `Tennis_Linux.zip`
    - macOS: `Tennis.app.zip`
    - Windows: `Tennis_Windows_x86_64.zip`
  - Extract the downloaded file and place it in the project directory.
  - Update the environment path in your code, e.g.:
    ```python
    env = UnityEnvironment(file_name="path/to/Tennis")
  
4. **Optional: Protocol Buffers**:
   - If compatibility issues arise, install a specific version of Protocol Buffers:
     ```bash
     pip install protobuf==3.20.3

## How to run the code

Follow these steps to train the agents in the Tennis environment:

- **Set Up the Environment**
  - Ensure the Tennis environment file is in the project directory and the path in the code is correctly specified.
- **Run the Training**:
  - If using a Python script (e.g., train.py), execute:
    ```bash
    python train.py

  - Alternatively, if using a Jupyter notebook, open it and run all cells:
    ```bash
    jupyter notebook Tennis_Collaboration_Competition.ipynb

- **Training Process**:
  - The script/notebook initializes the MADDPG agents and begins training.
  - It tracks episode scores and computes the average score over a 100-episode window.
  - Training stops when the average score reaches ≥ +0.5 over 100 episodes or a maximum episode limit is hit.
  - Model checkpoints (e.g., `checkpoint_agent0_actor.pth`, `checkpoint_agent0_critic.pth`) are saved upon solving the environment.

- **View Results**:
  - Console output shows episode scores, average scores, and elapsed time, e.g.:
  ```
  Episode 100	Avg Score: 0.0123	Max Score: 0.1000	Time: 1.23
  Episode 2050	Avg Score: 0.5012	Max Score: 0.7000	Time: 1.45
  Environment solved in 2050 episodes with average score 0.5012


  - A plot of scores is saved as scores_plot.png.

## Additional Notes
- Ensure your system has sufficient memory and computational resources, as training may take several hours depending on hardware.
- Modify hyperparameters in the code (e.g., learning rate, buffer size) to experiment with performance.

For further details, see the project report (if available) or the code comments.


   
