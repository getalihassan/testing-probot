# Developers

## Requirements

* Install developer requirements with `pip install -r requirements-dev.txt`
* Install local package with `pip install -e .`

## Testing

* Documatic uses pytest and unittest testing libraries
* Tests are present in `tests/`
* Run `pytest tests/` to run tests


## CI

The project uses GitHub Actions for CI/CD.

| CI File | Purpose |
|:----|:----|
| test-integration | Executes on pull request for any branch |
| test-unit | Executes on pull request for any branch. Runs linting (with black, isort). Run tests (with pytest) |
