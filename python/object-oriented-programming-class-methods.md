---
layout: default
title: "Object-Oriented Programming: Class Methods"
order: 53
---

Class methods are methods that operate on the class itself rather than instances of the class. They are defined using the `@classmethod` decorator.

### Defining and Using a Class Method

Example:

```python
class Person:
    count = 0

    def __init__(self, name):
        self.name = name
        Person.count += 1

    @classmethod
    def total_people(cls):
        return cls.count

person1 = Person("Alice")
person2 = Person("Bob")
print(Person.total_people())
```

### Expected Output

```plaintext
2
```

Class methods are commonly used for factory methods or for maintaining class-level data.