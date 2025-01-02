---
layout: default
title: "Static Methods"
order: 55
---

Static methods are methods that belong to a class but do not access or modify the class or instance attributes. They are defined using the `@staticmethod` decorator.

### Defining and Using a Static Method

Example:

```python
class Math:
    @staticmethod
    def add(a, b):
        return a + b

print(Math.add(3, 5))
```

### Expected Output

```plaintext
8
```

Static methods are used for utility functions that don't depend on the state of the object.