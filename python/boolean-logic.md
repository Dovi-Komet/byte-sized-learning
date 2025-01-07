---
layout: default
title: "Boolean Logic"
order: 12
---

Boolean logic is the foundation of decision-making in Python. It allows you to evaluate expressions as `True` or `False`.

## What Are Booleans?

Booleans are a data type in Python that represent one of two values: `True` or `False`. These values are used to express the truthfulness of a condition or statement.

### Examples of Booleans

```python
is_python_fun = True
is_tired = False

print(is_python_fun)  # True
print(is_tired)       # False
```

In Python:
- `True` and `False` are case-sensitive and must be written with an uppercase first letter.
- They are often the result of evaluating conditions or expressions.

## Boolean Operators

Boolean operators allow you to combine or modify boolean values to create more complex logical expressions.

1. **AND**: Returns `True` if both conditions are `True`.
2. **OR**: Returns `True` if at least one condition is `True`.
3. **NOT**: Inverts the boolean value.

### Example: Basic Boolean Operators

```python
a = True
b = False

print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```

## Comparison Operators

Comparison operators are used to compare two values and return a Boolean (`True` or `False`) based on the comparison.

### Common Comparison Operators

1. **Equal to (`==`)**: Returns `True` if both values are equal.
2. **Not equal to (`!=`)**: Returns `True` if the values are not equal.
3. **Greater than (`>`)**: Returns `True` if the left value is greater than the right value.
4. **Less than (`<`)**: Returns `True` if the left value is less than the right value.
5. **Greater than or equal to (`>=`)**: Returns `True` if the left value is greater than or equal to the right value.
6. **Less than or equal to (`<=`)**: Returns `True` if the left value is less than or equal to the right value.

### Example: Comparison Operators

```python
x = 10
y = 20

print(x == y)   # False
print(x != y)   # True
print(x > y)    # False
print(x < y)    # True
print(x >= 10)  # True
print(x <= 5)   # False
```

### Expected Output

```plaintext
False
True
False
True
True
False
```

## Combining Comparison and Boolean Operators

You can combine comparison operators and Boolean operators to create more complex conditions.

### Example: Combining Operators

```python
age = 25
income = 50000

# Check if age is between 18 and 30 and income is above 40000
is_eligible = (18 <= age <= 30) and (income > 40000)
print(is_eligible)  # True

# Check if age is below 18 or income is below 20000
needs_support = (age < 18) or (income < 20000)
print(needs_support)  # False
```

### Expected Output

```plaintext
True
False
```

## Summary

- Booleans (`True` and `False`) are a fundamental data type in Python.
- Boolean operators (`and`, `or`, `not`) combine or modify Boolean values.
- Comparison operators (`==`, `!=`, `>`, `<`, `>=`, `<=`) evaluate relationships between values and return Boolean results.
- You can combine comparison and Boolean operators to evaluate complex conditions.

Mastering Boolean logic and comparison operators will prepare you for creating dynamic and responsive code.
