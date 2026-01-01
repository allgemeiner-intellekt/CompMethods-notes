# Project Overview: Computational Methods for Economists using Python

## What is this project?

This is **Computational Methods for Economists using Python**, an open-access Jupyter Book by Richard W. Evans. It's a comprehensive educational resource covering Python programming, econometrics, machine learning, and structural estimation methods for economists.

The project serves both as a learning resource and reference implementation, with executable code examples organized by chapter/topic. The book is freely available online at: https://opensourceecon.github.io/CompMethods/

## Who is this for?

- **Economics graduates** learning Python for research and data analysis
- **Researchers** needing computational methods for econometrics
- **Students** studying computational economics
- **Practitioners** looking for reference implementations of econometric methods

## Python Requirements for Economics Graduates

### Core Python Version
- **Python 3.10+ required** (3.10 and 3.11 tested)
- The project uses modern Python features and best practices

### Essential Libraries for Economics (from environment.yml)

The `environment.yml` file specifies the complete scientific Python stack for economics:

#### **Data Analysis & Scientific Computing**
- `numpy` - Numerical computing and array operations
- `scipy` - Scientific computing and optimization
- `pandas` - Data manipulation and analysis
- `matplotlib` - Data visualization
- `bokeh` - Interactive visualization

#### **Development & Documentation**
- `jupyter` - Interactive computing notebooks
- `jupyter-book>=0.11.3` - Building the book
- `ipython` - Enhanced Python shell
- `black` - Code formatting
- `pytest` - Testing framework
- `coverage` - Code coverage analysis

#### **Documentation Tools**
- `sphinx` - Documentation generation
- `sphinx-exercise` / `sphinx-proof` - Educational content
- `sphinxcontrib-bibtex>=2.0.0` - Bibliography management
- `pydata-sphinx-theme` - Modern documentation theme

### Why these libraries matter for economics:
- **NumPy/SciPy**: Essential for numerical optimization, linear algebra, and statistical computations
- **Pandas**: Industry standard for data manipulation (time series, panel data)
- **Matplotlib/Bokeh**: Create publication-quality graphs and interactive dashboards
- **Jupyter**: Reproducible research and teaching

## Learning Path for Economics Graduates

### Phase 1: Python Fundamentals (Weeks 1-4)
1. **Python Basics** (`code/PythonIntro/`)
   - Variables, data types, control structures
   - Functions and basic programming concepts

2. **Standard Library** (`code/StandardLibrary/`)
   - Built-in modules for file I/O, datetime, etc.
   - Essential tools every Python programmer needs

3. **Error Handling & File I/O** (`code/Exceptions_FileIO/`)
   - Robust code with try/except blocks
   - Reading/writing data files (CSV, JSON, etc.)

### Phase 2: Scientific Python Stack (Weeks 5-8)
4. **NumPy** (`code/NumPyIntro/`, `code/AdvancedNumPy/`)
   - Array operations, linear algebra, broadcasting
   - Performance optimization for numerical code

5. **Pandas** (`code/Pandas1/`, `code/Pandas3/`)
   - DataFrames, Series, data manipulation
   - Time series analysis (crucial for economics!)
   - Merging, grouping, and aggregation

6. **Matplotlib** (`code/Matplotlib1/`, `code/Matplotlib2/`, `code/Matplotlib3/`)
   - Creating publication-quality graphs
   - Customizing plots for academic papers
   - Subplots, annotations, and styling

### Phase 3: Advanced Programming (Weeks 9-12)
7. **Object-Oriented Programming** (`code/ObjectOriented/`)
   - Classes, inheritance, polymorphism
   - Building reusable econometric models

8. **Unit Testing** (`code/UnitTest/`)
   - Writing tests for your economic models
   - Ensuring reproducibility and correctness

9. **Unix Shell** (`code/UnixShell1/`)
   - Command line skills for data processing
   - Automation and workflow management

### Phase 4: Econometric Methods (Weeks 13-16)
10. **Basic Empirical Methods** (`docs/book/basic_empirics/`)
    - Regression analysis, hypothesis testing
    - Logistic regression for binary outcomes

11. **Machine Learning** (`docs/book/basic_ml/`)
    - Introduction to ML concepts
    - Applications in economics

12. **Structural Estimation** (`docs/book/struct_est/`)
    - Maximum Likelihood Estimation (MLE) - `code/mle/`
    - Generalized Method of Moments (GMM) - `code/gmm/`
    - Simulated Method of Moments (SMM)

### Phase 5: Advanced Topics (Weeks 17+)
13. **Deep Learning** (`docs/book/deep_learn/`)
    - Neural networks for economic applications
    - Time series forecasting

14. **Git and GitHub** (`docs/book/git/`)
    - Version control for collaborative research
    - Open science practices

## Project Structure: Where to Find What

### Code Organization
```
code/
├── PythonIntro/           # Basic Python programming
├── StandardLibrary/       # Python standard library modules
├── Exceptions_FileIO/     # Error handling and file operations
├── NumPyIntro/           # Introduction to NumPy
├── AdvancedNumPy/        # Advanced NumPy techniques
├── Pandas1/              # Pandas basics
├── Pandas3/              # Advanced Pandas
├── Matplotlib1/          # Matplotlib basics
├── Matplotlib2/          # Intermediate Matplotlib
├── Matplotlib3/          # Advanced Matplotlib
├── ObjectOriented/       # Object-oriented programming
├── UnitTest/             # Testing with pytest
├── UnixShell1/           # Unix shell commands
├── mle/                  # Maximum Likelihood Estimation
├── gmm/                  # Generalized Method of Moments
└── StrEstPaper/          # Structural estimation paper example
```

### Data Files
```
data/
├── Pandas1/              # Data for Pandas examples
├── Pandas3/              # More Pandas datasets
├── Matplotlib3/          # Plotting data
├── basic_empirics/       # Empirical methods datasets
├── basic_ml/             # Machine learning data
├── gmm/                  # GMM estimation data
├── mle/                  # MLE estimation data
└── smm/                  # SMM estimation data
```

### Book Content
```
docs/book/
├── python/               # 10 chapters on Python fundamentals
├── basic_empirics/       # Basic empirical methods
├── basic_ml/             # Machine learning introduction
├── deep_learn/           # Neural networks and deep learning
├── struct_est/           # Structural estimation (MLE, GMM, SMM)
├── git/                  # Git and GitHub
└── appendix/             # Glossary and appendix
```

### Images and Visuals
```
images/
├── basic_empirics/       # Images for empirical methods
├── gmm/                  # GMM visualization
├── mle/                  # MLE diagrams
└── smm/                  # SMM illustrations
```

## Getting Started

### 1. Environment Setup
```bash
# Using Conda (recommended)
conda env create -f environment.yml
conda activate compmethods-dev

# Using pip
pip install -e .
```

### 2. Learning Approach
1. **Start with the book**: Read chapters in `docs/book/python/` sequentially
2. **Run the code**: Execute examples in corresponding `code/{topic}/` directories
3. **Modify and experiment**: Change parameters, try your own data
4. **Check understanding**: Run tests in `tests/` directory

### 3. Development Commands
```bash
# Format your code (important for consistency)
make format

# Run tests to verify understanding
make test

# Build the book locally to see your changes
make documentation
```

## Key Resources for Economics Graduates

### Foundational Python Skills
- **File I/O** (`code/Exceptions_FileIO/`): Handling economic datasets
- **NumPy** (`code/NumPyIntro/`): Matrix operations for econometrics
- **Pandas** (`code/Pandas1/`): Panel data and time series analysis
- **Matplotlib** (`code/Matplotlib1/`): Creating academic graphs

### Econometric Methods
- **Regression Analysis**: `docs/book/basic_empirics/BasicEmpirMethods.md`
- **Maximum Likelihood**: `code/mle/` and `docs/book/struct_est/MLE.md`
- **GMM Estimation**: `code/gmm/` and `docs/book/struct_est/GMM.md`

### Research Skills
- **Version Control**: `docs/book/git/intro.md`
- **Testing**: `code/UnitTest/` - Essential for reproducible research
- **Documentation**: All code includes docstrings and examples

## Tips for Economics Students

1. **Focus on Pandas time series** - Crucial for economic data analysis
2. **Master NumPy arrays** - Foundation for all econometric computations
3. **Learn to create publication-quality graphs** - `code/Matplotlib3/` has advanced examples
4. **Practice with real economic data** - Use datasets in `data/` directory
5. **Understand MLE and GMM** - Core estimation methods in modern econometrics

## Where to Get Help

1. **Book website**: https://opensourceecon.github.io/CompMethods/
2. **GitHub Issues**: https://github.com/OpenSourceEcon/CompMethods/issues
3. **Contributor Guide**: `docs/book/contrib/contributing.md`

## License and Citation

- **License**: AGPL-3.0 (open source for academic use)
- **Citation**: See `README.md` for proper citation format

---

*This overview was generated to help economics graduates navigate the Computational Methods for Economists using Python project. The project provides a comprehensive path from Python basics to advanced econometric methods, with executable examples and real economic datasets.*