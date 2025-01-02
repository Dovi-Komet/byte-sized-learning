---
layout: default
title: "Boolean Logic"
order: 9
---

Boolean logic is the foundation of decision-making in Python. It allows you to evaluate expressions as `True` or `False`.

### Boolean Operators

- **AND**: Returns `True` if both conditions are `True`.
- **OR**: Returns `True` if at least one condition is `True`.
- **NOT**: Inverts the boolean value.

Example:

```python
a = True
b = False

print(a and b)  # False
print(a or b)   # True
print(not a)    # False
```

### Combining Boolean Operators

Example:

```python
age = 20
has_permission = True

if age >= 18 and has_permission:
    print("Access granted")
else:
    print("Access denied")
```

### Expected Output

```plaintext
Access granted
```

Boolean logic is essential for building conditional statements and complex decision-making.
