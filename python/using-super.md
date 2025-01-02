---
layout: default
title: "Using super()`"
order: 45
---

The `super()` function is used to call a method from the parent class. It is especially useful in inheritance.

### Using `super()` to Call the Parent's Method

Example:

```python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)  # Call the parent class's __init__
        self.breed = breed
```

### Creating an Object with `super()`

Example:

```python
dog = Dog("Buddy", "Golden Retriever")
print(dog.name)
print(dog.breed)
```

### Expected Output

```plaintext
Buddy
Golden Retriever
```

The `super()` function allows you to extend the parent class's behavior while keeping its functionality intact.