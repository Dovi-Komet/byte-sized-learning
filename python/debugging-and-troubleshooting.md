---
title: "Debugging and Troubleshooting"
order: 34
---

# Debugging and Troubleshooting in Python

Debugging is the process of identifying and fixing errors in your code. Python provides various tools and techniques to help troubleshoot issues efficiently.

---

## Common Types of Errors

1. **Syntax Errors** – Occur when the code violates Python's syntax rules.
   ```python
   print("Hello"  # Missing closing parenthesis
   ```

2. **Runtime Errors (Exceptions)** – Occur during execution, such as division by zero.
   ```python
   result = 10 / 0  # ZeroDivisionError
   ```

3. **Logical Errors** – The program runs without errors but produces incorrect results.

---

## Debugging Techniques

### 1. Print Statements
Adding `print()` statements is a simple yet effective way to track variable values.

```python
def add_numbers(a, b):
    print(f"a: {a}, b: {b}")
    return a + b

result = add_numbers(5, "10")  # Intentional error
```

### 2. Using Assertions
Assertions help catch bugs early by validating assumptions.

```python
def divide(x, y):
    assert y != 0, "Denominator should not be zero"
    return x / y

divide(10, 0)  # AssertionError
```

### 3. Python's Built-in `pdb` Debugger
Python Debugger (`pdb`) allows stepping through code interactively.

```python
import pdb

def faulty_function(x):
    pdb.set_trace()  # Start debugging session
    y = x + 2
    return y

faulty_function(5)
```

#### Useful `pdb` Commands:
- `n` – Execute the next line.
- `c` – Continue execution.
- `p variable` – Print variable value.
- `q` – Quit the debugger.

### 4. Using `logging` for Better Insights
Instead of `print()`, use logging for tracking program execution in production.

```python
import logging

logging.basicConfig(level=logging.DEBUG)
logging.debug("This is a debug message")
```

### 5. Exception Handling with `try-except`
Catching exceptions prevents crashes and provides error messages.

```python
try:
    num = int("abc")  # ValueError
except ValueError as e:
    print(f"Error: {e}")
```

---

## Debugging Tools

### 1. **Using IDE Debuggers**
Most IDEs like PyCharm and VSCode offer built-in debuggers with features like breakpoints, watches, and stepping.

### 2. **Using `trace` Module**
Trace module helps track function calls.

```python
import trace

def sample_function():
    print("Tracing this function")

tracer = trace.Trace()
tracer.runfunc(sample_function)
```

### 3. **Using `cProfile` for Performance Debugging**
Analyze the runtime of different parts of your code.

```python
import cProfile

def compute():
    total = sum(range(100000))
    print(total)

cProfile.run("compute()")
```

---

## Troubleshooting Strategies

1. **Reproduce the Error**  
   - Clearly understand how and when the issue occurs.

2. **Read the Error Message Carefully**  
   - Analyze the stack trace to pinpoint the problem.

3. **Divide and Conquer**  
   - Isolate parts of the code to identify where the issue lies.

4. **Check Recent Changes**  
   - Review modifications that might have introduced the bug.

5. **Rubber Duck Debugging**  
   - Explain the code to someone else or even to a rubber duck!

6. **Search for Solutions**  
   - Utilize online resources such as Stack Overflow and Python documentation.

7. **Keep Track of Bugs**  
   - Use issue tracking systems like GitHub Issues or Jira.

---

## Common Debugging Scenarios

### 1. Handling Infinite Loops
Check for incorrect loop conditions.

```python
i = 0
while i < 5:
    print(i)
# Missing i += 1 leads to an infinite loop
```

### 2. Fixing Off-by-One Errors
Carefully check index ranges in loops and slicing.

```python
items = [1, 2, 3]
for i in range(len(items)):  # Correct range
    print(items[i])
```

### 3. Tracking Unintended Variable Modifications
Use breakpoints to monitor variable changes in loops.

```python
x = 10
for _ in range(5):
    x += 2
print(x)  # Is x the expected value?
```

---

## Best Practices for Debugging

1. **Write Readable Code**  
   - Clear code reduces the chance of introducing bugs.

2. **Test Small Units of Code**  
   - Use unit testing to verify functions individually.

3. **Use Version Control**  
   - Track code changes to revert when needed.

4. **Automate Testing**  
   - Continuous integration tools help catch bugs early.

5. **Document Known Issues**  
   - Maintain documentation of recurring issues and their solutions.

---

## Practice Exercises

1. **Debug the Following Code:**
   ```python
   def multiply(x, y):
       return x * y

   print(multiply(5))  # Fix the missing argument
   ```

2. **Identify and Fix the Bug:**
   ```python
   numbers = [1, 2, 3, 4, 5]
   print(numbers[5])  # Out-of-range error
   ```

3. **Use Logging Instead of Print:**
   ```python
   def greet(name):
       print("Hello", name)  # Convert to logging
   ```

Debugging is an essential skill in software development. Mastering debugging techniques and tools will help you identify and resolve issues efficiently.
