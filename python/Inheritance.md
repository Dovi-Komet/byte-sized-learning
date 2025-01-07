---
layout: default
title: "Inheritance"
order: 43
---

Inheritance is a fundamental concept in Object-Oriented Programming (OOP) that allows one class (child class) to inherit the attributes and methods of another class (parent class). This promotes code reuse and helps create a hierarchy of classes.

---

## What Is Inheritance?

- **Parent Class (Base Class)**: The class being inherited from.
- **Child Class (Derived Class)**: The class that inherits from the parent class.

Inheritance enables the child class to:
1. Use the attributes and methods of the parent class.
2. Override or extend the functionality of the parent class.

---

## Defining a Child Class

To create a child class, use the syntax:

```python
class ChildClass(ParentClass):
    pass
```

---

## Example: Basic Inheritance

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return "I make a sound."

class Dog(Animal):  # Dog inherits from Animal
    def speak(self):  # Method override
        return f"{self.name} says Woof!"
```

---

## Creating an Object of the Child Class

You can create an object of the child class just like you would for the parent class.

### Example: Using the Child Class

```python
dog = Dog("Buddy")  # Create an instance of Dog
print(dog.speak())  # Call the speak method
```

### Output:

```plaintext
Buddy says Woof!
```

---

## Overriding Methods

The child class can provide its own implementation of a method defined in the parent class. This is called **method overriding**.

### Example: Overriding a Method

```python
class Cat(Animal):  # Cat inherits from Animal
    def speak(self):  # Override the speak method
        return f"{self.name} says Meow!"
```

```python
cat = Cat("Whiskers")
print(cat.speak())
```

### Output:

```plaintext
Whiskers says Meow!
```

---

## Extending Functionality

The child class can add new attributes and methods in addition to those inherited from the parent class.

### Example: Adding New Functionality

```python
class Bird(Animal):
    def fly(self):
        return f"{self.name} is flying!"
```

```python
bird = Bird("Tweety")
print(bird.speak())  # Inherited method
print(bird.fly())    # New method
```

### Output:

```plaintext
I make a sound.
Tweety is flying!
```

---

## Using `super()` to Call Parent Methods

The `super()` function is used to call a method from the parent class. This is useful when you want to retain some functionality from the parent class while extending or modifying it.

### Example: Using `super()`

```python
class Puppy(Dog):
    def __init__(self, name, age):
        super().__init__(name)  # Call the parent class's __init__ method
        self.age = age

    def speak(self):
        return f"{self.name}, who is {self.age} months old, says Woof!"
```

```python
puppy = Puppy("Charlie", 6)
print(puppy.speak())
```

### Output:

```plaintext
Charlie, who is 6 months old, says Woof!
```

---

## Summary

- **Inheritance** allows a child class to inherit attributes and methods from a parent class.
- **Method overriding** lets you redefine parent methods in the child class.
- **Extending functionality** enables child classes to add new methods and attributes.
- Use `super()` to call parent methods when needed.

Inheritance helps create reusable and extensible code. Practice creating parent and child classes to understand this concept deeply.
