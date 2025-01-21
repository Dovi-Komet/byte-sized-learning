---
title: "OOP Basics"
order: 22
---

# OOP Basics

**Object-Oriented Programming (OOP)** is a programming paradigm that organizes code into objects, which are instances of classes. This approach helps structure programs for better readability, reusability, and scalability.

---

## Key OOP Concepts

1. **Class**:
   - A blueprint for creating objects.
   - Defines attributes (data) and methods (functions).

2. **Object**:
   - An instance of a class.
   - Contains specific data and can perform actions defined in the class.

3. **Attributes**:
   - Variables that store data for objects.

4. **Methods**:
   - Functions defined inside a class to perform actions.

---

## Defining a Class

Use the `class` keyword to define a class.

### Example:
```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Attribute
        self.age = age    # Attribute

    def greet(self):      # Method
        print(f"Hello, my name is {self.name}.")
```

---

## Creating an Object

Create an object by calling the class like a function.

### Example:
```python
# Create an object
person1 = Person("Alice", 30)

# Access attributes
print(person1.name)  # Output: Alice
print(person1.age)   # Output: 30

# Call methods
person1.greet()  # Output: Hello, my name is Alice.
```

---

## The `__init__` Method

The `__init__` method initializes object attributes when an object is created.

### Example:
```python
class Dog:
    def __init__(self, breed, color):
        self.breed = breed
        self.color = color

dog1 = Dog("Labrador", "Yellow")
print(dog1.breed)  # Output: Labrador
```

---

## Adding Methods

Methods define the behavior of a class.

### Example:
```python
class Calculator:
    def add(self, a, b):
        return a + b

calc = Calculator()
print(calc.add(3, 5))  # Output: 8
```

---

## Class vs Instance Attributes

- **Class Attributes**:
  - Shared across all instances of the class.
  - Defined outside the `__init__` method.

- **Instance Attributes**:
  - Unique to each object.
  - Defined inside the `__init__` method.

### Example:
```python
class Car:
    wheels = 4  # Class attribute

    def __init__(self, brand):
        self.brand = brand  # Instance attribute

car1 = Car("Toyota")
car2 = Car("Ford")

print(car1.wheels)  # Output: 4
print(car1.brand)   # Output: Toyota
```

---

## Encapsulation

Encapsulation restricts access to certain parts of an object to protect its internal state.

- Use `_attribute` for protected attributes.
- Use `__attribute` for private attributes.

### Example:
```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance

account = BankAccount(100)
account.deposit(50)
print(account.get_balance())  # Output: 150
```

---

## Benefits of OOP

1. **Modularity**: Code is organized into classes and objects.
2. **Reusability**: Classes can be reused in other programs.
3. **Scalability**: Easy to manage and extend large programs.
4. **Data Hiding**: Protects internal data from direct modification.

---

## Practice Exercises

1. **Create a Class**:
   - Define a class `Student` with attributes `name` and `grade`.
   - Add a method `is_passing` that returns `True` if the grade is >= 50.

2. **Bank Account**:
   - Create a class `Account` with methods to `deposit`, `withdraw`, and `check_balance`.

3. **Car Class**:
   - Define a class `Car` with class attribute `wheels` and instance attributes `brand` and `model`.
   - Add a method to display car details.

4. **Encapsulation**:
   - Create a class `Library` with a private attribute `_books` and methods to add, remove, and list books.

OOP is a cornerstone of modern programming, enabling the creation of organized and reusable code.