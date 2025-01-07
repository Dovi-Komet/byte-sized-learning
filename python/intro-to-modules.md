---
layout: default
title: "Intro to Modules"
order: 32
---

Modules in Python allow you to organize your code into separate files and reuse functionality. Python provides a vast collection of built-in modules, and you can also create your own.

## What Are Modules?

A module is simply a file containing Python code (functions, variables, or classes) that you can import into other files or scripts to use its functionality.

---

## Importing a Module

Use the `import` statement to bring in a module and access its functions or variables using the module name.

### Example: Importing a Module

```python
import math
print(math.sqrt(16))  # Access the sqrt function from the math module
```

### Output:

```plaintext
4.0
```

---

## Importing Specific Functions or Variables

You can import only the parts of a module you need using the `from ... import ...` syntax.

### Example: Importing Specific Functions

```python
from math import pi, sqrt
print("Value of pi:", pi)  # Use the imported pi variable
print("Square root of 25:", sqrt(25))  # Use the imported sqrt function
```

### Output:

```plaintext
Value of pi: 3.141592653589793
Square root of 25: 5.0
```

---

## Using Aliases for Modules or Functions

You can give modules or their components shorter names using the `as` keyword, which can make your code more concise.

### Example: Aliasing a Module

```python
import math as m
print(m.sqrt(16))  # Access sqrt function using the alias "m"
```

### Output:

```plaintext
4.0
```

### Example: Aliasing Functions

```python
from math import sqrt as square_root
print(square_root(9))  # Access sqrt using the alias "square_root"
```

### Output:

```plaintext
3.0
```

---

## Exploring Built-In Modules

Python comes with many built-in modules that you can use without installing anything. Some popular ones include:
- `math`: Provides mathematical functions and constants.
- `random`: Offers functions to generate random numbers.
- `os`: Interacts with the operating system.
- `datetime`: Works with dates and times.

### Example: Using the `random` Module

```python
import random
print(random.randint(1, 10))  # Generate a random integer between 1 and 10
```

---

## Summary

- **Modules** are files with Python code that you can import into other programs.
- Use `import` to bring in an entire module or `from ... import ...` to import specific components.
- Use aliases with the `as` keyword to simplify module or function names.
- Explore Python's built-in modules to access powerful functionality without additional coding.

Modules help you write clean, reusable, and organized code. In future lessons, we’ll explore creating your own modules and using external libraries.
