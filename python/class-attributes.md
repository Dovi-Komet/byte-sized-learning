---
layout: default
title: "Class Attributes"
order: 40.5
---

Class attributes are variables that belong to a class rather than any specific object (instance) of the class. They are shared across all instances of the class and are useful for storing data that is the same for every object.

---

## What Are Class Attributes?

- Defined directly in the class body, outside any method.
- Shared by all instances of the class.
- Accessed using the class name or an instance.

---

## Defining a Class Attribute

You define class attributes directly within the class, outside of the `__init__` method.

### Example: Defining and Accessing Class Attributes

```python
class Dog:
    species = "Canis familiaris"  # Class attribute

    def __init__(self, name, age):
        self.name = name  # Instance attribute
        self.age = age    # Instance attribute

# Create two instances of Dog
dog1 = Dog("Buddy", 5)
dog2 = Dog("Max", 3)

# Access class attributes
print(dog1.species)  # Access through an instance
print(dog2.species)  # Access through another instance
print(Dog.species)   # Access directly through the class
```

### Output:

```plaintext
Canis familiaris
Canis familiaris
Canis familiaris
```

---

## Modifying Class Attributes

You can modify a class attribute using the class name. Changes to class attributes affect all instances.

### Example: Modifying Class Attributes

```python
Dog.species = "Canine"

print(dog1.species)  # Output: Canine
print(dog2.species)  # Output: Canine
```

### Output:

```plaintext
Canine
Canine
```

---

## Overriding Class Attributes

While class attributes are shared, you can override them for a specific instance by assigning a new value to the attribute on that instance.

### Example: Overriding Class Attributes

```python
dog1.species = "Wolf"

print(dog1.species)  # Output: Wolf (overridden for this instance)
print(dog2.species)  # Output: Canine (class attribute remains unchanged)
print(Dog.species)   # Output: Canine (class attribute remains unchanged)
```

### Output:

```plaintext
Wolf
Canine
Canine
```

---

## Summary

- **Class Attributes**:
  - Shared across all instances of a class.
  - Defined directly in the class body, outside methods.
  - Accessed through the class name or an instance.
- **Instance-Specific Override**:
  - An instance can override a class attribute by assigning a new value to it.

Class attributes are useful for storing information that is the same for all objects of a class, such as constants or shared properties. Practice defining, modifying, and overriding class attributes to deepen your understanding.
