---
title: "Working with JSON"
order: 30
---

# Working with JSON in Python

JSON (JavaScript Object Notation) is a lightweight data format commonly used for data exchange between systems. Python provides the **`json`** module to parse JSON data and convert Python objects to JSON.

---

## Importing the `json` Module
```python
import json
```

---

## JSON Basics

### Example JSON String
```json
{
  "name": "Alice",
  "age": 25,
  "skills": ["Python", "Data Analysis", "Machine Learning"],
  "is_student": false
}
```

### JSON vs. Python

| JSON Data Type | Python Data Type |
|----------------|------------------|
| Object         | Dictionary       |
| Array          | List             |
| String         | String           |
| Number         | int or float     |
| Boolean        | bool             |
| null           | None             |

---

## Reading JSON

### Parse JSON String to Python Object
```python
json_string = '{"name": "Alice", "age": 25, "is_student": false}'
data = json.loads(json_string)

print(data)         # Output: {'name': 'Alice', 'age': 25, 'is_student': False}
print(data['name']) # Output: Alice
```

---

## Writing JSON

### Convert Python Object to JSON String
```python
python_data = {
    "name": "Alice",
    "age": 25,
    "skills": ["Python", "Data Analysis"],
    "is_student": False
}

json_string = json.dumps(python_data)
print(json_string)
```

#### Indented and Sorted JSON
```python
json_string = json.dumps(python_data, indent=4, sort_keys=True)
print(json_string)
```

---

## Working with Files

### Reading JSON from a File
```python
with open("data.json", "r") as file:
    data = json.load(file)

print(data)
```

### Writing JSON to a File
```python
with open("data.json", "w") as file:
    json.dump(python_data, file, indent=4)
```

---

## Handling Errors

### Invalid JSON
```python
try:
    invalid_json = '{"name": "Alice", "age": 25,}'
    data = json.loads(invalid_json)
except json.JSONDecodeError as e:
    print("Invalid JSON:", e)
```

---

## Advanced Usage

### Custom Serialization
Python objects that are not directly serializable (e.g., `datetime`) can be handled using a custom serializer.

#### Serializing `datetime`
```python
from datetime import datetime

data = {"event": "Launch", "date": datetime.now()}

def custom_serializer(obj):
    if isinstance(obj, datetime):
        return obj.isoformat()
    raise TypeError("Type not serializable")

json_string = json.dumps(data, default=custom_serializer)
print(json_string)
```

#### Deserializing `datetime`
```python
def custom_deserializer(dct):
    if "date" in dct:
        dct["date"] = datetime.fromisoformat(dct["date"])
    return dct

json_string = '{"event": "Launch", "date": "2025-01-16T10:30:00"}'
data = json.loads(json_string, object_hook=custom_deserializer)
print(data)
```

---

## Practical Examples

### API Response Simulation
```python
response = '{"status": "success", "data": {"id": 123, "name": "Alice"}}'
data = json.loads(response)
print(data["data"]["name"])  # Output: Alice
```

### Configuration File
```python
config = {
    "theme": "dark",
    "language": "en",
    "autosave": True
}

with open("config.json", "w") as file:
    json.dump(config, file, indent=4)

# Reading the configuration
with open("config.json", "r") as file:
    config = json.load(file)
    print(config["theme"])  # Output: dark
```

---

## Best Practices

1. **Validate JSON Data**:
   - Use `try-except` to handle potential parsing errors.

2. **Use Indentation**:
   - Add `indent=4` when writing JSON to improve readability.

3. **Serialize Non-Standard Objects**:
   - Provide a `default` function to handle custom objects.

---

## Practice Exercises

1. **JSON Parsing**:
   - Write a script to parse a JSON string representing a list of users and print their names.

2. **File Handling**:
   - Create a program that writes a dictionary to a JSON file and reads it back.

3. **Custom Serialization**:
   - Serialize a list of events with `datetime` objects to JSON and deserialize them back.

JSON is a powerful format for data exchange, and Python's `json` module makes it easy to work with. Mastering this module is essential for handling APIs, configuration files, and more.