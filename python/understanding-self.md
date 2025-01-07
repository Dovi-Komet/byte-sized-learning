---
layout: default
title: "Understanding self"
order: 44
---

The `self` keyword is a fundamental concept in Object-Oriented Programming (OOP) in Python. It represents the instance of the class and is used to access the attributes and methods of that instance.

---

## What Is `self`?

- `self` is a reference to the current instance of the class.
- It must be explicitly included as the first parameter in all instance methods.
- It is used to:
  - Access attributes and methods of the instance.
  - Differentiate instance-specific data from shared class attributes.

---

## Using `self` to Access Attributes

When defining attributes in a class, `self` is used to specify that the attributes belong to the instance.

### Example: Accessing Attributes with `self`

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Attribute belongs to the instance
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name}."
```

### Explanation:
- `self.name` refers to the `name` attribute of the current instance.
- `self.age` refers to the `age` attribute of the current instance.

---

## Using `self` to Call Methods

You can use `self` to call other methods within the same class.

### Example: Calling Methods with `self`

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name}."

    def introduce(self):
        return self.greet() + f" I am {self.age} years old."
```

```python
person = Person("Alice", 30)
print(person.introduce())
```

### Output:

```plaintext
Hello, my name is Alice. I am 30 years old.
```

---

## Differentiating Between Class and Instance Attributes

`self` is used to access instance-specific attributes, whereas class attributes are accessed using the class name.

### Example: Class vs. Instance Attributes

```python
class Dog:
    species = "Canis familiaris"  # Class attribute

    def __init__(self, name):
        self.name = name  # Instance attribute
```

```python
dog1 = Dog("Buddy")
dog2 = Dog("Max")

print(dog1.name)      # Instance-specific attribute
print(Dog.species)    # Shared class attribute
```

### Output:

```plaintext
Buddy
Canis familiaris
```

---

## Why Is `self` Explicit?

In Python, `self` must be explicitly declared as the first parameter of instance methods. This explicitness improves code readability and avoids ambiguity about which attributes and methods belong to the instance.

---

## Common Mistakes with `self`

1. **Forgetting to Include `self`**:
   - If you forget to include `self` as a parameter, Python will raise a `TypeError`.

   ```python
   class Example:
       def greet():
           print("Hello!")

   obj = Example()
   obj.greet()  # TypeError: greet() takes 0 positional arguments but 1 was given
   ```

2. **Using `self` for Class Attributes**:
   - Class attributes should be accessed using the class name, not `self`.

---

## Summary

- `self` is a reference to the instance of the class and must be included as the first parameter in instance methods.
- It is used to:
  - Access instance attributes and methods.
  - Differentiate instance-specific data from class-level data.
- Always include `self` explicitly in method definitions and calls.

Understanding `self` is crucial for working with classes and objects in Python. Practice using it in different contexts to solidify your understanding.
