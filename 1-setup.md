# Setup

## Requirements

* Python 3.8 and above
  * (walrus operator in `documatic/patterns/packages.py`)

## Installation

* Install locally with `pip install -e .`
* Or install from pypi

```
pip install documatic
```

The project follows semantic versioning (SemVer) scheme.
It is currently on `v0.7.5`.

## Environment

The project uses the following environment variables:

| VARIABLE | DEFAULT VALUE | CONSUMED IN | PURPOSE |
|:---------|:--------------|:---|:----|
| DOCUMATIC_API_KEY |  | `documatic.utils.requests.post` | Sent as a header in an API request |
| DOCUMATIC_PROJECT_NAME | DefaultProject | `documatic.utils.requests.post` | Sent as a header in an API request | 
| DOCUMATIC_RUN_LOCALLY | False | `documatic.utils.requests.post` | The address of an API request depends on the value |
