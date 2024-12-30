---
layout: default
title: "Object-Oriented Programming: Dunder Methods"
order: 48
---

Dunder methods (short for "double underscore") are special methods in Python that begin and end with double underscores. They allow you to define custom behavior for standard operators and functions.

### Common Dunder Methods

- `__init__`: Initializes an object.
- `__str__`: Defines how the object is represented as a string.
- `__repr__`: Provides a detailed string representation of the object.
- `__add__`: Allows custom behavior for the `+` operator.

### Example: `__str__` and `__repr__`

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"{self.name}, {self.age} years old"

    def __repr__(self):
        return f"Person(name={self.name}, age={self.age})"

person = Person("Alice", 30)
print(str(person))
print(repr(person))
```

### Expected Output

```plaintext
Alice, 30 years old
Person(name=Alice, age=30)
```

Dunder methods allow you to customize an object's behavior in Python.

---

Let me know when you're ready for the next lessons!
