---
layout: default
title: "Unit Testing"
order: 51
---

Unit testing is the process of testing individual units of code (e.g., functions, methods, or classes) to ensure they work as expected. Python provides the `unittest` module for writing and running tests.

---

## Why Unit Testing?

1. **Catch Bugs Early**: Identify issues in small, isolated parts of your code.
2. **Maintain Code Quality**: Ensure changes don’t break existing functionality.
3. **Improve Confidence**: Make it easier to refactor or extend your code.

---

## Writing a Test Case

A test case in Python is a class that inherits from `unittest.TestCase`. Each test method inside the class should start with `test_`.

### Example: Basic Test Case

```python
import unittest

def add(a, b):
    return a + b

class TestMathOperations(unittest.TestCase):
    def test_add(self):
        self.assertEqual(add(2, 3), 5)  # Check if add(2, 3) returns 5
        self.assertEqual(add(-1, 1), 0) # Check if add(-1, 1) returns 0

if __name__ == "__main__":
    unittest.main()
```

### Explanation:
1. The `add` function is the unit being tested.
2. The `TestMathOperations` class defines test methods.
3. `self.assertEqual()` checks if the actual result matches the expected result.

---

## Running Unit Tests

Save the test case in a file (e.g., `test_math.py`) and run it using the following command:

```bash
python -m unittest test_math.py
```

You’ll see output like this if all tests pass:

```plaintext
.
----------------------------------------------------------------------
Ran 1 test in 0.001s

OK
```

---

## Common Assertions in `unittest`

- `self.assertEqual(a, b)`: Check if `a` equals `b`.
- `self.assertNotEqual(a, b)`: Check if `a` does not equal `b`.
- `self.assertTrue(expr)`: Check if `expr` is `True`.
- `self.assertFalse(expr)`: Check if `expr` is `False`.
- `self.assertIn(item, container)`: Check if `item` is in `container`.

---

## Organizing Tests

1. **Separate Files**: Keep test files in a dedicated directory (e.g., `tests/`).
2. **Consistent Naming**: Use `test_` as a prefix for all test files and methods.

---

## Key Takeaways

- Unit testing ensures your code behaves as expected.
- Use the `unittest` module to define and run tests.
- Write small, focused test cases for each function or method.

---

In the next lesson, we’ll learn about testing with `pytest`, a powerful and user-friendly testing framework.
