---
layout: default
title: "json Module"
order: 38
---

The `json` module in Python provides tools for working with JSON (JavaScript Object Notation), a widely used format for data exchange. It allows you to convert Python objects to JSON strings and vice versa.

---

## Importing the `json` Module

To use the `json` module, import it into your program:

```python
import json
```

---

## Commonly Used Functions in the `json` Module

### Converting Python Objects to JSON (Serialization)

The `json.dumps()` function converts a Python object into a JSON string.

```python
import json

# Python object (dictionary)
data = {"name": "Alice", "age": 25, "city": "New York"}

# Convert Python object to JSON string
json_string = json.dumps(data)
print("JSON String:", json_string)
```

#### Explanation:
- `dumps()` means "dump as a string."
- The output is a JSON-formatted string.

---

### Writing JSON to a File

The `json.dump()` function writes JSON data to a file.

```python
# Write JSON data to a file
with open("data.json", "w") as file:
    json.dump(data, file)
print("JSON data written to file.")
```

---

### Reading JSON from a String (Deserialization)

The `json.loads()` function parses a JSON string into a Python object.

```python
# JSON string
json_string = '{"name": "Alice", "age": 25, "city": "New York"}'

# Convert JSON string to Python object
parsed_data = json.loads(json_string)
print("Parsed Data:", parsed_data)
```

#### Explanation:
- `loads()` means "load from a string."
- The result is a Python dictionary.

---

### Reading JSON from a File

The `json.load()` function reads JSON data from a file.

```python
# Read JSON data from a file
with open("data.json", "r") as file:
    loaded_data = json.load(file)
print("Loaded Data:", loaded_data)
```

---

## Formatting Options

The `json.dumps()` function supports formatting options like `indent` and `sort_keys` for better readability.

```python
# Convert Python object to a formatted JSON string
formatted_json = json.dumps(data, indent=4, sort_keys=True)
print("Formatted JSON:\n", formatted_json)
```

---

## Example: JSON Workflow

Here’s a complete example of creating, writing, reading, and parsing JSON data:

```python
import json

# Python dictionary
data = {"name": "Bob", "age": 30, "city": "London"}

# Write JSON to a file
with open("example.json", "w") as file:
    json.dump(data, file)

# Read JSON from the file
with open("example.json", "r") as file:
    loaded_data = json.load(file)

print("Original Data:", data)
print("Loaded Data:", loaded_data)
```

---

## Documentation

For more information, visit the [official Python documentation](https://docs.python.org/3/library/json.html){:target="_blank"}.

---

The `json` module is a powerful tool for working with structured data in Python. In the next lesson, we’ll explore the `random` module for generating random numbers and data.
