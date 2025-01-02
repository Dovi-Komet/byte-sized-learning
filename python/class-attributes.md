---
layout: default
title: "Class Attributes"
order: 42
---

Class attributes are shared across all instances of a class. They are defined directly in the class, outside any method.

### Defining a Class Attribute

Example:

```python
class Dog:
    species = "Canis familiaris"  # Class attribute

    def __init__(self, name, age):
        self.name = name
        self.age = age

dog1 = Dog("Buddy", 5)
dog2 = Dog("Max", 3)

print(dog1.species)
print(dog2.species)
```

### Expected Output

```plaintext
Canis familiaris
Canis familiaris
```

### Modifying Class Attributes

You can modify a class attribute, and the change will affect all instances.

Example:

```python
Dog.species = "Canine"
print(dog1.species)
print(dog2.species)
```

### Expected Output

```plaintext
Canine
Canine
```

Class attributes are useful for data shared among all objects of a class.