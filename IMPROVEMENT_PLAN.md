# Improvement Plan: python_fundamental

## Overview
Python learning scripts with no type annotations, no tests, and no structure. Good for initial learning but needs scaffolding to be a useful reference or portfolio piece.

## Improvements

### Modernization & Code Quality
- Add type hints to all function signatures (Python 3.13+ syntax: `str | None`, `list[int]`, etc.)
- Replace `%` and `.format()` string formatting with f-strings throughout
- Add `ruff` for linting and `black` for formatting
- Add a `pyproject.toml` with tool configuration

### Testing
- Add pytest unit tests for every function — creates a learning loop where exercises are self-verifying
- Organize tests in a `tests/` folder mirroring the script structure
- Add `pytest-cov` for coverage reporting
- Add GitHub Actions CI to run tests on every push

### Structure
- Organize scripts into topic folders: `01_data_types/`, `02_control_flow/`, `03_functions/`, `04_oop/`, `05_file_io/`, `06_modules/`
- Add a root `README.md` listing all topics with links to each folder

### Documentation
- Add module-level docstrings to each script explaining the topic covered
- Add docstrings to all functions with examples (enables `doctest` as a lightweight alternative to pytest)

### Advanced Topics
- Add exercises for: decorators, generators, context managers, async/await, dataclasses, pathlib, and the `collections` module

### DevOps
- Add a `requirements-dev.txt` or `[tool.poetry.dev-dependencies]` group for pytest, ruff, and black
- Add a pre-commit config for `ruff` and `black`
