---
layout: default
title: "Multiple Inheritance"
order: 57
---

In Python, a class can inherit from more than one parent class. This is called multiple inheritance.

### Example of Multiple Inheritance

Example:

```python
class Parent1:
    def greet(self):
        return "Hello from Parent1!"

class Parent2:
    def welcome(self):
        return "Welcome from Parent2!"

class Child(Parent1, Parent2):
    pass

child = Child()
print(child.greet())
print(child.welcome())
```

### Expected Output

```plaintext
Hello from Parent1!
Welcome from Parent2!
```

### Method Resolution Order (MRO)

When a method is called, Python uses the Method Resolution Order (MRO) to determine which method to execute. Use the `mro()` method to view the MRO:

```python
print(Child.mro())
```

### Expected Output

```plaintext
[<class '__main__.Child'>, <class '__main__.Parent1'>, <class '__main__.Parent2'>, <class 'object'>]
```

Understanding MRO is important when working with multiple inheritance.