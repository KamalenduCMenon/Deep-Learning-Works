# Polynomial Regression with Weight Decay


This project analyzes polynomial regression models on synthetic data:

Y = cos(2πX) + Z, where Z ∼ N(0, σ²)

We evaluate the impact of model complexity (degree), sample size (N), and noise (σ²) on training (Ein) and testing (Eout) errors — with and without **L2 regularization (weight decay)**.

## 🔧 Key Components
- `getData()`: Generate noisy data.
- `fitData()`: Fit polynomial regression with optional regularization.
- `getMSE()`: Compute mean squared error.
- `experiment()`: Run trials and plot average Ein/Eout.

## 🔍 Findings
- High-degree models overfit small datasets.
- Weight decay (λ = 0.1) improves generalization.
- Larger datasets reduce variance and testing error.

## 🛠 Tech
- Python, NumPy, Matplotlib
