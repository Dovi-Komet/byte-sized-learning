---
layout: default
title: "Understanding self"
order: 44
---

The `self` parameter in Python is a reference to the instance of the class. It allows instance methods to access and modify the attributes and methods of the object. While `self` is not a keyword, it is a widely adopted convention and must be explicitly specified as the first parameter in instance methods.

---

## Why Use `self`?

The `self` parameter ensures that the method operates on the correct instance of the class. Without `self`, methods cannot distinguish between attributes of different objects.

### Example: Using `self`

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Assign instance attribute
        self.age = age

    def greet(self):
        return f"Hi, my name is {self.name} and I am {self.age} years old."

# Create two instances
person1 = Person("Alice", 30)
person2 = Person("Bob", 25)

# Call greet method on each instance
print(person1.greet())  # Output: Hi, my name is Alice and I am 30 years old.
print(person2.greet())  # Output: Hi, my name is Bob and I am 25 years old.
```

- **Explanation**:
  - The `greet` method uses `self.name` and `self.age` to access attributes of the specific instance calling the method.

---

## `self` in Constructors

The `__init__` method uses `self` to initialize attributes specific to an instance.

### Example: Attribute Initialization

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model

    def details(self):
        return f"This car is a {self.make} {self.model}."

car = Car("Toyota", "Corolla")
print(car.details())  # Output: This car is a Toyota Corolla.
```

- **Explanation**:
  - `self.make` and `self.model` refer to attributes specific to the `car` instance.

---

## When to Use `self`

- To refer to instance attributes: `self.attribute_name`.
- To call other instance methods: `self.method_name()`.
- To distinguish between instance and local variables in methods.

### Example: Calling Methods with `self`

```python
class Calculator:
    def __init__(self, value):
        self.value = value

    def add(self, amount):
        return self.value + amount

    def multiply_and_add(self, multiplier, amount):
        result = self.add(amount) * multiplier  # Calls another method using self
        return result

calc = Calculator(10)
print(calc.multiply_and_add(2, 5))  # Output: 30
```

- **Explanation**:
  - The `multiply_and_add` method uses `self.add(amount)` to call the `add` method of the same instance.

---

## What Happens Without `self`?

If you omit `self`, Python raises a `TypeError` because the method doesn’t know which instance to operate on.

### Example: Missing `self`

```python
class Example:
    def greet():  # Missing self
        print("Hello!")

obj = Example()
obj.greet()  # Raises TypeError: greet() takes 0 positional arguments but 1 was given
```

---

## Summary

- `self` represents the current instance of the class.
- It is explicitly declared in instance methods and provides access to attributes and other methods of the instance.
- Using `self`, you can ensure that methods operate on the correct object, even when multiple objects exist.

In the next lesson, we’ll explore inheritance and how it allows classes to share functionality.
