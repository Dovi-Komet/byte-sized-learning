---
layout: default
title: "OOP Methods"
order: 43
---

Methods in Object-Oriented Programming (OOP) are functions defined within a class that operate on its attributes. They allow objects to interact with their data and implement behavior.

---

## Types of Methods

### 1. Instance Methods
Instance methods operate on instance attributes and require `self` as the first parameter.

```python
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

    def bark(self):
        return f"{self.name} says Woof!"

# Create an object
dog = Dog("Buddy", "Golden Retriever")

# Call an instance method
print(dog.bark())  # Output: Buddy says Woof!
```

- **Explanation**:
  - The `bark` method uses `self` to access the instance attribute `name`.
  - Each object has its own `name`, so the output is specific to the instance.

---

### 2. Class Methods
Class methods operate on class attributes and require `@classmethod` decorator. They take `cls` as the first parameter.

```python
class Dog:
    species = "Canis lupus familiaris"

    @classmethod
    def common_species(cls):
        return f"All dogs belong to {cls.species}."

# Call a class method
print(Dog.common_species())  # Output: All dogs belong to Canis lupus familiaris.
```

- **Explanation**:
  - Class methods can modify or access class attributes using `cls`.

---

### 3. Static Methods
Static methods do not operate on instance or class attributes. They are utility functions within the class, marked by `@staticmethod`.

```python
class Dog:
    @staticmethod
    def is_puppy(age):
        return age < 1

# Call a static method
print(Dog.is_puppy(0.5))  # Output: True
print(Dog.is_puppy(2))    # Output: False
```

- **Explanation**:
  - Static methods do not take `self` or `cls` as a parameter.
  - They are called directly on the class and are independent of any instance.

---

## Defining and Using Methods

### Example: Combining Instance and Class Methods

```python
class Circle:
    pi = 3.14159  # Class attribute

    def __init__(self, radius):
        self.radius = radius  # Instance attribute

    def area(self):
        return Circle.pi * (self.radius ** 2)  # Instance method

    @classmethod
    def from_diameter(cls, diameter):
        return cls(diameter / 2)  # Class method

# Create a Circle using the instance method
circle = Circle(5)
print(circle.area())  # Output: 78.53975

# Create a Circle using the class method
circle_from_diameter = Circle.from_diameter(10)
print(circle_from_diameter.area())  # Output: 78.53975
```

---

## Summary

- **Instance Methods**: Operate on instance attributes, take `self` as the first parameter.
- **Class Methods**: Operate on class attributes, take `cls` as the first parameter, and are defined using `@classmethod`.
- **Static Methods**: Do not depend on instance or class attributes, use `@staticmethod`.

In the next lesson, we’ll delve into the role of the `self` parameter in instance methods and how it works behind the scenes.
