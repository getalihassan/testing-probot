# Setup

<!---Documatic-section-Requirements-start--->
## Requirements

No exact compatable Python version has been detected.
Versions below 3.8 are compatable.
<!---Documatic-section-Requirements-end--->

<!---Documatic-section-Installation-start--->
## Installation


* Run `pip install -e .` in top-level directory to
install package in local directory.

* Install from pypi with 
```python
                pip install docserver
```
<!---Documatic-section-Installation-end--->

<!---Documatic-section-Environment Variables-start--->
## Environment Variables

<!---Documatic-block-env-vars-start--->
The following environment variables are read from the system:

<!---Documatic-block-env-reads-start--->
|VARIABLE|FILE|DEFAULT VALUE|
|:---|:---|:---|
|DOCUMATIC_NOTION_API_KEY|`docserver.cli`||
|docserver_API_KEY|`docserver.utils.auth`, `docserver.utils.config`||
|docserver_RUN_LOCALLY|`docserver.utils.auth`, `docserver.utils.config`||
|docserver_PROJECT_NAME|`docserver.utils.config`||
|KEY|`docserver.interactions.tools`||
<!---Documatic-block-env-reads-end--->

The following environment variables are written to the system:

<!---Documatic-block-env-writes-start--->
|VARIABLE|FILE|VALUE|
|:---|:---|:---|
|docserver_PROJECT_NAME|`docserver.utils.config`||
|docserver_RUN_LOCALLY|`docserver.utils.config`||
|KEY|`docserver.interactions.tools`||
<!---Documatic-block-env-writes-end--->
<!---Documatic-block-env-vars-end--->
<!---Documatic-section-Environment Variables-end--->

<!---Documatic-section-CLI-start--->
## CLI

The project has the following CLI commands:

* `docserver` runs `docserver.cli.generate_documentation`

Run a CLI command in a terminal to execute.
<!---Documatic-section-CLI-end--->