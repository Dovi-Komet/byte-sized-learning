---
layout: default
title: "json Module"
order: 37
---

The `json` module allows you to work with JSON (JavaScript Object Notation), a lightweight data format commonly used for data exchange between systems and APIs.

---

## What Is JSON?

- JSON is a text-based format that represents structured data.
- It uses key-value pairs (similar to Python dictionaries) and arrays (similar to Python lists).
- JSON is widely used in APIs and web applications.

---

## Converting Python Objects to JSON

Use `json.dumps()` to convert Python objects like dictionaries or lists into JSON strings.

### Example: Python to JSON

```python
import json

data = {"name": "Alice", "age": 30, "city": "New York"}
json_string = json.dumps(data)
print(json_string)
```

### Output:

```plaintext
{"name": "Alice", "age": 30, "city": "New York"}
```

---

## Formatting JSON Strings

You can make JSON strings more readable by using the `indent` parameter.

### Example: Pretty-Printed JSON

```python
pretty_json = json.dumps(data, indent=4)
print(pretty_json)
```

### Output:

```plaintext
{
    "name": "Alice",
    "age": 30,
    "city": "New York"
}
```

---

## Converting JSON to Python Objects

Use `json.loads()` to parse a JSON string and convert it into a Python object (e.g., dictionary or list).

### Example: JSON to Python

```python
json_data = '{"name": "Alice", "age": 30, "city": "New York"}'
parsed_data = json.loads(json_data)
print(parsed_data)
print(parsed_data["name"])
```

### Output:

```plaintext
{'name': 'Alice', 'age': 30, 'city': 'New York'}
Alice
```

---

## Reading and Writing JSON Files

The `json` module also allows you to read from and write to JSON files.

### Example: Writing to a JSON File

```python
with open("data.json", "w") as file:
    json.dump(data, file, indent=4)
```

This creates a file named `data.json` with the following content:

```plaintext
{
    "name": "Alice",
    "age": 30,
    "city": "New York"
}
```

### Example: Reading from a JSON File

```python
with open("data.json", "r") as file:
    file_data = json.load(file)
    print(file_data)
```

### Output:

```plaintext
{'name': 'Alice', 'age': 30, 'city': 'New York'}
```

---

## Summary

- Use `json.dumps()` to convert Python objects into JSON strings.
- Use `json.loads()` to parse JSON strings into Python objects.
- Use `json.dump()` and `json.load()` to work with JSON files.
- JSON is a crucial format for data interchange, especially in APIs and web development.

Practice converting between Python objects and JSON, and working with JSON files to become proficient in handling structured data.
