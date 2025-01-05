---
layout: default
title: "User Input"
order: 12
---

In many programs, you will need to get input from the user. Python makes this easy with the `input()` function.

## Getting Input from the User

The `input()` function allows you to prompt the user for information. The text inside the parentheses is displayed to the user as a prompt.

### Example: Basic User Input

```python
name = input("What is your name? ")
print("Hello, " + name + "!")
```

### Expected Output (if the user enters "Alice")

```plaintext
What is your name? Alice
Hello, Alice!
```

## Converting Input

By default, the `input()` function returns the input as a string. To perform mathematical operations, you must convert the input to a number using `int()` or `float()`.

### Example: Adding Two Numbers

```python
num1 = input("Enter the first number: ")
num2 = input("Enter the second number: ")

# Convert inputs to integers for addition
num1 = int(num1)
num2 = int(num2)

result = num1 + num2
print("The sum is: " + str(result))  # Convert the result back to a string for printing
```

### Expected Output (if the user enters "5" and "3")

```plaintext
Enter the first number: 5
Enter the second number: 3
The sum is: 8
```

## Why Convert Back to a String?

When printing the result of a mathematical operation, Python requires all parts of the message to be strings. If you try to concatenate a number (like `result`) directly with a string, Python will raise an error.

### Example: Without Conversion

```python
result = 8
print("The sum is: " + result)  # This will raise an error
```

### Error Output

```plaintext
TypeError: can only concatenate str (not "int") to str
```

To avoid this, you must use the `str()` function to convert the number back into a string before concatenating it with other text.

## What Happens Without Conversion?

If you forget to convert inputs to numbers, Python will treat them as strings and concatenate them instead of performing arithmetic.

### Example: Missing Conversion

```python
num1 = input("Enter the first number: ")
num2 = input("Enter the second number: ")

result = num1 + num2  # Strings will be concatenated
print("The sum is: " + result)
```

### Expected Output (if the user enters "5" and "3")

```plaintext
Enter the first number: 5
Enter the second number: 3
The sum is: 53
```

## Summary

- Use `input()` to get information from the user.
- Convert inputs to numbers with `int()` or `float()` for calculations.
- Convert numbers back to strings with `str()` when combining them with text for printing.
- Failing to convert correctly can lead to errors or unexpected results.

Practice using user input and conversions to build dynamic, interactive programs!
