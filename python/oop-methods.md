---
layout: default
title: "OOP Methods"
order: 41
---

Methods are functions defined inside a class that operate on objects. They allow objects to perform actions and interact with their attributes.

---

## What Are Methods?

- **Methods** are defined within a class and typically operate on the attributes of the object they belong to.
- They use the `self` parameter to refer to the current instance of the class.

---

## Defining a Method

Use the `def` keyword inside the class to define a method. Methods are similar to regular functions but must include `self` as their first parameter.

### Example: Defining a Method

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Attribute
        self.age = age    # Attribute

    def greet(self):  # Method
        return f"Hello, my name is {self.name}."
```

---

## Using a Method

Call a method on an object using the dot (`.`) operator.

### Example: Calling a Method

```python
person = Person("Alice", 30)  # Create an instance of Person
print(person.greet())         # Call the greet method
```

### Output:

```plaintext
Hello, my name is Alice.
```

---

## Methods with Parameters

Methods can accept additional parameters to perform more specific actions.

### Example: Method with Parameters

```python
class Calculator:
    def add(self, a, b):
        return a + b
```

```python
calc = Calculator()
result = calc.add(5, 3)
print("Sum:", result)
```

### Output:

```plaintext
Sum: 8
```

---

## Modifying Attributes with Methods

Methods can modify the attributes of an object.

### Example: Modifying Attributes

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def have_birthday(self):
        self.age += 1  # Increment the age attribute

person = Person("Alice", 30)
person.have_birthday()
print(f"{person.name} is now {person.age} years old.")
```

### Output:

```plaintext
Alice is now 31 years old.
```

---

## The `self` Keyword

The `self` keyword refers to the current instance of the class. It is used to access attributes and other methods within the class.

### Example: Using `self` to Call Another Method

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name}."

    def introduce(self):
        return self.greet() + f" I am {self.age} years old."
```

```python
person = Person("Bob", 25)
print(person.introduce())
```

### Output:

```plaintext
Hello, my name is Bob. I am 25 years old.
```

---

## Summary

- **Methods** are functions defined inside a class to operate on objects.
- Use `self` to refer to the instance and access its attributes or methods.
- Methods can accept parameters to perform specific actions or calculations.
- Methods can modify an object's attributes to reflect changes in its state.

Practice creating classes with methods to understand how they define the behavior of objects.
