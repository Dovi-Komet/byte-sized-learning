---
layout: default
title: "Polymorphism"
order: 47
---

Polymorphism allows objects of different classes to be treated as objects of a common parent class. It enables a single interface to work with different types.

### Example of Polymorphism

Different classes can implement the same method in their own way.

Example:

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

def animal_sound(animal):
    print(animal.speak())

dog = Dog()
cat = Cat()

animal_sound(dog)
animal_sound(cat)
```

### Expected Output

```plaintext
Woof!
Meow!
```

Polymorphism allows you to write more flexible and reusable code.