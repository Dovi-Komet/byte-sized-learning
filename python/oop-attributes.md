---
layout: default
title: "OOP Attributes"
order: 41
---

Attributes in Object-Oriented Programming (OOP) are variables that store data related to an object. Python provides flexibility in defining and accessing attributes. These attributes are either associated with the class or specific to an instance of the class.

---

## Types of Attributes

### 1. Instance Attributes
- Specific to an object.
- Defined within the `__init__` method or other instance methods.
- Use `self` to refer to the object’s attributes.

```python
class Dog:
    def __init__(self, name, breed):
        self.name = name  # Instance attribute
        self.breed = breed  # Instance attribute

# Create an object
dog1 = Dog("Buddy", "Golden Retriever")
dog2 = Dog("Max", "Poodle")

# Access instance attributes
print(dog1.name)  # Output: Buddy
print(dog2.breed)  # Output: Poodle
```

---

### 2. Class Attributes
- Shared across all objects of the class.
- Defined directly within the class body.
- Accessed using the class name or any instance of the class.

```python
class Dog:
    species = "Canis lupus familiaris"  # Class attribute

    def __init__(self, name, breed):
        self.name = name  # Instance attribute
        self.breed = breed  # Instance attribute

# Access class attribute
print(Dog.species)  # Output: Canis lupus familiaris

# Objects can also access the class attribute
dog1 = Dog("Buddy", "Golden Retriever")
print(dog1.species)  # Output: Canis lupus familiaris
```

---

## Modifying Attributes

### Modifying Instance Attributes
Instance attributes can be modified by directly accessing them via the object.

```python
dog1 = Dog("Buddy", "Golden Retriever")
print(dog1.name)  # Output: Buddy

dog1.name = "Charlie"  # Modify attribute
print(dog1.name)  # Output: Charlie
```

---

### Modifying Class Attributes
Class attributes can be modified using the class name.

```python
Dog.species = "Canis lupus"
print(Dog.species)  # Output: Canis lupus
```

---

## Dynamic Attributes

Attributes can also be added dynamically to objects.

```python
dog1.color = "Golden"  # Adding a new attribute dynamically
print(dog1.color)  # Output: Golden
```

---

## Summary

- **Instance Attributes**: Unique to each object, defined using `self`.
- **Class Attributes**: Shared across all instances, defined in the class body.
- **Dynamic Attributes**: Can be added to objects at runtime.

Understanding attributes is crucial for designing flexible and reusable classes. In the next lesson, we’ll dive deeper into class attributes and their behavior.
