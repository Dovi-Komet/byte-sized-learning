---
layout: default
title: "Class Attributes"
order: 42
---

Class attributes in Python are variables defined within the class body but outside any methods. These attributes are shared by all instances of the class, making them useful for data or functionality common to all objects.

---

## Defining Class Attributes

Class attributes are defined directly in the class body and are accessible through the class name or any instance.

```python
class Dog:
    # Class attribute
    species = "Canis lupus familiaris"

    def __init__(self, name, breed):
        # Instance attributes
        self.name = name
        self.breed = breed

# Accessing class attributes
print(Dog.species)  # Output: Canis lupus familiaris

# Creating objects
dog1 = Dog("Buddy", "Golden Retriever")
dog2 = Dog("Max", "Poodle")

# Class attributes are shared
print(dog1.species)  # Output: Canis lupus familiaris
print(dog2.species)  # Output: Canis lupus familiaris
```

---

## Modifying Class Attributes

Class attributes can be modified using the class name. Any change to a class attribute affects all instances.

```python
Dog.species = "Canis lupus"

# The updated value is reflected in all instances
print(dog1.species)  # Output: Canis lupus
print(dog2.species)  # Output: Canis lupus
```

---

## Difference Between Class and Instance Attributes

Class attributes are shared across all instances, while instance attributes are unique to each object.

```python
class Dog:
    species = "Canis lupus familiaris"  # Class attribute

    def __init__(self, name, breed):
        self.name = name  # Instance attribute
        self.breed = breed  # Instance attribute

# Create two objects
dog1 = Dog("Buddy", "Golden Retriever")
dog2 = Dog("Max", "Poodle")

# Modify instance attribute
dog1.name = "Charlie"

# Instance attributes are independent
print(dog1.name)  # Output: Charlie
print(dog2.name)  # Output: Max

# Class attributes remain shared
print(dog1.species)  # Output: Canis lupus familiaris
print(dog2.species)  # Output: Canis lupus familiaris
```

---

## Practical Use of Class Attributes

Class attributes are ideal for constants or values common to all instances.

```python
class Circle:
    # Class attribute: shared across all instances
    pi = 3.14159

    def __init__(self, radius):
        self.radius = radius  # Instance attribute

    def area(self):
        return Circle.pi * (self.radius ** 2)

# Create a circle object
circle = Circle(5)
print(circle.area())  # Output: 78.53975
```

---

## Summary

- **Class attributes** are shared across all instances and are used for data or behavior common to all objects.
- They are defined in the class body and accessed through the class name or an instance.
- Changes to a class attribute affect all instances of the class.

In the next lesson, we’ll explore how methods work within classes and how they interact with attributes.
