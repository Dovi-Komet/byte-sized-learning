---
layout: default
title: "Standard Library"
order: 34
---

Python includes a vast standard library that provides modules and functions for common tasks, eliminating the need to write everything from scratch. These built-in modules make Python versatile and powerful.

---

## What Is the Standard Library?

The standard library is a collection of modules that come pre-installed with Python. These modules provide functionality for:
- File handling
- System operations
- Math and random operations
- Working with dates and times
- Networking, and much more

---

## Commonly Used Modules

Here are some popular modules from the standard library:

1. **`os`**: Interact with the operating system (e.g., file and directory manipulation).
2. **`sys`**: Access system-specific parameters and functions.
3. **`datetime`**: Work with dates and times.
4. **`random`**: Generate random numbers.
5. **`json`**: Parse and write JSON data for working with structured information.

---

## Example: Using the `random` Module

The `random` module provides functions to generate random numbers and perform random operations.

### Example: Generate a Random Integer

```python
import random

number = random.randint(1, 10)  # Generate a random integer between 1 and 10
print("Random number:", number)
```

### Output:

```plaintext
Random number: 7  # (The actual number will vary.)
```

---

## Example: Using the `datetime` Module

The `datetime` module allows you to work with dates and times.

### Example: Getting the Current Date and Time

```python
from datetime import datetime

current_time = datetime.now()  # Get the current date and time
print("Current time:", current_time)
```

### Output:

```plaintext
Current time: 2025-01-03 12:34:56.789012  # (The actual output will vary.)
```

---

## Example: Using the `json` Module

The `json` module is used to parse JSON strings or write JSON data.

### Example: Parsing JSON Data

```python
import json

data = '{"name": "Alice", "age": 25}'
parsed_data = json.loads(data)  # Parse the JSON string into a Python dictionary
print("Name:", parsed_data["name"])
print("Age:", parsed_data["age"])
```

### Output:

```plaintext
Name: Alice
Age: 25
```

---

## Why Use the Standard Library?

- **Saves Time**: Avoid writing code for common tasks.
- **Reliable**: Pre-tested and optimized modules ensure stability.
- **Accessible**: No need for additional installations; included with Python.

---

## Summary

- The Python standard library provides a wide range of modules for various tasks, such as file handling, system operations, and data processing.
- Popular modules include `os`, `sys`, `datetime`, `random`, and `json`.
- Using these built-in modules simplifies your code and speeds up development.

Exploring the standard library is essential for efficient Python programming. Practice using these modules to discover their full potential.
