# CLAUDE.md

## Project Overview

This is *Computational Methods for Economists using Python*, an open-access Jupyter Book by Richard W. Evans. It's a comprehensive educational resource covering Python programming, econometrics, machine learning, and structural estimation methods for economists.

The project serves both as a learning resource and reference implementation, with executable code examples organized by chapter/topic.

## Common Development Commands

### Environment Setup
```bash
# Using Conda (recommended)
conda env create -f environment.yml
conda activate compmethods-dev

# Using pip
pip install -e .
```

### Code Formatting and Linting
```bash
# Format code with black and fix line lengths
make format

# Alternative direct commands
black . -l 79
linecheck . --fix
```

### Testing
```bash
# Run all tests (excluding those marked 'local')
make test

# Run specific test file
pytest tests/test_add_junk.py

# Run tests with coverage
pytest -m 'not local' --cov=./ --cov-report=xml
```

### Documentation
```bash
# Build the Jupyter Book
make documentation

# Clean and rebuild
jupyter-book clean docs/book
jupyter-book build docs/book
```

### Package Management
```bash
# Install package in development mode
make install

# Update version and changelog
make changelog
```

## Architecture and Structure

### Directory Organization
- `code/` - Example code organized by chapter (e.g., `code/NumPyIntro/`, `code/gmm/`, `code/mle/`)
- `data/` - Data files for examples, organized by chapter/topic
- `docs/book/` - Jupyter Book content with chapters in subdirectories:
  - `python/` - Python programming fundamentals (10 chapters)
  - `basic_empirics/` - Basic empirical methods
  - `basic_ml/` - Machine learning
  - `deep_learn/` - Deep learning
  - `struct_est/` - Structural estimation (MLE, GMM, SMM)
  - `git/` - Git and GitHub
  - `appendix/` - Glossary and appendix
- `images/` - Book images organized by topic
- `tests/` - Test suite (currently minimal)

### Key Configuration Files
- `Makefile` - Primary build automation with targets: `format`, `install`, `test`, `documentation`, `changelog`
- `setup.py` - Python package metadata and dependencies
- `environment.yml` - Conda environment specification
- `docs/book/_config.yml` - Jupyter Book configuration
- `docs/book/_toc.yml` - Book table of contents structure

### Testing Strategy
- Uses `pytest` with marker `'not local'` to exclude local-only tests
- Tests are organized to match code structure
- Code coverage tracked via Codecov in CI

### Documentation System
- Built with **Jupyter Book** (v0.11.3+)
- Uses **Sphinx** with extensions: `sphinx-exercise`, `sphinx-proof`, `sphinxcontrib-bibtex`
- References managed via BibTeX (`CompMethods_references.bib`)
- Deployed to GitHub Pages via CI/CD

## Development Workflow

### Code Organization
- Example code should be placed in `code/{topic}/` directories matching book chapters
- Data files go in `data/{topic}/` directories
- Images for book content go in `images/{topic}/` directories
- Tests should be added to `tests/` directory with meaningful names

### Adding New Content
1. Add markdown files to appropriate `docs/book/{topic}/` directory
2. Update `docs/book/_toc.yml` to include new chapter
3. Add example code to `code/{topic}/` directory
4. Add data files to `data/{topic}/` if needed
5. Add tests for new functionality
6. Update references in `CompMethods_references.bib` if citing new sources

### Version Management
- Version numbers follow semantic versioning
- Use `make changelog` to update version and generate changelog entries
- Changelog entries go in `changelog_entry.yaml` before running `make changelog`

## CI/CD Pipeline

Four GitHub Actions workflows:
1. `build_and_test.yml` - Builds and tests on multiple OS/Python versions
2. `check_format.yml` - Validates code formatting with black
3. `deploy_docs.yml` - Builds and deploys documentation to GitHub Pages
4. `docs_check.yml` - Validates documentation build

All workflows run on push and pull request events.

## Important Notes

- The book is **AGPL-3.0 licensed** - ensure contributions comply
- Python 3.10+ required (3.10 and 3.11 tested in CI)
- Use `-m 'not local'` when running tests to exclude local-only tests
- Code formatting: black with 79-character line limit + linecheck
- Bibliographic references use BibTeX format in `CompMethods_references.bib`
- The project follows open-source economics conventions from OpenSourceEcon
