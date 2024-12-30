---
layout: default
title: "Object-Oriented Programming: Dunder Methods for Operators"
order: 49
---

Dunder methods can be used to define custom behavior for operators like `+`, `-`, and `==`. These methods make objects more intuitive to use.

### Overloading the `+` Operator

You can use the `__add__` method to define how the `+` operator works for your objects.

Example:

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        return Point(self.x + other.x, self.y + other.y)

    def __str__(self):
        return f"Point({self.x}, {self.y})"

point1 = Point(1, 2)
point2 = Point(3, 4)
result = point1 + point2
print(result)
```

### Expected Output

```plaintext
Point(4, 6)
```

### Overloading the `==` Operator

You can use the `__eq__` method to define equality between objects.

Example:

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __eq__(self, other):
        return self.x == other.x and self.y == other.y

point1 = Point(1, 2)
point2 = Point(1, 2)
point3 = Point(3, 4)
print(point1 == point2)
print(point1 == point3)
```

### Expected Output

```plaintext
True
False
```

Operator overloading makes objects easier to work with in Python.