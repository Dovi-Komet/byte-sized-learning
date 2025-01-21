---
title: "Error and Exception Handling"
order: 21
---

# Error and Exception Handling

Errors and exceptions are common in programming. Python provides tools to handle these issues gracefully, ensuring that programs don't crash unexpectedly and can recover from errors.

---

## Types of Errors

1. **Syntax Errors**:
   - Caused by incorrect Python syntax.
   - Detected before the program runs.
   - Example:
     ```python
     print("Hello"  # Missing closing parenthesis
     ```

2. **Runtime Errors**:
   - Occur while the program is running.
   - Example:
     ```python
     print(1 / 0)  # ZeroDivisionError
     ```

3. **Logical Errors**:
   - The program runs but produces incorrect results due to faulty logic.
   - Example:
     ```python
     # Incorrect calculation
     area = 2 * 3.14 * r  # Missing square of radius
     ```

---

## Exceptions

Exceptions are runtime errors that can be caught and handled. Python has several built-in exceptions, such as:
- `ValueError`
- `TypeError`
- `KeyError`
- `IndexError`
- `ZeroDivisionError`

---

## Try-Except Blocks

Use `try` and `except` to handle exceptions.

### Syntax:
```python
try:
    # Code that may raise an exception
except ExceptionType:
    # Code to handle the exception
```

### Example:
```python
try:
    x = int(input("Enter a number: "))
    print(10 / x)
except ValueError:
    print("That's not a valid number!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

---

## Catching Multiple Exceptions

You can handle multiple exceptions in the same `except` block.

### Example:
```python
try:
    result = 10 / int(input("Enter a number: "))
except (ValueError, ZeroDivisionError) as e:
    print(f"An error occurred: {e}")
```

---

## Using `else` and `finally`

- **`else`**: Executes if no exceptions occur.
- **`finally`**: Always executes, regardless of exceptions.

### Example:
```python
try:
    file = open("example.txt", "r")
    content = file.read()
except FileNotFoundError:
    print("File not found!")
else:
    print("File read successfully.")
finally:
    print("End of operation.")
```

---

## Raising Exceptions

Use `raise` to generate exceptions manually.

### Example:
```python
def divide(a, b):
    if b == 0:
        raise ZeroDivisionError("Cannot divide by zero!")
    return a / b

try:
    print(divide(10, 0))
except ZeroDivisionError as e:
    print(e)
```

---

## Custom Exceptions

You can create your own exception classes by inheriting from `Exception`.

### Example:
```python
class NegativeNumberError(Exception):
    pass

def check_positive(number):
    if number < 0:
        raise NegativeNumberError("Negative numbers are not allowed!")

try:
    check_positive(-5)
except NegativeNumberError as e:
    print(e)
```

---

## Best Practices for Exception Handling

1. **Catch Specific Exceptions**: Avoid using a generic `except` unless necessary.
2. **Use `finally` for Cleanup**: Close files, release resources, etc.
3. **Don't Suppress Exceptions**: Handle errors meaningfully.
4. **Raise Exceptions When Necessary**: For invalid states or inputs.

---

## Practice Exercises

1. **Handle User Input**:
   - Write a program that asks for a number and catches exceptions if the user enters invalid input.

2. **File Handling**:
   - Try opening a file that doesn’t exist and handle the exception.

3. **Custom Exception**:
   - Create a custom exception `TooSmallError` and raise it if a number is less than 5.

4. **Chained Exceptions**:
   - Create a nested `try-except` block where one exception leads to another.

Exception handling ensures that your programs are robust and user-friendly, even in unexpected scenarios.