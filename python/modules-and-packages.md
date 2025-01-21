---
title: "Modules and Packages"
order: 25
---

# Modules and Packages

In Python, **modules** and **packages** allow you to organize code into smaller, reusable, and maintainable components. They help structure projects efficiently, especially as they grow larger.

---

## What is a Module?

A **module** is a file containing Python definitions and code. The filename has a `.py` extension.

### Example:
Create a file `math_operations.py`:
```python
# math_operations.py

def add(a, b):
    return a + b

def subtract(a, b):
    return a - b
```

Use the module in another file:
```python
import math_operations

print(math_operations.add(5, 3))       # Output: 8
print(math_operations.subtract(5, 3)) # Output: 2
```

---

## Importing Modules

You can import a module in several ways:

1. **Import Entire Module**:
   ```python
   import math_operations
   print(math_operations.add(2, 3))  # Access with module name
   ```

2. **Import Specific Functions**:
   ```python
   from math_operations import add
   print(add(2, 3))  # Access directly
   ```

3. **Import with Alias**:
   ```python
   import math_operations as mo
   print(mo.add(2, 3))  # Use alias
   ```

4. **Import All**:
   ```python
   from math_operations import *
   print(add(2, 3))  # Not recommended for large modules
   ```

---

## Built-in Modules

Python comes with many built-in modules. You can use them without installing anything.

### Example:
```python
import math
import random

print(math.sqrt(16))         # Output: 4.0
print(random.randint(1, 10)) # Output: Random number between 1 and 10
```

---

## What is a Package?

A **package** is a collection of modules grouped into a directory with an optional `__init__.py` file. The `__init__.py` file can be empty or contain initialization code for the package.

### Structure:
```
my_package/
    __init__.py
    module1.py
    module2.py
```

### Example:
1. Create a package:
    - `my_package/__init__.py`:
      ```python
      print("Initializing my_package")
      ```

    - `my_package/module1.py`:
      ```python
      def greet(name):
          return f"Hello, {name}!"
      ```

    - `my_package/module2.py`:
      ```python
      def farewell(name):
          return f"Goodbye, {name}!"
      ```

2. Use the package:
    ```python
    from my_package import module1, module2

    print(module1.greet("Alice"))   # Output: Hello, Alice!
    print(module2.farewell("Alice")) # Output: Goodbye, Alice!
    ```

---

## Installing and Using Third-Party Packages

Python has a rich ecosystem of third-party packages available through the **Python Package Index (PyPI)**.

1. **Installing Packages**:
   Use `pip`, the package installer for Python.
   ```bash
   pip install requests
   ```

2. **Using Installed Packages**:
   ```python
   import requests

   response = requests.get("https://api.github.com")
   print(response.status_code)  # Output: 200
   ```

---

## Relative Imports

Relative imports are used within packages to import from other modules in the same package.

### Example:
In `my_package/module1.py`:
```python
from .module2 import farewell

def greet_and_farewell(name):
    return f"{greet(name)} {farewell(name)}"
```

---

## Best Practices

1. Use **modules** to split large scripts into smaller, logical units.
2. Group related modules into **packages** for better organization.
3. Avoid circular imports by structuring your code logically.
4. Use descriptive names for modules and packages.
5. Document your modules and functions with comments or docstrings.

---

## Practice Exercises

1. **Create a Module**:
   - Write a module `calculator.py` with functions `add`, `subtract`, `multiply`, and `divide`.
   - Import and use these functions in another script.

2. **Create a Package**:
   - Create a package `utilities` with modules:
     - `file_utils.py` for file-related functions.
     - `string_utils.py` for string-related functions.
   - Test the package in a separate script.

3. **Use Built-in Modules**:
   - Write a script that uses the `os` and `sys` modules to display the current working directory and command-line arguments.

Modules and packages are essential tools for creating clean, reusable, and well-organized Python programs.