---
layout: default
title: "Custom Modules"
order: 33
---

Creating custom modules allows you to organize and reuse your own Python code across multiple programs. A custom module is simply a `.py` file containing functions, variables, or classes that can be imported and used in other files.

---

## Creating a Custom Module

1. Create a Python file (e.g., `my_module.py`) with your desired code.
2. Save it in the same directory as your main script or ensure it’s in the Python path.
3. Import the module in your main script to use its contents.

### Example:

**File: `my_module.py`**
```python
# my_module.py
def greet(name):
    return f"Hello, {name}!"

def add_numbers(a, b):
    return a + b
```

**File: `main.py`**
```python
# main.py
import my_module

print(my_module.greet("Alice"))  # Output: Hello, Alice!
print(my_module.add_numbers(5, 7))  # Output: 12
```

---

## Importing Specific Functions or Variables

You can import only the components you need using the `from ... import ...` syntax.

### Example:
```python
from my_module import greet

print(greet("Bob"))  # Output: Hello, Bob!
```

---

## Using Aliases for Modules

You can rename your custom module using the `as` keyword for convenience.

### Example:
```python
import my_module as mm

print(mm.greet("Charlie"))  # Output: Hello, Charlie!
```

---

## Organizing Modules in Directories

To structure larger projects, you can organize modules into directories. These directories must contain an `__init__.py` file to be recognized as a package.

### Example:

**Directory Structure:**
```plaintext
my_package/
    __init__.py
    helpers.py
    utilities.py
```

**File: `helpers.py`**
```python
# helpers.py
def say_hello():
    return "Hello from helpers!"
```

**File: `main.py`**
```python
# main.py
from my_package.helpers import say_hello

print(say_hello())  # Output: Hello from helpers!
```

---

Custom modules make your code more reusable and maintainable. In the next lesson, we’ll dive deeper into organizing modules into packages and using them effectively.
