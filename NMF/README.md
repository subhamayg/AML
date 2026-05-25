# Non-negative Matrix Factorization (NMF)

This project explores Non-negative Matrix Factorization (NMF) algorithms for dimensionality reduction and feature extraction, primarily applied to facial recognition datasets. It was developed for Assignment 1 of COMP5328 (Advanced Machine Learning).

## Overview

The project implements and evaluates different variations of NMF:
- **Multiplicative Update Factorization**: Standard NMF using multiplicative update rules.
- **Robust Non-negative Matrix Factorization (L1-Norm)**: NMF robust to outliers using an L1-norm loss formulation.
- **Encoding Algorithms**: Methods to encode new data using the learned factorizations.

## Datasets

The project is designed to use facial image datasets to evaluate the models:
- **ORL Dataset**: 40 distinct subjects under varying conditions.
- **Extended YaleB Dataset**: 38 subjects under different poses and illuminations.

## Evaluation Metrics

The quality of the factorization is evaluated using:
- Relative Reconstruction Errors (RRE)
- Accuracy & NMI (Normalized Mutual Information)

## Code Structure

- `algorithm/Code.ipynb`: The main Jupyter Notebook containing the implementations of NMF, data loading, training routines, and visualizations.
- `NIPS-2000-algorithms-for-non-negative-matrix-factorization-Paper.pdf`: Reference paper for the core NMF algorithms.

## How to Run

1. Open `algorithm/Code.ipynb` in Jupyter Notebook or a similar environment.
2. Ensure you have the necessary dependencies installed (e.g., NumPy, SciPy, Matplotlib).
3. The notebook is structured to first define the helper functions and models. You can run the tuning or single-split sections for fast execution, or the full experimental suite (which can take a couple of hours) for comprehensive results.
