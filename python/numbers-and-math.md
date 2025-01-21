---
title: "Numbers and Math"
order: 6
---

# Numbers and Math

Python is excellent for working with numbers. It provides robust support for numerical operations, from basic arithmetic to more advanced math.

## Number Types in Python

1. **Integers (`int`)**: Whole numbers (positive or negative).
   ```python
   x = 10  # Integer
   y = -5  # Negative integer
   ```
2. **Floating-Point Numbers (`float`)**: Numbers with a decimal point.
   ```python
   pi = 3.14159  # Float
   result = -0.5  # Negative float
   ```
3. **Complex Numbers (`complex`)**: Numbers with a real and imaginary part.
   ```python
   z = 2 + 3j  # Complex number
   ```

## Basic Arithmetic Operations

Python supports standard arithmetic operators:

| Operator | Description          | Example       | Result  |
|----------|----------------------|---------------|---------|
| `+`      | Addition             | `5 + 3`       | `8`     |
| `-`      | Subtraction          | `10 - 4`      | `6`     |
| `*`      | Multiplication       | `2 * 3`       | `6`     |
| `/`      | Division (float)     | `7 / 2`       | `3.5`   |
| `//`     | Floor Division       | `7 // 2`      | `3`     |
| `%`      | Modulus (remainder)  | `7 % 2`       | `1`     |
| `**`     | Exponentiation       | `2 ** 3`      | `8`     |

### Examples:
```python
a = 15
b = 4

print(a + b)  # 19
print(a - b)  # 11
print(a * b)  # 60
print(a / b)  # 3.75
print(a // b) # 3
print(a % b)  # 3
print(a ** b) # 50625
```

## Built-in Math Functions

Python provides several built-in functions for working with numbers:

| Function     | Description                        | Example          | Result  |
|--------------|------------------------------------|------------------|---------|
| `abs(x)`     | Absolute value                    | `abs(-5)`        | `5`     |
| `round(x, n)`| Round to `n` decimal places       | `round(3.14159, 2)` | `3.14` |
| `max(x, y)`  | Maximum value                     | `max(3, 7)`      | `7`     |
| `min(x, y)`  | Minimum value                     | `min(3, 7)`      | `3`     |
| `pow(x, y)`  | Raise `x` to the power of `y`     | `pow(2, 3)`      | `8`     |

## The `math` Module

For advanced mathematical operations, Python includes the `math` module.

### Using the `math` Module:
```python
import math

print(math.sqrt(16))  # 4.0
print(math.pi)        # 3.141592653589793
print(math.sin(math.radians(90)))  # 1.0
```

### Common `math` Functions:

| Function       | Description                          | Example                  |
|----------------|--------------------------------------|--------------------------|
| `math.sqrt(x)` | Square root of `x`                  | `math.sqrt(9)` → `3.0`   |
| `math.pi`      | Value of π                          | `math.pi` → `3.14159...` |
| `math.sin(x)`  | Sine of `x` (in radians)            | `math.sin(math.pi/2)` → `1.0` |
| `math.cos(x)`  | Cosine of `x` (in radians)          | `math.cos(0)` → `1.0`    |
| `math.log(x)`  | Natural logarithm of `x`            | `math.log(10)` → `2.302...` |

## Practice Exercises

1. Write a Python script to:
   - Add, subtract, multiply, and divide two numbers.
   - Use floor division and modulus to find the quotient and remainder.
2. Use the `math` module to calculate:
   - The square root of 64.
   - The sine of 45 degrees.
3. Round the number `7.56789` to 2 decimal places.

With these tools, you can confidently handle numerical operations in Python!