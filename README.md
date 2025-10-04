# Fixed-Sparsity Matrix Approximation from Matrix-Vector Products

This repository contains code and data to reproduce all numerical experiments from the paper on [Fixed-sparsity matrix approximation from matrix-vector products](https://arxiv.org/abs/2402.09379).

## Repository Contents

### Jupyter Notebooks
- **`sparse_recovery.ipynb`**: Main experiments comparing sparse recovery and coloring-based algorithms on two test problems:
  - Model problem: Inverse of a tridiagonal matrix with varying bandwidth
  - Trefethen primes: Inverse of a prime-diagonal matrix with structured sparsity

- **`hard_example.ipynb`**: Demonstrates sparsity patterns with different coloring properties:
  - Hard coloring example ($k^2$ coloring number for sparsity $s$)
  - Good coloring example (diagonal sparsity)

- **`coloring.ipynb`**: Analysis of coloring number vs sparsity for real-world matrices from SuiteSparse Matrix Collection

### Data Files
- **`model.npy`**: Cached results for model problem experiments
- **`trefethen_primes.npy`**: Cached results for Trefethen primes experiments
- **`matrices/`**: Downloaded SuiteSparse matrices (generated when running `coloring.ipynb`)

### Output
- **`imgs/`**: Generated figures (PDF format) used in the paper

## Dependencies

The code requires the following Python packages:
- `numpy` - Numerical computation
- `scipy` - Sparse matrix operations and scientific computing
- `matplotlib` - Plotting and visualization
- `sympy` - Symbolic mathematics (for prime number generation)
- `networkx` - Graph algorithms (for greedy coloring)
- `ssgetpy` - SuiteSparse Matrix Collection interface (only for `coloring.ipynb`)
- `jupyter` - Jupyter notebook interface

For LaTeX rendering in figures, you'll also need a LaTeX distribution installed on your system.
