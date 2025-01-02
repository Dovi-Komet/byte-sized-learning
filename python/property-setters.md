---
layout: default
title: "Property Setters"
order: 50
---

You can define setter methods to modify the value of an attribute.

### Using `@property` and `@<attribute>.setter`

Define a setter for an attribute using the `@<attribute>.setter` decorator.

Example:

```python
class Person:
    def __init__(self, name):
        self._name = name

    @property
    def name(self):
        return self._name

    @name.setter
    def name(self, new_name):
        self._name = new_name

person = Person("Alice")
print(person.name)
person.name = "Charlie"
print(person.name)
```

### Expected Output

```plaintext
Alice
Charlie
```

Property setters allow controlled modification of attributes.