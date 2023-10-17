# Setting up the development environment

1. Create a new virtual environment and activate it:
    ```bash
    python -m venv .venv
    source .venv/bin/activate
    ```
2. Install development packages (linters, etc.):
    ```bash
    pip install -r requirements-dev.txt
    ```
3. Install pre-commit hooks:
    ```bash
    pre-commit install
    ```

# Dependency management

[pip-tools](https://pypi.org/project/pip-tools/) is used to keep requirements
pinned properly.

Define requirements as usual in the `requirements-*.in` files and
`pip-compile` will generate the corresponding txt file. E.g.,
`pip-compile requirements-dev.in` will generate requirements-dev.txt.

Both `.in` and `.txt` files will be tracked by git, and
they are synced with a pre-commit hook (i.e., `pip-compile` is run
automatically during each commit).

To install the dependencies, use `pip-sync`, e.g.,
```bash
pip-sync requirements-dev.txt`
```
