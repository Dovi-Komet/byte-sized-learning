---
layout: default
title: "OOP Basics"
order: 40
---

Object-Oriented Programming (OOP) is a programming paradigm that organizes code using objects, which are instances of classes. OOP makes it easier to group related data and behavior, leading to more structured and reusable code.

---

## What Is a Class?

A **class** is a blueprint for creating objects. It defines:
- **Attributes**: Variables that store the object's data.
- **Methods**: Functions that define the object's behavior.

---

## Defining a Class

Use the `class` keyword to define a class. The `__init__` method (constructor) is used to initialize an object's attributes when the class is instantiated.

### Example: Defining a Class

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Attribute
        self.age = age    # Attribute

    def greet(self):  # Method
        return f"Hello, my name is {self.name} and I am {self.age} years old."
```

---

## Creating an Object

You create an object (an instance of a class) by calling the class with its required arguments.

### Example: Creating an Object

```python
person1 = Person("Alice", 30)  # Create an instance of the Person class
print(person1.greet())         # Call the greet method
```

### Output:

```plaintext
Hello, my name is Alice and I am 30 years old.
```

---

## Adding More Methods

You can add additional methods to perform actions specific to the class.

### Example: Adding Methods

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name}."

    def is_adult(self):
        return self.age >= 18
```

### Using the Methods

```python
person2 = Person("Bob", 17)
print(person2.greet())         # Output: Hello, my name is Bob.
print("Is adult:", person2.is_adult())  # Output: Is adult: False
```

---

## The `self` Keyword

The `self` keyword represents the instance of the class. It is used to access attributes and methods within the class.

### Example: Using `self`

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def update_name(self, new_name):
        self.name = new_name
```

---

## Summary

- A **class** is a blueprint for creating objects with attributes and methods.
- An **object** is an instance of a class, representing a specific entity.
- The `__init__` method initializes the object's attributes when it is created.
- The `self` keyword is used to refer to the current instance of the class.

OOP allows you to model real-world entities and their behaviors, making your code more organized and reusable. Practice creating classes and objects to deepen your understanding of this powerful paradigm.
