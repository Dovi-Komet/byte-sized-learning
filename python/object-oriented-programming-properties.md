---
layout: default
title: "Object-Oriented Programming: Properties"
order: 46
---

Properties in Python allow you to control access to attributes using methods while still accessing them like attributes.

### Using `property()` to Create a Getter

You can use the `property()` function to create a getter for an attribute.

Example:

```python
class Person:
    def __init__(self, name):
        self._name = name

    def get_name(self):
        return self._name

    name = property(get_name)

person = Person("Alice")
print(person.name)
```

### Expected Output

```plaintext
Alice
```

### Using `@property` Decorator

The `@property` decorator simplifies creating properties.

Example:

```python
class Person:
    def __init__(self, name):
        self._name = name

    @property
    def name(self):
        return self._name

person = Person("Bob")
print(person.name)
```

### Expected Output

```plaintext
Bob
```