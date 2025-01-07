---
layout: default
title: "OOP Attributes"
order: 41
---

Attributes are variables associated with an object. They store the state of an object and can be used to hold information specific to that object.

---

## Types of Attributes

### 1. Instance Attributes
- Defined inside the `__init__` method.
- Specific to each object (instance) of the class.
- Accessed and modified using the `self` keyword.

### Example: Instance Attributes

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Instance attribute
        self.age = age    # Instance attribute

# Create objects with their own attributes
person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

print(person1.name, person1.age)  # Alice 30
print(person2.name, person2.age)  # Bob 25
```

---

## Modifying Instance Attributes

You can modify instance attributes directly by accessing them through the object.

### Example: Modifying Attributes

```python
person1.age = 31  # Update the age attribute of person1
print(person1.age)  # 31
```

### Output:

```plaintext
31
```

---

## Adding New Attributes Dynamically

You can add attributes to an object dynamically, but this practice should be used cautiously to maintain code clarity.

### Example: Adding Attributes Dynamically

```python
person1.height = 170  # Add a new attribute to person1
print(person1.height)  # 170
```

### Output:

```plaintext
170
```

Note: Dynamically added attributes are specific to the object and not shared across other instances.

---

## Class Attributes (Preview)

Unlike instance attributes, class attributes are shared across all objects of the class. We’ll explore class attributes in detail in the next lesson.

---

## Summary

- **Instance Attributes**:
  - Defined within the `__init__` method using `self`.
  - Specific to each object and can be accessed or modified individually.
- **Dynamic Attributes**:
  - Attributes can be added dynamically, but this practice should be limited to maintain clarity.

Attributes allow you to represent the unique state of each object. Practice defining, accessing, and modifying attributes to understand their role in OOP.
