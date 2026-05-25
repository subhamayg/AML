# Label Noise Robustness

This project focuses on implementing machine learning algorithms that are robust to label noise, developed as part of Assignment 2 for COMP5328 (Advanced Machine Learning).

## Overview

In real-world datasets, labels are often noisy or corrupted. This project explores methods to mitigate the impact of such noise on model performance.

Key implementations include:
- **Transition Matrix Estimator**: Utilizing the Anchor Point Method to estimate the label noise transition matrix.
- **Robust Classifiers**:
  - Cross-Entropy with Noise Correction (Forward Learning)
  - Co-teaching with Symmetric Cross-Entropy (SCE) loss

## Datasets

The algorithms are evaluated on image classification datasets such as CIFAR and FashionMNIST, simulating various types and levels of label noise.

## Code Structure

- `algorithm/Code.ipynb`: The main Jupyter Notebook containing data exploration, model definitions, training loops, and evaluation metrics.
- `algorithm/T_cifar_est.pt`: Pre-computed transition matrix for CIFAR.
- `algorithm/top1_accuracy_results.csv`: Saved accuracy results for the models.

## How to Run

1. Open `algorithm/Code.ipynb` in Jupyter Notebook or a similar environment.
2. Ensure you have the necessary dependencies installed (e.g., PyTorch, NumPy, Pandas).
3. Run the cells sequentially to train and evaluate the models. Note that rigorous performance evaluation (the 10 splits section) may take a significant amount of time to execute.
