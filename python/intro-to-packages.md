---
layout: default
title: "Intro to Packages"
order: 33
---

A package is a collection of modules organized into directories with a special `__init__.py` file. Packages allow you to structure larger projects by grouping related modules together.

## What Is a Package?

- A **module** is a single Python file containing code.
- A **package** is a directory containing one or more modules, along with an `__init__.py` file that identifies the directory as a package.

---

## Creating a Package

### Steps to Create a Package

1. Create a directory to serve as the package (e.g., `my_package`).
2. Add an `__init__.py` file inside the directory. This file can be empty or include initialization code for the package.
3. Add one or more Python files (modules) inside the package directory.

### Example Directory Structure

```plaintext
my_package/
    __init__.py
    math_utils.py
    string_utils.py
```

---

## Example: Package Creation

### `math_utils.py`

```python
# File: my_package/math_utils.py
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

### `string_utils.py`

```python
# File: my_package/string_utils.py
def capitalize_words(text):
    return " ".join(word.capitalize() for word in text.split())
```

### `__init__.py`

```python
# File: my_package/__init__.py
# Initialize the package (optional)
print("my_package has been imported.")
```

---

## Using a Package

To use the package, ensure that the package directory is in the same directory as your script or is part of your Python path.

### Example: Importing from a Package

```python
from my_package import math_utils, string_utils

result = math_utils.add(2, 3)
formatted_text = string_utils.capitalize_words("hello world")

print("Addition Result:", result)
print("Formatted Text:", formatted_text)
```

### Output:

```plaintext
my_package has been imported.
Addition Result: 5
Formatted Text: Hello World
```

---

## Importing All Modules

You can use the `*` syntax to import all modules from a package if the `__init__.py` file specifies an `__all__` list.

### Example: `__init__.py` with `__all__`

```python
# File: my_package/__init__.py
__all__ = ["math_utils", "string_utils"]
```

---

## Organizing Large Projects

Packages make it easy to organize code in larger projects by grouping related functionality. For example, you might have:

```plaintext
ecommerce/
    __init__.py
    products/
        __init__.py
        product.py
        inventory.py
    orders/
        __init__.py
        order.py
        payment.py
```

---

## Summary

- A package is a directory containing modules and an `__init__.py` file.
- Use `from package_name import module_name` to access modules within a package.
- Organize related functionality into packages for better project structure.
- Use the `__init__.py` file for initialization or to define the package's public API.

Packages help you manage and organize code effectively in larger projects. Practice creating and using packages to improve your ability to structure complex applications.
