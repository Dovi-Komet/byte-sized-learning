---
title: "Comments"
order: 6
---

# Comments in Python

Comments are lines in your code that Python ignores during execution. They are useful for documenting your code and making it easier to understand for yourself and others.

---

### Why Use Comments?

- **Clarify code**: Explain what your code does.
- **Debugging**: Temporarily disable certain parts of your code by commenting them out.
- **Collaboration**: Help others understand your code when working in teams.

---

### Types of Comments

1. **Single-Line Comments**

   Single-line comments start with a `#` symbol. Everything after `#` on that line is ignored by Python.

   Example:
   ```python
   # This is a single-line comment
   print("Hello, World!")  # This prints a greeting
   ```

2. **Multi-Line Comments**

   Python doesn’t have a specific syntax for multi-line comments, but you can use triple quotes (`'''` or `"""`) to simulate them.

   Example:
   ```python
   '''
   This is a multi-line comment.
   It spans multiple lines.
   '''
   print("Multi-line comments example")
   ```

   **Note**: Triple quotes are technically string literals. If they’re not assigned to a variable, they act like comments.

---

### Best Practices for Comments

1. **Keep comments concise and relevant.**
2. **Avoid obvious comments.** Example:
   ```python
   x = 10  # Assigns 10 to x
   ```
   The comment here doesn’t add value.
3. **Use comments to explain why, not what.** Example:
   ```python
   # Using a list comprehension for better performance
   squares = [x**2 for x in range(10)]
   ```

---

### Practice Task

1. Create a new file called `comments_example.py`.
2. Add the following code with appropriate comments:

    ```python
    # Calculate the square of numbers from 1 to 5
    for number in range(1, 6):
        # Print the square of the current number
        print(number**2)
    ```

3. Run the program and observe how comments help clarify what each part of the code does.

---

### Key Takeaways

- Use `#` for single-line comments and triple quotes for multi-line comments.
- Comments should enhance readability and understanding.
- Avoid over-commenting or stating the obvious.

---

### Next Steps

In the next lesson, we’ll learn about variables and data types in Python.
