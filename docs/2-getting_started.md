# Getting Started

## Codebase Structure

Documatic has a well-segmented structure,
with a max folder depth of 1.\
45 python files in total.

```
|- documatic
   |- __init__.py
   |- cli.py
   |- docs/
   |- integration/
   |- patterns/
   |- structure/
   |- summaries/
   |_ utils/
```

```{image} ../assets/code_sequence_diagram.png
---
width: 400
---
```

## Interactions

At a high-level:

* The codebase makes REST requests (POST) in 1 location
  * `documatic.utils.requests.post` makes POST requests to address at `aws`

```{image} ../assets/post_request_diagram.png
---
width: 400
---
```

## Entrypoints

### CLI

The project has the following CLI commands:

| Command | Args | Function Executed |
|:---|:---|:---|
| `documatic` | "document" (default="technical") | `documatic.cli.generate_documentation`
| `documatic-init` | - | `documatic.utils.config.create_config` |

#### `documatic`

```
generate_documentation() -> None

This function takes a command-line argument, and if it is  "changelog", it calls another function to generate a changelog.
Otherwise, this function generates a technical document in markdown format.
The current working directory must be the root of the project
for which documentation is to be generated. Does not raise.
```

#### `documatic-init`

```
create_config()

The code has a high cyclomatic complexity.
Create a minimal config file.
Must be called when project root is current working directory.
Some information must be filled out by a user, such as `api_key`.
`srcdir` is assumed to be `src` or just home directory.
Writes config file to CWD / ".documatic.ini" Does not raise.
```

Run a CLI command in a terminal to execute.

### Imports

* There are 1 source code objects in top-level `__main__`/`__init__`
* These entrypoints are broken down into the following modules:
  * `documatic.utils` has 1 entrypoints

### `parse_config`

* Stored in `documatic/utils/config.py`
 
```
parse_config(project_root: Path) -> Dict

The function takes a path to a project root directory and returns a config.
It reads a .documatic.ini file or pyproject.toml file and parses the config.
Loads environment variables stored in `.env` via `python-dotenv`
```