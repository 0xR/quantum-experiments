## Getting started

Make sure you have `uv` installed. When you're on Mac run `brew install uv`

Next create a venv by running `uv venv`

Now run

```
uv pip compile pyproject.toml --generate-hashes -o requirements.lock
uv pip sync requirements.lock
```

to install the dependencies

## Jupyter Notebook Pre-commit Setup

This repository uses pre-commit hooks to automatically clean Jupyter notebook outputs before committing. This keeps our git history clean and focused on the actual notebook content.

After installing dependencies, just run:
```
pre-commit install
```

Now whenever you commit changes that include Jupyter notebooks, the outputs will be automatically stripped before committing. 

If you need to manually clean notebook outputs, you can run:
```
pre-commit run nbstripout
```

Note: The pre-commit configuration is already set up in `.pre-commit-config.yaml`
