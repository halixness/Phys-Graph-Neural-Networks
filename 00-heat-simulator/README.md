## Jacobi Heat Simulator

[![Generic badge](https://img.shields.io/badge/using-PyTorch-orange.svg)](https://pytorch.org/)
[![Generic badge](https://img.shields.io/badge/using-Deep_Graph_Library-<COLOR>.svg)](https://docs.dgl.ai/)

A simple Graph Neural Network applied to heat propagation simulations ([Jacobi Method](https://en.wikipedia.org/wiki/Jacobi_method)).

| Real          | Prediction    |
| ------------- |:-------------:|
| <img src="https://github.com/halixness/GNN-Phys/blob/main/00-heat-simulator/animation/real/real.gif" width="250" height="250"/>      | <img src="https://github.com/halixness/GNN-Phys/blob/main/00-heat-simulator/animation/prediction/prediction.gif" width="250" height="250"/> |

## Architecture 

We created a simple GNN consisting in:

- GraphConv Layer
- ReLU Activation
- GraphConv Layer

For each timestep, the heatmap is transformed into a Graph, where each node is a heat cell with up to 4 neighbours (left, right, up, down, except for border cells).

## Dataset

The dataset has been generated with a heat simulator written in C. The simulation is represented by ~60 timesteps, each one encoded as a 510x510 grid of floats ranging from 0 to 1 (heatmap values).
