---
layout: default
title: "Standard Library"
order: 35
---

The Python Standard Library is a collection of modules and packages that come pre-installed with Python. It provides a wide range of functionality, such as handling file I/O, working with data formats, network communication, and more. By using the standard library, you can avoid reinventing the wheel and speed up development.

---

## What Is the Standard Library?

The standard library includes modules for various tasks, such as:

- File I/O (`open()`, `os` module)
- Data manipulation (`json`, `csv`)
- String handling (`re` for regular expressions)
- Date and time (`datetime`, `time`)
- Mathematical operations (`math`, `random`)

These modules are included with Python and are available for immediate use without needing to install anything extra.

---

## How to Use the Standard Library

You can import and use the standard library modules like you would any other Python module.

### Example: Using the `os` Module
The `os` module provides functions to interact with the operating system, such as working with files and directories.

```python
import os

# Get the current working directory
current_directory = os.getcwd()
print(current_directory)
```

### Output:
```plaintext
/path/to/your/current/directory
```

---

### Example: Using the `datetime` Module
The `datetime` module allows you to work with dates and times.

```python
import datetime

# Get the current date and time
now = datetime.datetime.now()
print(now)
```

### Output:
```plaintext
2025-01-14 10:30:45.123456
```

---

## Useful Modules in the Standard Library

Here are some commonly used modules in the standard library:

- **`os`**: Provides functions for interacting with the operating system (e.g., file operations, environment variables).
- **`datetime`**: Supplies classes for working with dates and times.
- **`math`**: Offers mathematical functions like trigonometric operations, logarithms, etc.
- **`random`**: Used to generate random numbers and perform random selections.
- **`json`**: Allows working with JSON data, which is often used in web applications.
- **`sys`**: Provides access to system-specific parameters and functions.

---

## Finding Modules in the Standard Library

You can check the official Python documentation to explore more about the standard library:

- [Python Standard Library Documentation](https://docs.python.org/3/library/){:target="_blank"}

Alternatively, you can list the available modules on your system using the `help()` function in the Python shell:

```python
help("modules")
```

---

The Python standard library is vast and extremely useful, offering built-in tools to help solve common problems. In the next lesson, we’ll dive into some of the most commonly used modules, starting with `os`, to explore their capabilities in more detail.
