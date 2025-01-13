---
layout: default
title: "Intro to Modules"
order: 32
---

A module in Python is a file that contains Python code, such as functions, variables, and classes. Modules allow you to organize your code into reusable components, making it easier to manage and maintain.

---

## What Are Modules?

Modules are Python files with the extension `.py`. By importing modules, you can use the code they contain in your program.

### Example:
If you have a file named `my_module.py` with the following code:
```python
# my_module.py
def greet(name):
    return f"Hello, {name}!"
```

You can use it in another file:
```python
import my_module

print(my_module.greet("Alice"))
```

### Output:
```plaintext
Hello, Alice!
```

---

## Built-In Modules

Python comes with many built-in modules, such as `math`, `os`, and `random`. These modules provide pre-written code for common tasks.

### Example: Using the `math` Module
```python
import math

print(math.sqrt(16))  # Calculate the square root
```

### Output:
```plaintext
4.0
```

---

## Importing Specific Functions or Variables

You can import specific components from a module instead of the entire module.

### Example:
```python
from math import pi, sqrt

print(pi)          # Print the value of π
print(sqrt(25))    # Calculate the square root
```

### Output:
```plaintext
3.141592653589793
5.0
```

---

## Renaming Modules with `as`

You can use the `as` keyword to give a module or function an alias.

### Example:
```python
import math as m

print(m.sqrt(49))  # Use the alias `m`
```

### Output:
```plaintext
7.0
```

---

## Finding Available Functions in a Module

The `dir()` function lists all attributes (functions, variables, etc.) of a module.

### Example:
```python
import math

print(dir(math))  # List all attributes of the math module
```

---

## Writing Your Own Module

You can create your own module by saving Python code in a `.py` file and importing it into another script.

### Example:
Create a file named `utilities.py`:
```python
# utilities.py
def add(a, b):
    return a + b
```

Then use it in another file:
```python
import utilities

print(utilities.add(3, 5))  # Output: 8
```

---

Modules help you organize your code and reuse functionality efficiently. In the next lesson, we’ll explore how to create and use custom modules in more detail.
