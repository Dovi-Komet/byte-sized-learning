---
layout: default
title: "Custom Modules"
order: 32
---

Creating custom modules allows you to organize your code into reusable components, making your programs easier to manage and maintain.

## What Is a Custom Module?

A custom module is simply a Python file (`.py`) containing code such as functions, classes, or variables. You can import this file into other Python files to reuse its functionality.

---

## Creating a Module

1. Create a new file named `my_module.py`.
2. Add the following code to define a simple function:

```python
# File: my_module.py
def greet(name):
    return f"Hello, {name}!"
```

---

## Using Your Module

To use the custom module, create another file (e.g., `main.py`) in the same directory and import your module using the `import` statement.

### Example: Importing a Custom Module

```python
# File: main.py
import my_module

message = my_module.greet("Alice")
print(message)
```

### Output:

```plaintext
Hello, Alice!
```

---

## Importing Specific Functions

If you only need certain functions from your module, you can use the `from ... import ...` syntax.

### Example: Importing a Specific Function

```python
from my_module import greet

print(greet("Bob"))
```

### Output:

```plaintext
Hello, Bob!
```

---

## Adding More Functions or Variables

You can expand your custom module by adding more functionality.

### Example: Expanded `my_module.py`

```python
# File: my_module.py
def greet(name):
    return f"Hello, {name}!"

def add(a, b):
    return a + b

PI = 3.14159
```

### Using the Expanded Module

```python
# File: main.py
import my_module

print(my_module.greet("Alice"))
print("Sum:", my_module.add(5, 3))
print("Value of PI:", my_module.PI)
```

### Output:

```plaintext
Hello, Alice!
Sum: 8
Value of PI: 3.14159
```

---

## Organizing Custom Modules

If your project grows, you can organize modules into folders. Create a folder (e.g., `my_package`) and add an `__init__.py` file to make it a package. We’ll explore this in a future lesson.

---

## Summary

- A custom module is any Python file that you can import into another script.
- Use `import` to bring in the entire module or `from ... import ...` to import specific components.
- Expand your modules to include multiple functions, variables, or classes for reusability.
- Organize modules into folders for better project structure as your codebase grows.

Creating custom modules helps you write modular and reusable code. Practice making and importing your own modules to enhance your coding efficiency.
