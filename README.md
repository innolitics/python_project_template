# Python Project Template

This repository holds a template for a Python project. Use it to kick start
your own.

It includes:

- Formatters
    - black
    - isort
- Linters
    - ruff
- Type checkers
    - mypy
- pre-commit adds hooks for:
    - check-yaml
    - check-case-conflict
    - debug-statements
    - detect-private-key
    - check-added-large-files
    - end-of-file-fixer
    - trailing-whitespace
    - ruff
    - black
    - isort
    - prettier (yaml)
    - pip-tools (sync `requirements.in` with `requirements.txt`)
    - pyright
- github actions
    - dependabot (security updates)
    - ruff
    - black
    - pytest
    - mypy

## Usage

1. Install copier and copy the template repo:
    ```bash
    pip install copier
    copier copy . /path/to/your/new-project
    ```
2. Initialize a git repository in the new project folder and add all files
    introduced by `copier`:
    ```bash
    cd /path/to/your/new-project
    git init -b main
    git add -A
    ```
3. Read `new-project/CONTRIBUTING.md` to create the development
    environment for the new project.
4. Create your first commit (this should run pre-commit hooks):
    ```bash
    git commit -m "Initial commit"
    ```

