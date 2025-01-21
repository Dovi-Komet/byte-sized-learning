---
title: "Inheritance and Polymorphism"
order: 23
---

# Inheritance and Polymorphism

Inheritance and polymorphism are core concepts of Object-Oriented Programming (OOP) that promote code reuse and flexibility.

---

## Inheritance

**Inheritance** allows a class (child) to inherit attributes and methods from another class (parent). The child class can also have additional attributes and methods or override existing ones.

### Syntax:
```python
class Parent:
    # Parent class
    pass

class Child(Parent):
    # Child class inherits Parent
    pass
```

### Example:
```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        return "I make a sound."

class Dog(Animal):
    def speak(self):
        return "Woof!"

dog = Dog("Buddy")
print(dog.name)   # Output: Buddy
print(dog.speak())  # Output: Woof!
```

---

## The `super()` Function

The `super()` function allows the child class to call methods from the parent class.

### Example:
```python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)  # Call the parent class's __init__
        self.breed = breed

dog = Dog("Buddy", "Labrador")
print(dog.name)   # Output: Buddy
print(dog.breed)  # Output: Labrador
```

---

## Method Overriding

A child class can override methods from the parent class to provide specialized behavior.

### Example:
```python
class Bird:
    def fly(self):
        return "I can fly!"

class Penguin(Bird):
    def fly(self):
        return "I cannot fly."

penguin = Penguin()
print(penguin.fly())  # Output: I cannot fly.
```

---

## Polymorphism

**Polymorphism** allows objects of different classes to be treated as objects of a common parent class. This enables the same interface to handle different types of objects.

### Example:
```python
class Cat(Animal):
    def speak(self):
        return "Meow!"

animals = [Dog("Buddy"), Cat("Kitty")]

for animal in animals:
    print(f"{animal.name}: {animal.speak()}")

# Output:
# Buddy: Woof!
# Kitty: Meow!
```

---

## Abstract Classes and Methods

Abstract classes serve as blueprints for other classes. They can define methods that must be implemented by child classes.

- Use the `abc` module to create abstract classes.

### Example:
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

    @abstractmethod
    def perimeter(self):
        pass

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

    def perimeter(self):
        return 2 * (self.width + self.height)

rect = Rectangle(4, 5)
print(rect.area())      # Output: 20
print(rect.perimeter()) # Output: 18
```

---

## Multiple Inheritance

A class can inherit from more than one parent class.

### Example:
```python
class A:
    def method_a(self):
        return "Method from A"

class B:
    def method_b(self):
        return "Method from B"

class C(A, B):
    pass

c = C()
print(c.method_a())  # Output: Method from A
print(c.method_b())  # Output: Method from B
```

---

## Best Practices

1. Use inheritance to model "is-a" relationships (e.g., a Dog is an Animal).
2. Avoid deep inheritance hierarchies; they can make code harder to understand.
3. Use `super()` to access parent class methods and ensure proper initialization.
4. Prefer composition over inheritance when a class "has-a" relationship (e.g., a Car has an Engine).

---

## Practice Exercises

1. **Basic Inheritance**:
   - Create a parent class `Vehicle` with attributes `brand` and `model`.
   - Create a child class `Car` with an additional attribute `seats`.

2. **Method Overriding**:
   - Define a parent class `Shape` with a method `area`.
   - Create child classes `Circle` and `Square` that override `area`.

3. **Polymorphism**:
   - Create a parent class `Instrument` with a method `play`.
   - Create child classes `Guitar` and `Piano` that implement `play`.

4. **Abstract Classes**:
   - Define an abstract class `Animal` with an abstract method `sound`.
   - Implement `sound` in child classes `Dog` and `Cat`.

Inheritance and polymorphism help create flexible, reusable, and organized code structures for complex applications.