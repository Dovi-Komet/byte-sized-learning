---
layout: default
title: "OOP Basics"
order: 40
---

Object-Oriented Programming (OOP) is a programming paradigm based on the concept of objects, which can contain data (attributes) and code (methods). OOP helps organize code, makes it reusable, and mirrors real-world concepts.

---

## Key Concepts of OOP

### 1. Classes and Objects
- **Class**: A blueprint for creating objects. It defines attributes and methods.
- **Object**: An instance of a class.

### 2. Attributes and Methods
- **Attributes**: Variables that store data related to the object.
- **Methods**: Functions defined in a class that describe the behaviors of an object.

---

## Defining a Class

You can define a class in Python using the `class` keyword.

```python
# Define a class
class Dog:
    # Constructor method to initialize attributes
    def __init__(self, name, breed):
        self.name = name  # Instance attribute
        self.breed = breed  # Instance attribute

    # Method
    def bark(self):
        return f"{self.name} says Woof!"
```

---

## Creating an Object

To create an object, call the class as if it were a function.

```python
# Create an object of the Dog class
my_dog = Dog("Buddy", "Golden Retriever")

# Access attributes
print(my_dog.name)  # Output: Buddy

# Call a method
print(my_dog.bark())  # Output: Buddy says Woof!
```

---

## Explanation

1. The `__init__` Method:
   - Called when an object is created.
   - Used to initialize the object's attributes.
2. The `self` Parameter:
   - Refers to the instance of the class.
   - Allows access to the instance’s attributes and methods.

---

## Example: Car Class

```python
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def start(self):
        return f"The {self.year} {self.make} {self.model} is starting."

# Create an object
my_car = Car("Toyota", "Camry", 2022)
print(my_car.start())  # Output: The 2022 Toyota Camry is starting.
```

---

## Benefits of OOP

1. **Modularity**: Code is organized into classes.
2. **Reusability**: Classes can be reused in different programs.
3. **Scalability**: New functionality can be added with minimal changes.

---

In the next lesson, we will explore how to define and use attributes in classes.
