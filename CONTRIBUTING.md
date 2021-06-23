# Contributing

> **Prerequisites**:
>
> Install [Poetry](https://github.com/python-poetry/poetry) by following the [official installation instructions](https://github.com/python-poetry/poetry#installation). Optionally (but recommended), configure Poetry to create a virtual environment in a folder named `.venv` within the root directory of the project:
>
> ```bash
> poetry config virtualenvs.in-project true
> ```

To create a development environment and install the runtime and development dependencies, run:

```bash
poetry install -E enum -E union
poetry run pre-commit install --install-hooks
```

Then you can make your changes, and commit them with

```
poetry run git commit # Pre-commit hooks should be run, checking your code
```

Every commit is checked with pre-commit hooks for:

- style consistency with [flake8](https://flake8.pycqa.org/en/latest/manpage.html)
- type safety with [mypy](http://mypy-lang.org/)
- test conformance by running [tests](./tests) with [pytest](https://docs.pytest.org/en/latest/)
  - You can run `poetry run pytest` from the command line.
