
# Deep Q-Networks (DQN) with RGB Images as Observations

This repository contains the implementation of a **Deep Q-Network (DQN)** agent that uses 56x56 pixel RGB images (representing the top-down view of the agent) as the state representation. The agent includes a custom neural network architecture for both the policy network and the target network.

## Task Objectives

1. **Training**  
   - Train the DQN agent for a maximum of 3000 episodes.
   - Plot the reward as a function of training steps using TensorBoard.

2. **Evaluation**  
   - Evaluate the trained policy by:
     - Calculating the **episode completion rate** (percentage of episodes where the agent reached the goal).  
     - Measuring the **average number of steps** per episode.  
     - Calculating the **average reward** over 1000 evaluation episodes.

3. **Hyper-Parameter Tuning**  
   - Perform hyper-parameter tuning to find optimal training values for maximizing the **average reward** and **completion rate**.

## Implementation Details

### Neural Network Architecture

The neural network is divided into two parts:
1. **Feature Learning Layers**  
   - Configurable **number of convolutional layers**.
   - **Kernel size** and **stride** for each CNN layer.

2. **Function Approximator Layers**  
   - Configurable **number of hidden, fully-connected, feed-forward layers**.
   - **Number of neurons** in each hidden layer.
   - **Non-linear activation function** for each layer (ReLU recommended).

### Training Hyper-Parameters

The training process involves tuning the following hyper-parameters:
- **Learning rate (α)**.
- **Discount factor (γ)**.
- **Interval**: The number of training steps between fixed Q-value target updates.
- **Mini-batch size** for experience replay.

### Exploration Hyper-Parameters

For the ε-greedy exploration strategy, the following hyper-parameters are configurable:
- Maximum and minimum ε-values (**ε_max** and **ε_min**) for the exploration threshold.
- **Epsilon decay rate (ε_decay)** to reduce exploration over time.

## Key Features

- RGB images used as observations for state representation.
- Custom neural network architecture for the policy and target networks.
- Training and evaluation metrics visualized with TensorBoard.
- Fine-tuned hyper-parameters for optimal performance.
- Modular design for easy customization of the neural network and training parameters.

## Results

- Plots of reward trends over training steps.
- Episode completion rate, average steps, and average reward over 1000 evaluation episodes.
- Hyper-parameter tuning results for optimal performance.
