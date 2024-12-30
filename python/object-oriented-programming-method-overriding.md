---
layout: default
title: "Object-Oriented Programming: Method Overriding"
order: 41
---

Method overriding allows a child class to provide a specific implementation of a method from its parent class.

### Overriding a Method

Define a method in the child class with the same name as the parent class method.

Example:

```python
class Animal:
    def speak(self):
        return "I make a sound."

class Cat(Animal):
    def speak(self):
        return "Meow!"
```

### Using the Overridden Method

Example:

```python
cat = Cat()
print(cat.speak())
```

### Expected Output

```plaintext
Meow!
```

Overriding enables customization of inherited behavior.