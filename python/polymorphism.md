---
layout: default
title: "Polymorphism"
order: 49
---

Polymorphism is a core concept in Object-Oriented Programming (OOP). It allows objects of different classes to be treated as objects of a common parent class, enabling a single interface to work with different types.

---

## What Is Polymorphism?

- **Definition**: Polymorphism means "many forms." It allows the same method or operation to behave differently based on the object that invokes it.
- **Key Benefit**: Write code that can work with objects of different types, making it more flexible and reusable.

---

## Example: Polymorphism with Methods

Different classes can implement the same method in their own way. When you call the method, the appropriate version is executed based on the object.

### Example: Overriding Methods for Polymorphism

```python
class Animal:
    def speak(self):
        return "I make a sound."

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"

# Function that uses polymorphism
def animal_sound(animal):
    print(animal.speak())

dog = Dog()
cat = Cat()

animal_sound(dog)  # Calls Dog's speak method
animal_sound(cat)  # Calls Cat's speak method
```

### Output:

```plaintext
Woof!
Meow!
```

---

## Polymorphism with Functions

Polymorphism is not limited to methods. It also applies to functions that can accept objects of different types and call their respective methods.

### Example: Using Polymorphism in a Function

```python
animals = [Dog(), Cat(), Animal()]

for animal in animals:
    print(animal.speak())
```

### Output:

```plaintext
Woof!
Meow!
I make a sound.
```

---

## Polymorphism with Abstract Classes (Preview)

Polymorphism often works with abstract classes and interfaces. Abstract classes define a common interface, and derived classes provide specific implementations. This will be covered in detail in the next lesson.

---

## Why Use Polymorphism?

1. **Code Reusability**:
   - Write generic functions or methods that work with multiple types of objects.

2. **Flexibility**:
   - Add new classes or types without modifying existing code.

3. **Scalability**:
   - Handle more complex hierarchies or systems with a single interface.

---

## Summary

- **Polymorphism**:
  - Enables objects of different classes to be treated as objects of a common parent class.
  - Allows methods with the same name to behave differently depending on the object.
- Polymorphism is key to writing flexible and reusable code, especially in systems with complex class hierarchies.

Practice implementing polymorphism to see how it simplifies and enhances your programs.
