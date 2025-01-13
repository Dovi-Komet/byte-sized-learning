---
layout: default
title: "Exceptions"
order: 30
---

Exceptions are Python's way of indicating that something has gone wrong during program execution. When an error occurs, Python raises an exception, which can be caught and handled to prevent the program from crashing.

---

## What Are Exceptions?

An exception is an event that disrupts the normal flow of a program. Python provides many built-in exceptions, such as `ValueError`, `TypeError`, and `ZeroDivisionError`.

### Example:
```python
# Raising a ValueError
num = int("abc")
```

### Output:
```plaintext
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 10: 'abc'
```

---

## Raising Exceptions

You can explicitly raise exceptions in your code using the `raise` keyword.

### Example:
```python
age = -5
if age < 0:
    raise ValueError("Age cannot be negative!")
```

### Output:
```plaintext
Traceback (most recent call last):
  File "<stdin>", line 3, in <module>
ValueError: Age cannot be negative!
```

---

## Handling Specific Exceptions

Use `try` and `except` blocks to handle specific exceptions.

### Example:
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

### Output:
```plaintext
Cannot divide by zero!
```

---

## Using the `as` Keyword

The `as` keyword lets you capture the exception object for more information.

### Example:
```python
try:
    num = int("abc")
except ValueError as e:
    print(f"Error occurred: {e}")
```

### Output:
```plaintext
Error occurred: invalid literal for int() with base 10: 'abc'
```

---

## Defining Custom Exceptions

You can create your own exceptions by subclassing the `Exception` class.

### Example:
```python
class NegativeValueError(Exception):
    pass

def check_positive(number):
    if number < 0:
        raise NegativeValueError("Negative values are not allowed!")

try:
    check_positive(-10)
except NegativeValueError as e:
    print(e)
```

### Output:
```plaintext
Negative values are not allowed!
```

---

Exceptions help identify and manage errors gracefully. In the next lesson, we’ll explore how to use the `finally` block to clean up resources after exception handling.
