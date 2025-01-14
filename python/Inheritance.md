---
layout: default
title: "Inheritance"
order: 45
---

Inheritance is a fundamental concept in object-oriented programming (OOP) that allows one class (the child class) to inherit attributes and methods from another class (the parent class). This promotes code reuse and establishes a relationship between the classes.

---

## Defining a Parent Class

A parent class is the base class that contains common attributes and methods. Child classes inherit from the parent class.

### Example: Creating a Parent Class

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return f"{self.name} makes a sound."
```

---

## Creating a Child Class

To create a child class, specify the parent class in parentheses during the definition.

### Example: Inheriting from a Parent Class

```python
class Dog(Animal):
    def speak(self):
        return f"{self.name} barks."

# Create instances of the parent and child classes
generic_animal = Animal("Animal")
dog = Dog("Buddy")

print(generic_animal.speak())  # Output: Animal makes a sound.
print(dog.speak())            # Output: Buddy barks.
```

- **Explanation**:
  - The `Dog` class inherits from the `Animal` class.
  - The `speak` method is overridden in the `Dog` class.

---

## Overriding Methods

Child classes can modify or extend methods from the parent class. This is known as method overriding.

### Example: Overriding a Method

```python
class Cat(Animal):
    def speak(self):
        return f"{self.name} meows."

cat = Cat("Whiskers")
print(cat.speak())  # Output: Whiskers meows.
```

- **Explanation**:
  - The `Cat` class overrides the `speak` method to provide its own implementation.

---

## Using `super()`

The `super()` function allows child classes to access methods and attributes of the parent class.

### Example: Using `super()`

```python
class Bird(Animal):
    def speak(self):
        parent_speech = super().speak()
        return f"{parent_speech} Chirp chirp!"

bird = Bird("Tweety")
print(bird.speak())  # Output: Tweety makes a sound. Chirp chirp!
```

- **Explanation**:
  - The `Bird` class calls the `speak` method of the `Animal` class using `super()`.

---

## Multiple Inheritance

Python supports multiple inheritance, where a class can inherit from multiple parent classes.

### Example: Multiple Inheritance

```python
class Walker:
    def walk(self):
        return "This animal can walk."

class Flyer:
    def fly(self):
        return "This animal can fly."

class Bird(Walker, Flyer):
    pass

bird = Bird()
print(bird.walk())  # Output: This animal can walk.
print(bird.fly())   # Output: This animal can fly.
```

- **Explanation**:
  - The `Bird` class inherits methods from both `Walker` and `Flyer`.

---

## Why Use Inheritance?

1. **Code Reuse**: Avoid duplicating code in multiple classes.
2. **Logical Hierarchy**: Establish relationships between classes, such as "is-a" relationships.
3. **Extensibility**: Easily add or modify functionality in child classes.

---

In the next lesson, we’ll explore encapsulation and how it helps protect data in classes.
