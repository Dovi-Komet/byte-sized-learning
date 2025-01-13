---
layout: default
title: "Intro to Packages"
order: 34
---

A package in Python is a way to organize related modules into a directory structure. Packages help manage larger projects by grouping modules into logical collections.

---

## What Is a Package?

A package is simply a directory that contains an `__init__.py` file and one or more module files. The `__init__.py` file marks the directory as a Python package and can also include initialization code for the package.

### Example:

**Directory Structure:**
```plaintext
my_package/
    __init__.py
    module1.py
    module2.py
```

- `my_package`: The package directory.
- `__init__.py`: Initializes the package.
- `module1.py` and `module2.py`: Modules within the package.

---

## Creating a Package

1. Create a directory for your package.
2. Add an empty `__init__.py` file inside the directory.
3. Add module files to the directory.

---

### Example:

**Step 1: Create a Directory**
Create a directory named `my_package`.

**Step 2: Add Modules**
Add two files: `math_tools.py` and `string_tools.py`.

**File: `math_tools.py`**
```python
# math_tools.py
def add(a, b):
    return a + b

def multiply(a, b):
    return a * b
```

**File: `string_tools.py`**
```python
# string_tools.py
def capitalize_words(sentence):
    return " ".join(word.capitalize() for word in sentence.split())
```

**Step 3: Add an `__init__.py` File**
Create an empty `__init__.py` file. This file can remain empty or include package initialization code.

---

## Using a Package

You can import modules from the package using the `import` statement.

### Example:
```python
from my_package import math_tools, string_tools

print(math_tools.add(3, 5))  # Output: 8
print(string_tools.capitalize_words("hello world"))  # Output: Hello World
```

---

## Importing Specific Functions

You can also import specific components from the modules.

### Example:
```python
from my_package.math_tools import multiply

print(multiply(4, 7))  # Output: 28
```

---

## Nested Packages

Packages can contain sub-packages, allowing for even more organization.

**Directory Structure:**
```plaintext
my_package/
    __init__.py
    sub_package/
        __init__.py
        module3.py
```

You can access `module3` using:
```python
from my_package.sub_package import module3
```

---

Packages are essential for organizing large codebases and making them maintainable. In the next lesson, we’ll explore Python’s standard library and how to use its built-in packages.
