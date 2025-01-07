---
layout: default
title: "APIs with requests"
order: 76
---

The `requests` library makes it easy to interact with APIs.

### Making a GET Request

Example:

```python
import requests

response = requests.get("https://api.github.com")
print(response.status_code)
print(response.json())
```

### Expected Output (example data)

```plaintext
200
{'current_user_url': 'https://api.github.com/user', ...}
```

### Sending Data with a POST Request

Example:

```python
data = {"key": "value"}
response = requests.post("https://httpbin.org/post", json=data)
print(response.json())
```

### Expected Output (example data)

```plaintext
{'json': {'key': 'value'}, ...}
```

APIs are essential for integrating external services into your Python applications.
