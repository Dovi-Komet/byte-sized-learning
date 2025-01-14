---
layout: default
title: "Encapsulation"
order: 46
---

Encapsulation is a principle in object-oriented programming (OOP) that restricts direct access to some of an object's components, protecting the data and ensuring it is accessed and modified in a controlled way. It is implemented using access modifiers in Python.

---

## Public, Protected, and Private Attributes

### Public Attributes

Attributes that can be accessed from anywhere in the program.

```python
class Person:
    def __init__(self, name):
        self.name = name  # Public attribute

person = Person("Alice")
print(person.name)  # Output: Alice
```

---

### Protected Attributes

Attributes prefixed with a single underscore (`_`) are treated as protected. They can still be accessed directly but are intended to be accessed only within the class and its subclasses.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self._age = age  # Protected attribute

    def get_age(self):
        return self._age

person = Person("Alice", 30)
print(person._age)  # Output: 30 (direct access, but not recommended)
```

---

### Private Attributes

Attributes prefixed with double underscores (`__`) are private and cannot be accessed directly outside the class. This enforces stricter encapsulation.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.__age = age  # Private attribute

    def get_age(self):
        return self.__age  # Controlled access through a method

person = Person("Alice", 30)
# print(person.__age)  # Raises AttributeError
print(person.get_age())  # Output: 30
```

- **Explanation**:
  - The private attribute `__age` is accessed using the `get_age` method.
  - Direct access to `__age` raises an `AttributeError`.

---

## Benefits of Encapsulation

1. **Data Protection**: Prevents unauthorized access or modification of data.
2. **Controlled Access**: Allows data to be accessed or modified only through specific methods.
3. **Flexibility**: Implementation details can be changed without affecting external code.

---

## Example: Encapsulation in Action

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
            return f"Deposited {amount}. New balance: {self.__balance}"
        return "Invalid deposit amount."

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount
            return f"Withdrew {amount}. New balance: {self.__balance}"
        return "Invalid withdrawal amount or insufficient funds."

    def get_balance(self):
        return self.__balance

# Using the BankAccount class
account = BankAccount(100)
print(account.get_balance())  # Output: 100
print(account.deposit(50))    # Output: Deposited 50. New balance: 150
print(account.withdraw(30))   # Output: Withdrew 30. New balance: 120
# print(account.__balance)    # Raises AttributeError
```

---

Encapsulation ensures that the internal state of an object is protected and managed properly. In the next lesson, we’ll explore polymorphism and how it allows objects to be used interchangeably.
