---
layout: default
title: "Boolean Logic"
order: 12
---

Boolean logic forms the foundation of decision-making in Python programs. It allows you to compare values and evaluate conditions.

## Boolean Values

In Python, there are two boolean values: `True` and `False`. They are used to represent truth values.

### Example:
```python
is_sunny = True
is_raining = False
print(is_sunny)   # Output: True
print(is_raining) # Output: False
```

## Comparison Operators

Python provides comparison operators to compare values. These operators return a boolean result (`True` or `False`).

| Operator | Description                  | Example             | Result  |
|----------|------------------------------|---------------------|---------|
| `==`     | Equal to                    | `5 == 5`           | `True`  |
| `!=`     | Not equal to                | `5 != 3`           | `True`  |
| `>`      | Greater than                | `7 > 3`            | `True`  |
| `<`      | Less than                   | `3 < 7`            | `True`  |
| `>=`     | Greater than or equal to    | `7 >= 7`           | `True`  |
| `<=`     | Less than or equal to       | `3 <= 5`           | `True`  |

### Example:
```python
x = 10
y = 5
print(x > y)  # Output: True
print(x == y) # Output: False
```

## Logical Operators

Logical operators are used to combine boolean expressions.

| Operator | Description                      | Example                     | Result  |
|----------|----------------------------------|-----------------------------|---------|
| `and`    | Returns `True` if both are `True` | `True and False`           | `False` |
| `or`     | Returns `True` if at least one is `True` | `True or False`    | `True`  |
| `not`    | Negates a boolean value          | `not True`                 | `False` |

### Example:
```python
x = 10
y = 5
z = 3

print(x > y and y > z) # Output: True
print(x < y or z < y)  # Output: True
print(not (x > y))     # Output: False
```

## Truthy and Falsy Values

In Python, some values are considered "truthy" (treated as `True`) or "falsy" (treated as `False`) in a boolean context.

- **Truthy**: Non-zero numbers, non-empty strings, non-empty lists, etc.
- **Falsy**: `0`, `None`, empty strings (`""`), empty lists (`[]`), etc.

### Example:
```python
if "Hello":  # Non-empty string is truthy
    print("This is truthy!")

if 0:  # Zero is falsy
    print("This won’t print.")
else:
    print("This is falsy!")
```

---

In the next lesson, we’ll learn how to use boolean logic to create conditional statements.
