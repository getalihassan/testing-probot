# documatic/utils/

* `utils/` subdirectory does not import code from other parts of the codebase
* It primarily contains small, independent functions

```{image} ../assets/utils_diagram.png
---
width: 400
---
```

_A selection of relevant functionality has been extracted._

## request.py

Contains a single function, `post`.

```python
post(endpoint: str, payload)

Gets the Documatic API key from system environment.
If the api key does not exist, it returns.
Posts the payload to the endpoint.
If the response status is not 200, returns None.
If the response status is 200, it returns the received message.
Makes REST request (POST) to a server.
```
