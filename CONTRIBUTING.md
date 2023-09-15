# pip-tools
We use [pip-tools](https://pypi.org/project/pip-tools/) to keep our requirements pinned properly.

We define our requirements as usual in requirements.in and requirements-dev.in
`pip-compile` will generate a requirements.txt
`pip-compile requirements-dev.in` will generate requirements-dev.txt

Both: in and .txt files will be tracked by git.
We keep them synced with a pre-commit hook.

To install these dependencies, we use the other command of pip-tools: `pip-sync`.
pip-sync ingests the generated .txt files:
`pip-sync requirements-dev.txt`

# pre-commit
Configured in the file `.pre-commit-config.yaml`. Use `pre-commit install` to install the hooks
For pre-commit to work with pyright, we have to install the dependencies in requirements.txt in a local
virtual env. Following: https://github.com/RobertCraigie/pyright-python#pre-commit

```
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

