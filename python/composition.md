---
layout: default
title: "Composition"
order: 53
---

Composition is a design principle where one class is composed of objects of another class. It allows you to build complex objects by combining simpler ones.

### Example of Composition

A `Car` class might be composed of an `Engine` class.

Example:

```python
class Engine:
    def __init__(self, horsepower):
        self.horsepower = horsepower

    def start(self):
        return "Engine starts."

class Car:
    def __init__(self, make, model, engine):
        self.make = make
        self.model = model
        self.engine = engine

    def start(self):
        return f"{self.make} {self.model}: {self.engine.start()}"

engine = Engine(150)
car = Car("Toyota", "Corolla", engine)
print(car.start())
```

### Expected Output

```plaintext
Toyota Corolla: Engine starts.
```

Composition provides flexibility and reusability in your code.