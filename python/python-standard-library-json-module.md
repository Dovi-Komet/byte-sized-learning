---
layout: default
title: "Python Standard Library: `json` Module"
order: 34
---

The `json` module allows you to work with JSON data, which is a common format for exchanging data between systems.

### Converting Python Objects to JSON

Use `json.dumps()` to convert a Python object into a JSON string.

Example:

```python
import json
data = {"name": "Alice", "age": 30, "city": "New York"}
json_string = json.dumps(data)
print(json_string)
```

### Expected Output

```plaintext
{"name": "Alice", "age": 30, "city": "New York"}
```

### Converting JSON to Python Objects

Use `json.loads()` to convert a JSON string back into a Python object.

Example:

```python
json_data = '{"name": "Alice", "age": 30, "city": "New York"}'
parsed_data = json.loads(json_data)
print(parsed_data)
print(parsed_data["name"])
```

### Expected Output

```plaintext
{'name': 'Alice', 'age': 30, 'city': 'New York'}
Alice
```

The `json` module is essential for working with APIs and data interchange.