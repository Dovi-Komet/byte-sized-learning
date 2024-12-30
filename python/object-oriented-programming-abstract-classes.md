---
layout: default
title: "Object-Oriented Programming: Abstract Classes"
order: 45
---

An abstract class is a class that cannot be instantiated directly. It is meant to be a blueprint for other classes. Abstract classes are defined using the `abc` module.

### Defining an Abstract Class

Use `@abstractmethod` to define methods that must be implemented in child classes.

Example:

```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

# animal = Animal()  # This will raise an error
dog = Dog()
print(dog.speak())
```

### Expected Output

```plaintext
Woof!
```

Abstract classes ensure that derived classes implement specific methods.