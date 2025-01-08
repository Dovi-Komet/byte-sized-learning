---
layout: default
title: "Numbers and Math"
order: 8
---

Python provides robust support for working with numbers and performing mathematical operations. There are three primary types of numbers in Python: integers, floats, and complex numbers.

## Number Types in Python

1. **Integer (`int`)**: Whole numbers, positive or negative, without a decimal point.
   ```python
   x = 10  # An integer
   y = -5  # A negative integer
   print(x, y)
   ```

2. **Float (`float`)**: Numbers that include a decimal point.
   ```python
   pi = 3.14  # A float
   e = -2.718 # A negative float
   print(pi, e)
   ```

3. **Complex Numbers (`complex`)**: Numbers with a real and imaginary part. Represented as `a + bj`.
   ```python
   z = 2 + 3j  # A complex number
   print(z.real, z.imag)  # Outputs the real and imaginary parts
   ```

## Basic Mathematical Operations

Python supports common arithmetic operators for basic math:

| Operator | Description            | Example          |
|----------|------------------------|------------------|
| `+`      | Addition               | `5 + 3 = 8`      |
| `-`      | Subtraction            | `10 - 4 = 6`     |
| `*`      | Multiplication         | `7 * 2 = 14`     |
| `/`      | Division               | `9 / 3 = 3.0`    |
| `//`     | Floor Division         | `9 // 2 = 4`     |
| `%`      | Modulus (Remainder)    | `10 % 3 = 1`     |
| `**`     | Exponentiation         | `2 ** 3 = 8`     |

### Examples
```python
# Basic operations
a = 10
b = 3
print(a + b)  # Addition: 13
print(a - b)  # Subtraction: 7
print(a * b)  # Multiplication: 30
print(a / b)  # Division: 3.3333...
print(a // b) # Floor Division: 3
print(a % b)  # Modulus: 1
print(a ** b) # Exponentiation: 1000
```

## Useful Built-in Functions

Python provides several built-in functions for numbers:

- **`abs(x)`**: Returns the absolute value of `x`.
  ```python
  print(abs(-5))  # Output: 5
  ```

- **`round(x, n)`**: Rounds `x` to `n` decimal places.
  ```python
  print(round(3.14159, 2))  # Output: 3.14
  ```

- **`pow(x, y)`**: Computes `x` raised to the power of `y`.
  ```python
  print(pow(2, 3))  # Output: 8
  ```

## The `math` Module

Python's `math` module provides additional functions for advanced mathematical operations.

### Example Usage:
```python
import math

# Square root
print(math.sqrt(16))  # Output: 4.0

# Trigonometric functions
print(math.sin(math.pi / 2))  # Output: 1.0

# Logarithm
print(math.log(10))  # Output: 2.302585092994046 (natural log)
```

To use the `math` module, it must first be imported with `import math`.

---

In the next lesson, we’ll explore how to work with strings in Python.
