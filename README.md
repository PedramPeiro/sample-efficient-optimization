# Sample Efficient Optimization: Multi-Objective Bayesian Approach for Repair Workshop Operations

## Overview

This repository contains the implementation of a multi-objective optimization framework for repair workshop operations, aiming to minimize the maximum queue length and operational costs. The project combines simulation, probabilistic modeling, and optimization techniques to deliver robust, interpretable solutions for system improvement.

## Key Features

- **Custom Discrete-Event Simulator**: Models the workflow of a repair workshop, incorporating variability in inter-arrival times, service durations, and rework processes.
- **Gaussian Process Modeling**: Utilizes Sparse Gaussian Processes for efficient and accurate surrogate modeling of the maximum queue length.
- **Multi-Objective Bayesian Optimization (MOBO)**: Identifies Pareto-optimal trade-offs between queue management and operational cost.
- **Variance Reduction Techniques**: Enhances the reliability of predictions using metrics like maximum waiting time for better interpretability.

## Methodology

1. **Simulation**: 
   - Models the repair workflow across five workstations.
   - Captures system dynamics such as rework, maintenance, and priority handling.

2. **Gaussian Process Modeling**:
   - Implements Sparse GP to predict the maximum queue length (Qmax) with reduced computational overhead.
   - Incorporates advanced kernels (e.g., RBF, Matérn, and Spectral Mixture) to model complex relationships.

3. **Optimization**:
   - Employs MOBO to balance conflicting objectives.
   - Uses acquisition functions like qNEHVI and qNParEGO for efficient exploration.

4. **Variance Reduction**:
   - Applies the Control Variates method to improve the accuracy of Qmax predictions.

## Results

- **Pareto Front Generation**: Demonstrates trade-offs between cost and Qmax using MOBO.
- **Performance Metrics**: Achieves robust predictions with low variance and high interpretability.

## Technologies Used

- Python
- TensorFlow
- PyTorch
- Gaussian Processes (GPyTorch)
- NVIDIA GPU for accelerated computation

