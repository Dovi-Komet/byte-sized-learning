---
title: "Boolean Logic"
order: 11
---

# Boolean Logic

**Boolean logic** is the foundation of decision-making in Python. It involves expressions that evaluate to either `True` or `False`, and it's commonly used in conditional statements and loops.

---

## Boolean Values

Python has two Boolean values: `True` and `False`.

### Examples:
```python
print(True)   # True
print(False)  # False
print(type(True))  # <class 'bool'>
```

---

## Comparison Operators

Comparison operators are used to compare values, returning `True` or `False`.

| Operator | Description                  | Example       | Result  |
|----------|------------------------------|---------------|---------|
| `==`     | Equal to                     | `5 == 5`      | `True`  |
| `!=`     | Not equal to                 | `5 != 3`      | `True`  |
| `<`      | Less than                    | `3 < 5`       | `True`  |
| `<=`     | Less than or equal to        | `5 <= 5`      | `True`  |
| `>`      | Greater than                 | `7 > 3`       | `True`  |
| `>=`     | Greater than or equal to     | `7 >= 8`      | `False` |

### Examples:
```python
x = 10
y = 20

print(x == y)  # False
print(x < y)   # True
print(x >= 10) # True
```

---

## Logical Operators

Logical operators combine multiple conditions.

| Operator | Description              | Example                  | Result |
|----------|--------------------------|--------------------------|--------|
| `and`    | Returns `True` if both conditions are `True` | `(5 > 3) and (10 > 7)` | `True` |
| `or`     | Returns `True` if at least one condition is `True` | `(5 > 3) or (10 < 7)` | `True` |
| `not`    | Reverses the Boolean value | `not (5 > 3)`           | `False`|

### Examples:
```python
# and operator
print((5 > 3) and (10 > 7))  # True
print((5 > 3) and (10 < 7))  # False

# or operator
print((5 > 3) or (10 < 7))   # True
print((5 < 3) or (10 < 7))   # False

# not operator
print(not (5 > 3))           # False
```

---

## Truthy and Falsy Values

In Python, some values are considered **truthy** or **falsy** when evaluated in a Boolean context:

- **Falsy Values**: `None`, `False`, `0`, `0.0`, `""` (empty string), `[]` (empty list), `{}` (empty dictionary).
- **Truthy Values**: Most other values.

### Examples:
```python
print(bool(0))        # False
print(bool(""))       # False
print(bool(123))      # True
print(bool("Python")) # True
```

---

## Short-Circuit Evaluation

Logical operators use **short-circuit evaluation**, meaning Python stops evaluating as soon as the result is determined.

### Examples:
```python
x = 10

# Short-circuit with 'or'
print((x > 5) or (x / 0))  # True (no error because the first condition is True)

# Short-circuit with 'and'
print((x > 15) and (x / 0))  # False (no error because the first condition is False)
```

---

## Common Use Cases

1. **Validating Input**:
   ```python
   age = int(input("Enter your age: "))
   if age > 0 and age < 120:
       print("Valid age")
   else:
       print("Invalid age")
   ```

2. **Combining Conditions**:
   ```python
   score = 85
   if score >= 90 or (score >= 80 and score < 90):
       print("You passed!")
   ```

3. **Negation**:
   ```python
   is_logged_in = False
   if not is_logged_in:
       print("Please log in.")
   ```

---

## Practice Exercises

1. Write a program that:
   - Asks the user for a number.
   - Prints whether the number is positive, negative, or zero.

2. Create a program to:
   - Check if a string entered by the user is empty or not.

3. Write a program that:
   - Asks for two numbers.
   - Prints `True` if both numbers are greater than 10; otherwise, prints `False`.

Boolean logic is at the heart of decision-making in Python and is essential for creating dynamic and interactive programs!
