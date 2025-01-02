---
layout: default
title: "Inheritance"
order: 43
---

Inheritance allows one class (child class) to inherit the attributes and methods of another class (parent class). This promotes code reuse.

### Defining a Child Class

Use the syntax `class ChildClass(ParentClass):`.

Example:

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return "I make a sound."

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"
```

### Creating an Object of the Child Class

Example:

```python
dog = Dog("Buddy")
print(dog.speak())
```

### Expected Output

```plaintext
Buddy says Woof!
```

Inheritance allows you to override methods and extend the functionality of the parent class.