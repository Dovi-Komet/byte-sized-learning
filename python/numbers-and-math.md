---
title: "Numbers and Math"
order: 8
---

# Numbers and Math

Python makes it easy to work with numbers. Whether you're performing simple arithmetic or complex mathematical operations, Python provides a variety of tools to help you out.

---

### Types of Numbers in Python

Python has two primary types of numbers:

1. **Integers**: Whole numbers, positive or negative, without decimals.
    ```python
    age = 25  # Integer
    ```

2. **Floats**: Numbers with a decimal point.
    ```python
    price = 19.99  # Float
    ```

---

### Basic Mathematical Operations

You can perform common mathematical operations using Python’s arithmetic operators:

1. **Addition** (`+`)
    ```python
    result = 5 + 3
    print(result)  # Output: 8
    ```

2. **Subtraction** (`-`)
    ```python
    result = 5 - 3
    print(result)  # Output: 2
    ```

3. **Multiplication** (`*`)
    ```python
    result = 5 * 3
    print(result)  # Output: 15
    ```

4. **Division** (`/`)
    ```python
    result = 5 / 3
    print(result)  # Output: 1.666...
    ```

5. **Floor Division** (`//`) - Divides and rounds down to the nearest integer.
    ```python
    result = 5 // 3
    print(result)  # Output: 1
    ```

6. **Modulus** (`%`) - Returns the remainder of the division.
    ```python
    result = 5 % 3
    print(result)  # Output: 2
    ```

7. **Exponentiation** (`**`) - Raises a number to the power of another.
    ```python
    result = 5 ** 3
    print(result)  # Output: 125
    ```

---

### Order of Operations

Python follows the order of operations (PEMDAS), which stands for:

- **P**arentheses
- **E**xponents
- **M**ultiplication and **D**ivision (left to right)
- **A**ddition and **S**ubtraction (left to right)

Example:
```python
result = 2 + 3 * 4
print(result)  # Output: 14 (Multiplication happens first)
```

To change the order of operations, use parentheses:
```python
result = (2 + 3) * 4
print(result)  # Output: 20
```

---

### Practice Task

1. Create a new file called `math_example.py`.
2. Write the following code:

    ```python
    # Perform basic arithmetic
    sum_result = 10 + 5
    diff_result = 10 - 5
    prod_result = 10 * 5
    div_result = 10 / 5
    mod_result = 10 % 3
    exp_result = 2 ** 3

    # Print results
    print("Sum:", sum_result)
    print("Difference:", diff_result)
    print("Product:", prod_result)
    print("Division:", div_result)
    print("Modulus:", mod_result)
    print("Exponentiation:", exp_result)
    ```

3. Run the program and verify the output of each operation.

---

### Key Takeaways

- Python supports basic arithmetic operations such as addition, subtraction, multiplication, and division.
- Python also supports advanced operations like floor division, modulus, and exponentiation.
- Python follows the order of operations (PEMDAS), which you can control using parentheses.

---

### Next Steps

In the next lesson, we'll dive into working with strings, another fundamental data type in Python.
