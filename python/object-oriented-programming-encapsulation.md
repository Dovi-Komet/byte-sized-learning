---
layout: default
title: "Object-Oriented Programming: Encapsulation"
order: 43
---

Encapsulation is the practice of restricting access to certain parts of an object and exposing only what is necessary. It helps protect the internal state of an object.

### Public Attributes and Methods

By default, all attributes and methods in Python are public, meaning they can be accessed directly.

Example:

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Public attribute
        self.age = age    # Public attribute

person = Person("Alice", 30)
print(person.name)
print(person.age)
```

### Expected Output

```plaintext
Alice
30
```

### Private Attributes

Private attributes are defined with a double underscore (`__`) prefix. They cannot be accessed directly from outside the class.

Example:

```python
class Person:
    def __init__(self, name, age):
        self.__name = name  # Private attribute
        self.__age = age    # Private attribute

    def get_info(self):
        return f"{self.__name} is {self.__age} years old."

person = Person("Bob", 25)
print(person.get_info())
# print(person.__name)  # This will raise an AttributeError
```

### Expected Output

```plaintext
Bob is 25 years old.
```

Encapsulation allows better control over how attributes are accessed or modified.