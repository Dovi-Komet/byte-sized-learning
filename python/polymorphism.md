---
layout: default
title: "Polymorphism"
order: 47
---

Polymorphism is a key concept in object-oriented programming (OOP) that allows objects of different classes to be treated as objects of a common superclass. It enables a single interface to represent different types of objects, making code more flexible and reusable.

---

## Polymorphism with Methods

In Python, polymorphism is typically achieved by defining methods with the same name in different classes. These methods can perform different operations depending on the class of the object.

### Example: Polymorphism with Methods

```python
class Dog:
    def speak(self):
        return "Woof!"

class Cat:
    def speak(self):
        return "Meow!"

def animal_speak(animal):
    print(animal.speak())

# Using the animal_speak function
dog = Dog()
cat = Cat()

animal_speak(dog)  # Output: Woof!
animal_speak(cat)  # Output: Meow!
```

---

## Polymorphism with Inheritance

Polymorphism is often used with inheritance. A subclass can override methods of the superclass, and the overridden method is called depending on the object type.

### Example: Polymorphism with Inheritance

```python
class Shape:
    def area(self):
        raise NotImplementedError("Subclasses must implement this method")

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

# Using polymorphism with shapes
shapes = [Rectangle(4, 5), Circle(3)]

for shape in shapes:
    print(shape.area())
# Output:
# 20
# 28.26
```

---

## Polymorphism with Built-in Functions

Python’s built-in functions like `len`, `sorted`, and `max` demonstrate polymorphism by working with different types of objects.

### Example: Polymorphism with `len`

```python
print(len("Hello"))  # Output: 5
print(len([1, 2, 3, 4]))  # Output: 4
print(len({"a": 1, "b": 2}))  # Output: 2
```

---

## Advantages of Polymorphism

1. **Flexibility**: Allows functions to use objects of different types.
2. **Reusability**: Encourages the use of generalized code.
3. **Scalability**: Makes it easy to add new classes with the same interface.

---

## Key Takeaways

- Polymorphism allows objects of different classes to be used interchangeably if they implement the same method interface.
- It enhances code readability, scalability, and reusability.
- Polymorphism is commonly used with methods, inheritance, and built-in functions.

---

In the next lesson, we’ll explore lambda functions and how they enable concise and functional programming in Python.
