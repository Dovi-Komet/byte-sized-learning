---
layout: default
title: "Method Overriding"
order: 44
---

Method overriding allows a child class to provide a specific implementation of a method that is already defined in its parent class. This enables customization of inherited behavior.

---

## What Is Method Overriding?

- A child class can override a method from the parent class by defining a method with the same name.
- The overridden method in the child class replaces the parent class's method for that object.

---

## Example: Overriding a Method

```python
class Animal:
    def speak(self):
        return "I make a sound."

class Cat(Animal):  # Cat inherits from Animal
    def speak(self):  # Override the speak method
        return "Meow!"
```

---

## Using the Overridden Method

When you call the overridden method on an instance of the child class, the child's implementation is used.

### Example:

```python
cat = Cat()  # Create an instance of Cat
print(cat.speak())  # Call the overridden speak method
```

### Output:

```plaintext
Meow!
```

---

## Retaining Parent Behavior with `super()`

If you want to retain some behavior from the parent class while extending it, use the `super()` function to call the parent class's method.

### Example: Extending the Parent Method

```python
class Dog(Animal):
    def speak(self):
        parent_speech = super().speak()  # Call the parent method
        return f"{parent_speech} Woof!"
```

```python
dog = Dog()
print(dog.speak())
```

### Output:

```plaintext
I make a sound. Woof!
```

---

## Practical Use of Method Overriding

Method overriding is useful when creating specialized behavior for child classes while maintaining a consistent interface.

### Example: Different Animal Sounds

```python
class Bird(Animal):
    def speak(self):
        return "Tweet!"

class Cow(Animal):
    def speak(self):
        return "Moo!"
```

```python
animals = [Cat(), Dog(), Bird(), Cow()]

for animal in animals:
    print(animal.speak())
```

### Output:

```plaintext
Meow!
I make a sound. Woof!
Tweet!
Moo!
```

---

## Summary

- **Method Overriding**:
  - Allows a child class to redefine a method from the parent class.
  - Provides specific behavior for objects of the child class.
- Use `super()` to call the parent method if you want to retain or extend its functionality.

Method overriding is a cornerstone of polymorphism, allowing you to customize behavior in a hierarchy of classes. Practice overriding methods to understand how it enables flexible and reusable code.
