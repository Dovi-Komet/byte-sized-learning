---
layout: default
title: "Using super()"
order: 45
---

The `super()` function is used to call methods from the parent class. It is commonly used in inheritance to retain or extend the behavior of the parent class.

---

## What Is `super()`?

- `super()` gives you access to methods and attributes of the parent class.
- It is primarily used to call the parent class's constructor (`__init__`) or other methods.

---

## Using `super()` to Call the Parent Class's Constructor

The `super()` function is often used in the child class's constructor to initialize attributes inherited from the parent class.

### Example: Initializing Attributes with `super()`

```python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)  # Call the parent class's __init__
        self.breed = breed
```

---

## Creating an Object with `super()`

You can create an instance of the child class and access both inherited and child-specific attributes.

### Example:

```python
dog = Dog("Buddy", "Golden Retriever")
print(dog.name)   # Inherited from Animal
print(dog.breed)  # Specific to Dog
```

### Output:

```plaintext
Buddy
Golden Retriever
```

---

## Using `super()` to Call Other Methods

`super()` can also be used to call methods from the parent class in addition to the constructor.

### Example: Extending a Method with `super()`

```python
class Animal:
    def speak(self):
        return "I make a sound."

class Dog(Animal):
    def speak(self):
        parent_speech = super().speak()  # Call the parent method
        return f"{parent_speech} Woof!"
```

```python
dog = Dog()
print(dog.speak())
```

### Output:

```plaintext
I make a sound. Woof!
```

---

## Why Use `super()`?

1. **Avoid Repetition**:
   - Reuse parent class functionality without rewriting code.

2. **Maintain Parent Behavior**:
   - Extend or modify behavior while retaining the original functionality.

3. **Simplify Hierarchies**:
   - In complex inheritance hierarchies, `super()` ensures the correct method is called in a predictable order (important for multiple inheritance).

---

## Example: `super()` in Multiple Inheritance

In multiple inheritance, `super()` ensures methods are called in the correct order, defined by the **Method Resolution Order (MRO)**.

### Example: Multiple Inheritance with `super()`

```python
class A:
    def do_something(self):
        print("A's method")

class B(A):
    def do_something(self):
        super().do_something()
        print("B's method")

class C(B):
    def do_something(self):
        super().do_something()
        print("C's method")
```

```python
obj = C()
obj.do_something()
```

### Output:

```plaintext
A's method
B's method
C's method
```

---

## Summary

- **`super()`**:
  - Calls methods from the parent class.
  - Commonly used to initialize attributes in the child class.
  - Extends or modifies behavior without rewriting parent class logic.
- **Key Benefits**:
  - Avoids code repetition.
  - Simplifies complex inheritance hierarchies.
  - Ensures predictable method calls in multiple inheritance scenarios.

Practice using `super()` to create flexible and reusable class hierarchies while retaining the functionality of parent classes.
