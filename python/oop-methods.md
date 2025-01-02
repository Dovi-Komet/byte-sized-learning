---
layout: default
title: "OOP Methods"
order: 41
---

Methods are functions defined inside a class that operate on objects.

### Defining a Method

Use the `def` keyword inside the class to define a method.

Example:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name}."
```

### Using a Method

Call the method on an object using the dot (`.`) operator.

Example:

```python
person = Person("Alice", 30)
print(person.greet())
```

### Expected Output

```plaintext
Hello, my name is Alice.
```

Methods allow you to define actions that objects can perform.