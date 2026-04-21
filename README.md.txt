# Self-Pruning Neural Network

## Overview
This project implements a self-pruning neural network where each weight is controlled by a learnable gate. The network learns to remove unnecessary connections during training.

## Key Features
- Custom PrunableLinear layer
- Learnable gate mechanism
- L1 sparsity regularization
- CIFAR-10 dataset training
- Sparsity vs accuracy trade-off

## How It Works
Each weight has a gate (0–1). During training:
- Important weights → gate ≈ 1
- Unimportant weights → gate ≈ 0 (pruned)

## Results
The model was trained with different lambda values to study sparsity vs accuracy.

## How to Run
```bash
pip install torch torchvision matplotlib
python self_pruning_network.py