# Python Project Template

Install copier

```
pip install copier
```

```
copier copy python_project_template your_project
```

Read `your_project/CONTRIBUTING.md` to kick-start your new project.

```
cd your_project
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python -m pre-commit install
```

It includes:

Formatters:
- black
- isort

Linters:
- ruff

Static analyzers:
- pyright

pre-commit adds hooks for:
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
- pip-tools (sync requirements.in with requirements.txt)
- pyright

github actions:
- dependabot (security updates)
- ruff
- black
- pytest

