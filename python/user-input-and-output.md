---
title: "User Input and Output"
order: 10
---

# User Input and Output

Interacting with users is a fundamental part of many Python programs. Python provides simple functions to **read input** from users and **output information** to the screen.

---

## Output: `print()`

The `print()` function is used to display messages, variables, or results on the screen.

### Basic Usage:
```python
# Print a string
print("Hello, World!")

# Print variables
name = "Alice"
age = 30
print("Name:", name, "Age:", age)

# Using f-strings for output
print(f"My name is {name} and I am {age} years old.")
```

### Printing with Formatting
You can customize the output format:
```python
# Print with separators
print("Python", "is", "fun", sep=" - ")  # Python - is - fun

# Print with an end character
print("This is line 1.", end=" ")
print("This is line 2.")  # This is line 1. This is line 2.
```

---

## Input: `input()`

The `input()` function allows you to read input from the user. It always returns the input as a string.

### Basic Usage:
```python
# Reading input
name = input("What is your name? ")
print(f"Hello, {name}!")
```

### Converting Input
Since `input()` returns a string, you may need to convert it to other types like integers or floats.

```python
# Converting to an integer
age = input("Enter your age: ")
age = int(age)
print(f"You are {age} years old.")

# Converting to a float
height = float(input("Enter your height in meters: "))
print(f"Your height is {height}m.")
```

### Handling Multiple Inputs
You can split user input into multiple values using the `split()` method:
```python
# Input multiple values
data = input("Enter two numbers separated by space: ")
a, b = map(int, data.split())
print(f"Sum: {a + b}")
```

---

## Common Use Cases

### Greeting Example:
```python
name = input("What is your name? ")
print(f"Nice to meet you, {name}!")
```

### Adding Numbers:
```python
num1 = int(input("Enter the first number: "))
num2 = int(input("Enter the second number: "))
print(f"The sum is: {num1 + num2}")
```

### Custom Output Formatting:
```python
item = input("Enter an item: ")
price = float(input("Enter the price: "))
print(f"The price of {item} is ${price:.2f}.")
```

---

## Practice Exercises

1. Write a program to:
   - Ask the user for their first and last name.
   - Print a greeting that includes their full name.

2. Write a program to:
   - Ask the user for two numbers.
   - Calculate and display their sum, difference, product, and quotient.

3. Create a program that:
   - Asks the user for their birth year.
   - Calculates and displays their current age (use `2025` as the current year).

4. Ask the user for three numbers separated by spaces. Calculate and print:
   - Their sum.
   - Their average.

Mastering user input and output is essential for creating interactive Python programs!
