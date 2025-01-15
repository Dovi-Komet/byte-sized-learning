---
title: "Variables and Types"
order: 7
---

# Variables and Types

Variables are used to store data in Python, and each variable has a specific type that determines what kind of data it holds.

---

### What is a Variable?

A variable is a name that refers to a value. You can think of it as a labeled container that holds information.

Example:
```python
age = 25  # The variable 'age' stores the value 25
```

---

### Rules for Naming Variables

1. Variable names must start with a letter or an underscore (`_`).
2. They can contain letters, numbers, and underscores, but cannot start with a number.
3. Variable names are case-sensitive (`Age` and `age` are different).
4. Avoid using Python reserved keywords (e.g., `if`, `else`, `while`).

---

### Data Types in Python

Python has several built-in data types, and the type of a variable is determined automatically when you assign a value.

1. **Numbers**
    - Integers: Whole numbers.
      ```python
      age = 25
      ```
    - Floats: Numbers with a decimal point.
      ```python
      price = 19.99
      ```

2. **Strings**
    - Text data, enclosed in single or double quotes.
      ```python
      name = "Alice"
      greeting = 'Hello'
      ```

3. **Booleans**
    - Represents `True` or `False`.
      ```python
      is_logged_in = True
      ```

4. **NoneType**
    - Represents the absence of a value.
      ```python
      result = None
      ```

---

### Checking Data Types

You can use the `type()` function to check the type of a variable:

```python
age = 25
print(type(age))  # Output: <class 'int'>
```

---

### Practice Task

1. Create a new file called `variables_example.py`.
2. Write the following code:

    ```python
    # Assign values to variables
    name = "John"
    age = 30
    is_student = True

    # Print the values and their types
    print("Name:", name, "- Type:", type(name))
    print("Age:", age, "- Type:", type(age))
    print("Is student:", is_student, "- Type:", type(is_student))
    ```

3. Run the program and observe the output.

---

### Key Takeaways

- Variables store data, and their types are inferred based on the value assigned.
- Python supports various data types like integers, floats, strings, booleans, and `NoneType`.
- Use `type()` to check the type of a variable.

---

### Next Steps

In the next lesson, we’ll explore how to work with numbers and perform mathematical operations in Python.
