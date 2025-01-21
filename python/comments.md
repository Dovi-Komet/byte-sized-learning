---
title: "Comments"
order: 4
---

# Comments

Comments are an essential part of writing clean and maintainable code. They allow you to explain your code to others (or your future self) and make your programs easier to understand.

## What are Comments?

- Comments are lines in your code that are ignored by the Python interpreter.
- They are used to document your code and provide explanations.

## Why Use Comments?

1. **Explain Code**: Help others (and yourself) understand your logic.
2. **Debugging**: Temporarily disable parts of your code.
3. **Documentation**: Describe what your code does and why.

## Writing Comments in Python

### Single-Line Comments

Single-line comments start with a `#` symbol. Everything after the `#` is ignored by Python.

Example:
```python
# This is a single-line comment
print("Hello, World!")  # This prints a message
```

### Multi-Line Comments

Python does not have a specific syntax for multi-line comments. However, you can use a series of single-line comments or a multi-line string (enclosed in triple quotes) to achieve the same effect.

#### Using Single-Line Comments:
```python
# This is a multi-line comment
# Each line starts with a '#'
print("Multi-line comments example")
```

#### Using Multi-Line Strings:
Multi-line strings are enclosed in triple quotes (`'''` or `"""`). While they are technically strings, they can be used as comments if they are not assigned to a variable.

```python
"""
This is a multi-line comment.
It can span multiple lines.
"""
print("Using multi-line strings for comments")
```

## Best Practices for Comments

1. **Be Concise**: Write short and clear comments.
2. **Avoid Redundancy**: Don't explain what is already obvious from the code.
   - Poor comment:
     ```python
     x = 10  # Assign 10 to x
     ```
   - Better comment:
     ```python
     x = 10  # Initial value for the counter
     ```
3. **Update Comments**: Ensure comments are accurate as the code evolves.
4. **Use Docstrings**: Use triple-quoted strings to document functions, classes, or modules.

### Example of Docstrings:
```python
def greet(name):
    """
    This function greets a person by name.
    
    Parameters:
    name (str): The name of the person to greet.
    
    Returns:
    None
    """
    print(f"Hello, {name}!")
```

## Practice Exercises

1. Write a Python script with:
   - A single-line comment explaining the purpose of the script.
   - A multi-line comment providing more detailed documentation.
2. Create a function and document it using a docstring.

With comments, you can make your code readable, professional, and easier to maintain!