# CompMethods Notes - Resource Summary

This document provides a comprehensive overview of the Computational Methods course resources, including code examples, datasets, and the recommended learning path.

## Table of Contents

1. [Code Folder Overview](#code-folder-overview)
2. [Data Folder Overview](#data-folder-overview)
3. [Recommended Learning Path](#recommended-learning-path)

---

## Code Folder Overview

The `code/` directory contains Python scripts, Jupyter notebooks, and supplementary files organized by topic.

### Core Python Programming

| Folder | Files | Description |
|--------|-------|-------------|
| **PythonIntro** | `python_intro.py` | Basic Python fundamentals: sphere volume calculation, string manipulation, list operations, pig latin translator, palindrome finder, harmonic series |
| **StandardLibrary** | `standard_library.py`, `box.py` | Python standard library usage: `itertools`, `math`, power set calculation, "Shut the Box" game implementation |
| **Exceptions_FileIO** | `exceptions_fileIO.py` | Exception handling, random walk with keyboard interrupt handling, `ContentFilter` class for file manipulation |
| **ObjectOriented** | `object_oriented.py` | OOP concepts: `Backpack` class, inheritance (`Knapsack`, `Jetpack`), magic methods (`__add__`, `__lt__`), `ComplexNumber` class |
| **UnitTest** | `specs.py`, `test_specs.py` | Unit testing with pytest: testing `smallest_factor`, `month_length`, `operate`, `Fraction` class, Set game logic |
| **UnixShell1** | `unixshell1.sh` | Unix shell commands and bash scripting for file management, directory operations, permissions, archiving |

### Numerical Computing & Data Analysis

| Folder | Files | Description |
|--------|-------|-------------|
| **NumPyIntro** | `numpy_intro.py` | NumPy array creation, matrix multiplication, stacking functions, row normalization, slicing grid problems |
| **AdvancedNumPy** | `advanced_numpy.py` | Advanced operations: fancy indexing, performance benchmarking, `einsum`, array padding, prime factorization |
| **Pandas1** | `pandas1.ipynb` (notebook) | Introduction to Pandas DataFrames: data loading, filtering, basic operations |
| **Pandas3** | `pandas3.ipynb` (notebook) | Advanced Pandas: groupby, pivot tables, complex data transformations |

### Data Visualization

| Folder | Files | Description |
|--------|-------|-------------|
| **Matplotlib1** | `matplotlib_intro.py` | Basic visualization: variance plots, trigonometric functions, subplot grids, scatter plots, heatmaps, contour maps |
| **Matplotlib2** | `matplotlib2.ipynb` (notebook) | Intermediate Matplotlib techniques |
| **Matplotlib3** | `animation.ipynb` (notebook) | Matplotlib animations |

### Econometrics & Structural Estimation

| Folder | Files | Description |
|--------|-------|-------------|
| **gmm** | `distributions.py` | PDF functions for GMM: Lognormal, Gamma (GA), Generalized Gamma (GG), Generalized Beta 2 (GB2) distributions |
| **mle** | `distributions.py` | PDF functions for MLE: Same distributions as gmm for likelihood estimation |
| **StrEstPaper** | LaTeX templates | Templates for papers and presentations |

### Other

| Folder | Files | Description |
|--------|-------|-------------|
| **junk_funcs.py** | - | Placeholder/test module |

---

## Data Folder Overview

The `data/` directory contains datasets organized by topic, supporting the code examples and exercises.

### Pandas Practice Data

| File | Format | Size | Description |
|------|--------|------|-------------|
| `budget.csv` | CSV | 1.7 KB | Budget tracking (Rent, Groceries, Gas, Utilities, etc.) |
| `paychecks.csv` | CSV | 0.8 KB | Paycheck data for datetime ranges |
| `DJIA.csv` | CSV | 53.9 KB | Dow Jones Industrial Average historical stock data |
| `crime_data.csv` | CSV | 5.3 KB | US crime statistics by year |
| `college.csv` | CSV | 78.8 KB | US college statistics (private/public, tuition, donations) |
| `mammal_sleep.csv` | CSV | 4.4 KB | Mammal sleep data |
| `Ohio_1999.csv` | CSV | 35.3 KB | Ohio labor statistics (race, sex, education, hours, earnings) |
| `titanic.csv` | CSV | 108 KB | Titanic passenger survival data |

### Visualization Data

| File | Format | Size | Description |
|------|--------|------|-------------|
| `orbits.npz` | NumPy | 135 KB | 3D orbital coordinates for Mercury, Venus, Earth, Mars |

### Basic Empirical Methods

| File | Format | Size | Description |
|------|--------|------|-------------|
| `Auto.csv` | CSV | 18 KB | Auto fuel economy data (mpg, cylinders, displacement, etc.) |
| `maketable1.dta` | Stata | 14 KB | Stata format econometrics data |

### Logistic Regression

| File | Format | Size | Description |
|------|--------|------|-------------|
| `titanic-train.csv` | CSV | 60.3 KB | Titanic training data for classification |
| `titanic_clean.csv` | CSV | 15.5 KB | Cleaned Titanic dataset for logit models |

### Machine Learning

| File | Format | Size | Description |
|------|--------|------|-------------|
| `Hitters.csv` | CSV | 35 KB | Baseball player statistics for salary prediction |

### Structural Estimation (GMM/MLE/SMM)

| File | Format | Size | Description |
|------|--------|------|-------------|
| `MacroSeries.txt` | TXT | 10 KB | Macroeconomic time series |
| `hh_inc_synth.txt` | TXT | 3.0 MB | Synthetic household income (~50,000 values) |
| `claims.txt` | TXT | 191 KB | Insurance claims data (~5,000 values) |
| `usincmoms.txt` | TXT | 0.8 KB | US income moments data |
| `Econ381totpts.txt` | TXT | 1 KB | Economics exam scores |

---

## Recommended Learning Path

Based on the Jupyter Book structure in `docs/book/_toc.yml`, the following is the recommended order for learning:

### Phase 1: Python Fundamentals
1. **PythonIntro** - Basic syntax, data types, functions
2. **StandardLibrary** - Built-in modules and utilities
3. **Exceptions_FileIO** - Error handling and file operations
4. **ObjectOriented** - Classes, inheritance, design patterns

### Phase 2: Numerical & Data Computing
5. **NumPyIntro** → **AdvancedNumPy** - Array operations, vectorization
6. **Pandas1** → **Pandas3** - DataFrame manipulation, analysis

### Phase 3: Data Visualization
7. **Matplotlib1** → **Matplotlib2** → **Matplotlib3** - From basic plots to animations

### Phase 4: Software Engineering Best Practices
8. **UnitTest** - Writing tests with pytest
9. **UnixShell1** - Command line proficiency

### Phase 5: Econometrics Methods
10. **basic_empirics** - Basic empirical methods, OLS regression
11. **basic_ml** - Introduction to machine learning

### Phase 6: Advanced Structural Estimation
12. **mle** - Maximum Likelihood Estimation
13. **gmm** - Generalized Method of Moments
14. **smm** - Simulated Method of Moments

---

### Quick Reference: Code-to-Data Mapping

| Code Module | Data Folder | Key Datasets |
|-------------|-------------|--------------|
| Pandas1, Pandas3 | `Pandas1/`, `Pandas3/` | budget.csv, titanic.csv, college.csv, DJIA.csv |
| Matplotlib3 | `Matplotlib3/` | orbits.npz |
| basic_empirics | `basic_empirics/` | Auto.csv, titanic_train.csv |
| basic_ml | `basic_ml/` | Hitters.csv |
| gmm | `gmm/` | hh_inc_synth.txt, MacroSeries.txt |
| mle | `mle/` | claims.txt, MacroSeries.txt |
| smm | `smm/` | claims.txt, usincmoms.txt, MacroSeries.txt |

---

*Generated from repository structure analysis. Last updated: 2026-01-01*
