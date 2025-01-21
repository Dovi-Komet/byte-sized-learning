---
title: "Encapsulation"
order: 24
---

# Encapsulation

**Encapsulation** is one of the four fundamental principles of Object-Oriented Programming (OOP). It restricts direct access to an object's internal state and allows controlled access through methods, ensuring the data's integrity and security.

---

## Key Concepts of Encapsulation

1. **Attributes and Methods**:
   - **Attributes**: Store data within an object.
   - **Methods**: Define the behavior of an object and control access to its attributes.

2. **Access Modifiers**:
   - **Public**: Accessible from anywhere.
   - **Protected**: Indicated by a single underscore (`_`) and meant to be accessed only within the class or subclasses.
   - **Private**: Indicated by a double underscore (`__`) and inaccessible from outside the class.

---

## Example of Public Access

Public attributes and methods can be accessed from anywhere.

```python
class Employee:
    def __init__(self, name, salary):
        self.name = name  # Public attribute
        self.salary = salary  # Public attribute

    def display_info(self):  # Public method
        print(f"Employee: {self.name}, Salary: {self.salary}")

emp = Employee("Alice", 50000)
print(emp.name)  # Output: Alice
emp.display_info()  # Output: Employee: Alice, Salary: 50000
```

---

## Example of Protected Access

Protected attributes are intended for use within the class and its subclasses.

```python
class Animal:
    def __init__(self, name):
        self._name = name  # Protected attribute

    def _make_sound(self):  # Protected method
        return "Generic sound"

class Dog(Animal):
    def bark(self):
        return f"{self._name} says Woof!"

dog = Dog("Buddy")
print(dog.bark())  # Output: Buddy says Woof!
```

---

## Example of Private Access

Private attributes are only accessible within the class and are not directly accessible from outside.

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
        else:
            print("Invalid deposit amount!")

    def get_balance(self):
        return self.__balance

account = BankAccount(1000)
account.deposit(500)
print(account.get_balance())  # Output: 1500
# print(account.__balance)  # Error: AttributeError
```

---

## Accessing Private Attributes

Private attributes can still be accessed using name mangling (not recommended for regular use).

```python
print(account._BankAccount__balance)  # Output: 1500
```

---

## Getters and Setters

Getters and setters are methods used to access and update private attributes in a controlled manner.

### Example:
```python
class Product:
    def __init__(self, price):
        self.__price = price  # Private attribute

    def get_price(self):  # Getter
        return self.__price

    def set_price(self, price):  # Setter
        if price > 0:
            self.__price = price
        else:
            print("Invalid price!")

product = Product(100)
print(product.get_price())  # Output: 100
product.set_price(150)
print(product.get_price())  # Output: 150
```

---

## Using `@property` for Getters and Setters

Python provides the `@property` decorator to simplify getter and setter methods.

### Example:
```python
class Employee:
    def __init__(self, name, salary):
        self.__name = name
        self.__salary = salary

    @property
    def salary(self):  # Getter
        return self.__salary

    @salary.setter
    def salary(self, value):  # Setter
        if value > 0:
            self.__salary = value
        else:
            print("Salary must be positive!")

emp = Employee("Alice", 50000)
print(emp.salary)  # Output: 50000
emp.salary = 60000
print(emp.salary)  # Output: 60000
```

---

## Benefits of Encapsulation

1. **Data Hiding**:
   - Protects sensitive data from direct modification.

2. **Control Access**:
   - Provides controlled ways to read or update attributes.

3. **Improved Maintainability**:
   - Encourages modular and organized code.

4. **Security**:
   - Ensures that the internal state of an object is consistent and valid.

---

## Practice Exercises

1. **Private Attributes**:
   - Create a `Student` class with private attributes `name` and `grade`.
   - Add getter and setter methods for both attributes.

2. **Protected Methods**:
   - Define a parent class `Vehicle` with a protected method `_engine`.
   - Create a subclass `Car` that overrides the `_engine` method.

3. **@property Decorators**:
   - Write a `Circle` class with a private attribute `radius`.
   - Use `@property` to calculate and return the area.

Encapsulation helps protect your data and ensures your objects behave predictably, making your programs robust and maintainable.