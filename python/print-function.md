---
title: "print Function"
order: 5
---

# The `print` Function

The `print()` function is one of the most commonly used functions in Python. It allows you to display text, numbers, and other data on the screen.

---

### Syntax of `print()`

The basic syntax of the `print()` function is:

```python
print(object, ..., sep=' ', end='\n', file=sys.stdout, flush=False)
```

- **object**: The data or message you want to display. You can provide one or more objects, separated by commas.
- **sep**: The separator between multiple objects. Default is a space (`' '`).
- **end**: The string appended at the end of the output. Default is a newline (`'\n'`).
- **file**: Specifies the output stream. Default is the standard output (`sys.stdout`).
- **flush**: If `True`, forces the output to be flushed immediately.

---

### Examples of `print()`

1. **Printing Text**:
    ```python
    print("Hello, World!")
    ```
    Output:
    ```plaintext
    Hello, World!
    ```

2. **Printing Numbers**:
    ```python
    print(42)
    ```
    Output:
    ```plaintext
    42
    ```

3. **Printing Multiple Values**:
    ```python
    print("The answer is", 42)
    ```
    Output:
    ```plaintext
    The answer is 42
    ```

4. **Using `sep`**:
    ```python
    print("Python", "is", "fun", sep="-")
    ```
    Output:
    ```plaintext
    Python-is-fun
    ```

5. **Using `end`**:
    ```python
    print("Hello", end=" ")
    print("World!")
    ```
    Output:
    ```plaintext
    Hello World!
    ```

---

### Practice Task

1. Create a new file named `print_examples.py`.
2. Write and run the following code:

    ```python
    # Print a greeting
    print("Welcome to Python!")

    # Print multiple values with custom separators
    print("Learning", "Python", "step", "by", "step", sep="->")

    # Print without a newline at the end
    print("This is the first line.", end=" ")
    print("This is the continuation.")
    ```

3. Observe the output and experiment with different `sep` and `end` values.

---

### Key Takeaways

- The `print()` function is highly versatile and can display various types of data.
- Customize the output format using `sep` and `end`.
- Practice using `print()` to get comfortable with its features.

---

### Next Steps

In the next lesson, we’ll explore how to use comments to document and clarify your Python code.
