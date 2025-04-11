## Getting started

Make sure you have `uv` installed. When you're on Mac run `brew install uv`

Next create a venv by running `uv venv`

Now run

```
uv pip compile pyproject.toml --generate-hashes -o requirements.lock
uv pip sync requirements.lock
```

to install the dependencies
