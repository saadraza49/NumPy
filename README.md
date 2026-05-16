# NumPy

<p align="center">
  <img src="https://numpy.org/images/logo.svg" alt="NumPy Logo" width="200"/>
</p>

<p align="center">
  <strong>The fundamental package for scientific computing with Python</strong>
</p>

<p align="center">
  <a href="https://pypi.org/project/numpy/"><img src="https://img.shields.io/pypi/v/numpy.svg" alt="PyPI version"/></a>
  <a href="https://numpy.org/doc/stable/"><img src="https://img.shields.io/badge/docs-stable-blue.svg" alt="Documentation"/></a>
  <a href="https://github.com/saadraza49/NumPy/actions"><img src="https://img.shields.io/github/actions/workflow/status/saadraza49/NumPy/build_test.yml?branch=main" alt="Build Status"/></a>
  <a href="https://opensource.org/licenses/BSD-3-Clause"><img src="https://img.shields.io/badge/license-BSD--3--Clause-orange.svg" alt="License"/></a>
  <img src="https://img.shields.io/pypi/pyversions/numpy" alt="Python versions"/>
</p>

---

## Overview

NumPy is the foundational library for numerical computing in Python. It provides:

- A powerful **N-dimensional array** object (`ndarray`)
- **Broadcasting** functions for arithmetic operations
- Tools for integrating **C/C++ and Fortran** code
- Useful **linear algebra**, **Fourier transform**, and **random number** capabilities

NumPy is the backbone of the scientific Python ecosystem — used by libraries like **pandas**, **SciPy**, **Matplotlib**, **scikit-learn**, and **TensorFlow**.

---

## Table of Contents

- [Installation](#installation)
- [Quick Start](#quick-start)
- [Key Features](#key-features)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)

---

## Installation

### Using pip

```bash
pip install numpy
```

### Using conda

```bash
conda install numpy
```

### From source

```bash
git clone https://www.github.com/saadraza49/NumPy.git
cd NumPy
pip install .
```

**Requirements:** Python 3.9+

---

## Quick Start

```python
import numpy as np

# Create arrays
a = np.array([1, 2, 3, 4, 5])
b = np.arange(0, 10, 2)

# Array arithmetic
print(a + b)       # [1, 4, 7, 10, 13]
print(a * 2)       # [2, 4, 6, 8, 10]
print(np.sqrt(a))  # [1.  1.41 1.73 2.  2.24]

# Multi-dimensional arrays
matrix = np.zeros((3, 3))
identity = np.eye(3)

# Linear algebra
A = np.array([[1, 2], [3, 4]])
eigenvalues, eigenvectors = np.linalg.eig(A)

# Random numbers
rng = np.random.default_rng(seed=42)
samples = rng.normal(loc=0, scale=1, size=1000)
```

---

## Key Features

### N-Dimensional Arrays
NumPy's core is the `ndarray` — a fast, flexible container for large data sets in Python. Arrays support vectorized operations, making numerical code concise and efficient.

### Broadcasting
Perform arithmetic on arrays of different shapes without writing explicit loops:

```python
a = np.array([[1], [2], [3]])   # shape (3, 1)
b = np.array([10, 20, 30])      # shape (3,)
print(a + b)
# [[11 21 31]
#  [12 22 32]
#  [13 23 33]]
```

### Linear Algebra (`numpy.linalg`)
Full suite of linear algebra operations: matrix multiplication, decompositions (SVD, QR, Cholesky), determinants, inverses, and eigenvalue solvers.

### Fourier Transforms (`numpy.fft`)
Efficient computation of discrete Fourier transforms for signal processing and frequency analysis.

### Random Sampling (`numpy.random`)
Modern random number generation with a range of probability distributions and a Generator-based API for reproducible results.

### Universal Functions (ufuncs)
Fast element-wise operations that support broadcasting, type casting, and output accumulation — with optional C-level performance.

---

## Documentation

| Resource | Link |
|---|---|
| Official Docs | [numpy.org/doc](https://numpy.org/doc/stable/) |
| API Reference | [numpy.org/doc/stable/reference](https://numpy.org/doc/stable/reference/) |
| NumPy Tutorials | [numpy.org/learn](https://numpy.org/learn/) |
| Release Notes | [github.com/saadraza49/NumPy/releases](https://www.github.com/saadraza49/NumPy/releases) |

---

## Contributing

We welcome contributions! Please read our [Contributing Guide](CONTRIBUTING.md) before submitting a pull request.

```bash
# Fork and clone the repo
git clone https://www.github.com/saadraza49/NumPy.git
cd NumPy

# Install in development mode
pip install -e ".[dev]"

# Run tests
python -m pytest numpy/
```

Please follow our [Code of Conduct](CODE_OF_CONDUCT.md) in all interactions.

---

## Citing NumPy

If you use NumPy in your research, please cite:

> Harris, C.R., Millman, K.J., van der Walt, S.J. et al.
> *Array programming with NumPy.* Nature 585, 357–362 (2020).
> [doi:10.1038/s41586-020-2649-2](https://doi.org/10.1038/s41586-020-2649-2)

---

## License

NumPy is distributed under the [BSD 3-Clause License](LICENSE.txt).

---