# Cartpole-BAC-ML

This repository contains an implementation of a Deep Q-Network (DQN) to solve the CartPole environment. Developed as part of the **BAC ML team S26** projects.

## Overview

The project uses Reinforcement Learning (specifically, DQN with experience replay and a target network) to balance a pole on a moving cart. It interacts with the `CartPole-v1` environment from OpenAI's Gymnasium. The neural network architecture and training loop are defined in PyTorch. 

## Repository Structure

- `cartpole_dqn.ipynb`: The main Jupyter Notebook containing the DQN implementation, training loop, plotting, and evaluation.
- `cartpole_best.pth`: The saved PyTorch state dictionary for the best-performing model during training.
- `LICENSE`: The repository's license file.

## Requirements

To run the notebook, you will need the following libraries installed:
- `torch` (PyTorch)
- `gymnasium`
- `numpy`
- `matplotlib`
- `IPython`

Install them via pip:

```bash
pip install torch gymnasium numpy matplotlib ipython
```

## Usage

1. Open the [cartpole_dqn.ipynb](cartpole_dqn.ipynb) notebook.
2. Run the cells sequentially to build the model architecture (`CartPoleBrain`) and hyperparameter settings.
3. The training loop will execute, automatically periodically updating a live matplotlib plot with the current and rolling average scores.
4. The notebook securely saves the highest performing model dynamically to `cartpole_best.pth`.
5. You can run the final cell at the end of the notebook to load the model checkpoint and verify its final weights.

## Neural Network Architecture

The repository utilizes a simple Multi-Layer Perceptron (MLP) for its policy and target network:
- **Input:** 4 state features (cart position, cart velocity, pole angle, pole velocity at tip)
- **Hidden Layers:** 2 layers of 64 nodes with ReLU activations
- **Output:** 2 nodes representing the Q-values for moving the cart left or right.

## Acknowledgements

- **BAC ML team S26**
- [Gymnasium (CartPole-v1)](https://gymnasium.farama.org/environments/classic_control/cart_pole/)
