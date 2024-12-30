---
layout: default
title: "Object-Oriented Programming: Attributes"
order: 37
---

Attributes are variables associated with an object. They store the state of an object.

### Instance Attributes

Instance attributes are defined within a class and are specific to each object.

Example:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

print(person1.name, person1.age)
print(person2.name, person2.age)
```

### Expected Output

```plaintext
Alice 30
Bob 25
```

Each object has its own set of attributes.

### Modifying Attributes

You can modify attributes directly.

Example:

```python
person1.age = 31
print(person1.age)
```

### Expected Output

```plaintext
31
```