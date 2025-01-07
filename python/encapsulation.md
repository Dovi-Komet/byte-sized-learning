---
layout: default
title: "Encapsulation"
order: 48
---

Encapsulation is a key principle of Object-Oriented Programming (OOP). It involves restricting access to certain parts of an object and exposing only the necessary functionality. This helps protect the internal state of an object and enforces controlled access to its data.

---

## What Is Encapsulation?

Encapsulation allows you to:
1. **Hide implementation details** from the outside world.
2. **Expose a public interface** for interacting with the object.
3. **Control access** to attributes and methods to ensure data integrity.

---

## Public Attributes and Methods

By default, all attributes and methods in Python are public, meaning they can be accessed directly from outside the class.

### Example: Public Attributes

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Public attribute
        self.age = age    # Public attribute

person = Person("Alice", 30)
print(person.name)  # Accessing public attribute
print(person.age)   # Accessing public attribute
```

### Output:

```plaintext
Alice
30
```

---

## Private Attributes

Private attributes are prefixed with a double underscore (`__`). They cannot be accessed directly from outside the class.

### Example: Private Attributes

```python
class Person:
    def __init__(self, name, age):
        self.__name = name  # Private attribute
        self.__age = age    # Private attribute

    def get_info(self):  # Public method to access private attributes
        return f"{self.__name} is {self.__age} years old."

person = Person("Bob", 25)
print(person.get_info())
# print(person.__name)  # This will raise an AttributeError
```

### Output:

```plaintext
Bob is 25 years old.
```

### Why Use Private Attributes?

- To prevent external modification of sensitive data.
- To enforce validation or specific behavior when accessing or modifying attributes.

---

## Accessing Private Attributes Indirectly

You can provide **getter** and **setter** methods to access and modify private attributes indirectly.

### Example: Getter and Setter Methods

```python
class Person:
    def __init__(self, name, age):
        self.__name = name
        self.__age = age

    # Getter for name
    def get_name(self):
        return self.__name

    # Setter for name
    def set_name(self, name):
        if name:  # Simple validation
            self.__name = name
        else:
            print("Name cannot be empty.")

person = Person("Charlie", 40)
print(person.get_name())  # Access private attribute via getter

person.set_name("Charles")  # Modify private attribute via setter
print(person.get_name())
```

### Output:

```plaintext
Charlie
Charles
```

---

## Name Mangling in Python

Private attributes in Python are not truly private; they are "name-mangled" to prevent accidental access. This means the attribute's actual name is changed internally.

### Example: Name Mangling

```python
class Example:
    def __init__(self):
        self.__private = "This is private"

obj = Example()
# Access using name mangling
print(obj._Example__private)
```

### Output:

```plaintext
This is private
```

While name mangling allows access to private attributes, it is not recommended. Use public methods instead.

---

## Summary

- **Public Attributes**:
  - Accessible directly from outside the class.
  - Suitable for non-sensitive data.
- **Private Attributes**:
  - Prefixed with `__` to restrict direct access.
  - Accessed and modified via getter and setter methods.
- **Encapsulation Benefits**:
  - Protects the internal state of an object.
  - Ensures controlled and validated access to data.

Encapsulation is essential for creating secure and maintainable code. Practice using private attributes and methods to understand how encapsulation enhances your programs.
