---
title: "Functions"
order: 14
---

# Functions

**Functions** allow you to organize your code into reusable blocks. They help improve readability, reduce repetition, and make your code more modular.

---

## Defining Functions

You define a function in Python using the `def` keyword.

### Syntax:
```python
def function_name(parameters):
    # Code to execute
    return result  # Optional
```

### Example:
```python
def greet(name):
    print(f"Hello, {name}!")
```

---

## Calling Functions

To execute a function, you "call" it by using its name followed by parentheses.

### Example:
```python
# Define the function
def greet(name):
    print(f"Hello, {name}!")

# Call the function
greet("Alice")  # Output: Hello, Alice!
```

---

## Function Parameters and Arguments

Functions can take **parameters** (placeholders) that are replaced with **arguments** (values) when the function is called.

### Example:
```python
def add(a, b):
    return a + b

result = add(5, 3)
print(result)  # Output: 8
```

### Default Parameters:
You can provide default values for parameters.
```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()          # Output: Hello, Guest!
greet("Alice")   # Output: Hello, Alice!
```

### Keyword Arguments:
You can specify arguments by name when calling the function.
```python
def introduce(name, age):
    print(f"My name is {name} and I am {age} years old.")

introduce(age=25, name="Bob")
```

---

## Return Values

Functions can return values using the `return` statement.

### Example:
```python
def square(num):
    return num * num

result = square(4)
print(result)  # Output: 16
```

If no `return` is used, the function returns `None` by default.

---

## Scope of Variables

Variables created inside a function have **local scope** and are not accessible outside the function.

### Example:
```python
def my_function():
    x = 10  # Local variable
    print(x)

my_function()
# print(x)  # Error: x is not defined
```

---

## `*args` and `**kwargs`

### `*args`: Allows a function to accept any number of positional arguments.
```python
def sum_all(*numbers):
    return sum(numbers)

print(sum_all(1, 2, 3, 4))  # Output: 10
```

### `**kwargs`: Allows a function to accept any number of keyword arguments.
```python
def print_info(**info):
    for key, value in info.items():
        print(f"{key}: {value}")

print_info(name="Alice", age=30, city="New York")
```

---

## Anonymous Functions (`lambda`)

Lambda functions are one-liner functions defined using the `lambda` keyword.

### Syntax:
```python
lambda arguments: expression
```

### Example:
```python
square = lambda x: x * x
print(square(5))  # Output: 25
```

---

## Common Use Cases

1. **Reusable Logic**:
   ```python
   def is_even(num):
       return num % 2 == 0

   print(is_even(4))  # True
   print(is_even(7))  # False
   ```

2. **Mathematical Operations**:
   ```python
   def add(a, b):
       return a + b

   print(add(3, 5))  # 8
   ```

3. **Working with Lists**:
   ```python
   def double_elements(elements):
       return [x * 2 for x in elements]

   print(double_elements([1, 2, 3]))  # [2, 4, 6]
   ```

---

## Practice Exercises

1. Write a function `greet_user(name)` that:
   - Takes a user's name as input.
   - Prints a greeting like "Hello, [name]!"

2. Create a function `calculate_area(length, width)` that:
   - Takes two arguments (length and width).
   - Returns the area of a rectangle.

3. Define a function `find_max(numbers)` that:
   - Accepts a list of numbers.
   - Returns the largest number in the list.

4. Build a function `is_prime(num)` that:
   - Checks if a number is prime.
   - Returns `True` if it is, and `False` otherwise.

Functions are a core concept in Python and form the building blocks of reusable and efficient code!
