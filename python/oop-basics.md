---
layout: default
title: "OOP Basics"
order: 39
---

Object-Oriented Programming (OOP) is a programming paradigm that organizes code using objects, which are instances of classes.

### What is a Class?

A class is a blueprint for creating objects. It defines the properties (attributes) and actions (methods) that the objects will have.

### Defining a Class

Use the `class` keyword to define a class.

Example:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name} and I am {self.age} years old."
```

### Creating an Object

You create an object (an instance of a class) by calling the class.

Example:

```python
person1 = Person("Alice", 30)
print(person1.greet())
```

### Expected Output

```plaintext
Hello, my name is Alice and I am 30 years old.
```

OOP makes it easier to structure and reuse your code by grouping related data and behavior.