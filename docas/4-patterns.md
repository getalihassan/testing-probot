# documatic/patterns/

* `patterns/` subdirectory relies most on `utils/` (imports 6 times)
* It primarily contains small, independent functions
* Tom Titcombe <tom@documatic.com> is the inferred code owner

```{image} ../assets/patterns_diagram.png
---
width: 400
---
```

_A selection of relevant functionality has been extracted._

## tools.py

File has 48 lines added and 5 lines removed
in the past 4 weeks. Tom Titcombe <tom@documatic.com> is the inferred code owner.

```
read_packages(project_dir: Path) -> List[str]

This function reads a file called "requirements.txt"
in the project directory,
and if it exists
it reads the contents of the file into a list of strings.
Then it calls a function called "post"
with the contents of the file as a parameter.

Does not raise.
Reads files (`requirements.txt`)
and will likely error if they are not available.
```

## interactions.py


File has 68 lines added and 21 lines removed
in the past 4 weeks. Tom Titcombe <tom@documatic.com> is the inferred code owner.

```
detect_requests_calls(file_contents: str) -> bool

This function detects whether the file contains any requests.get() calls.
```

```
detect_fastapi_calls(file_contents: str) -> bool

The function detects FastAPI calls
by looking for the string 'FastAPI'
or 'from fastapi' or 'import fastapi' in the file.
Does not raise.
```

```
describe_file_architecture(file_path: Path) -> str

The function has two parts:
1. Read the file and store its contents in a variable named "full_contents".
2. Check the contents of the file and return a string if any of the architecture checks pass

Does not raise.
```

```
describe_api(filepath: Path) -> Optional[str]

The function takes a filepath and returns a string.
It calls a function to check if the file contains an API.
If it does, it extracts every function in the file
and calls `summarise_function` to get a summary.

Does not raise.
```
