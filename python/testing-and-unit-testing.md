---
title: "Testing and Unit Testing"
order: 35
---

# Testing and Unit Testing in Python

Testing ensures that code works as expected and helps prevent future issues when changes are made. Python provides several frameworks and tools to facilitate testing, with **unit testing** being a fundamental approach.

---

## Why Testing is Important

1. Ensures code correctness and reliability.
2. Reduces debugging time and effort.
3. Helps catch bugs early in development.
4. Facilitates easier code refactoring and updates.
5. Increases confidence in code quality.

---

## Types of Testing

1. **Unit Testing** – Tests individual functions or components.
2. **Integration Testing** – Tests how different modules work together.
3. **Functional Testing** – Tests the overall application behavior.
4. **Regression Testing** – Ensures new changes don’t break existing functionality.
5. **Performance Testing** – Evaluates speed and efficiency.

---

## Introduction to Unit Testing

Unit tests verify the smallest parts of an application, such as functions or methods, in isolation.

### Python's Built-in `unittest` Module

The `unittest` module provides a robust framework to write and run unit tests.

### Writing a Basic Unit Test

1. Import the `unittest` module.
2. Create a test class inheriting from `unittest.TestCase`.
3. Define test methods that start with `test_`.
4. Use assertions to check expected outcomes.

```python
import unittest

def add(a, b):
    return a + b

class TestMathOperations(unittest.TestCase):

    def test_addition(self):
        self.assertEqual(add(2, 3), 5)
        self.assertEqual(add(-1, 1), 0)

if __name__ == '__main__':
    unittest.main()
```

---

## Assertions in Unit Tests

Assertions verify expected outcomes. Common assertions in `unittest`:

- `assertEqual(a, b)` – Checks if `a == b`.
- `assertNotEqual(a, b)` – Checks if `a != b`.
- `assertTrue(x)` – Checks if `x` is `True`.
- `assertFalse(x)` – Checks if `x` is `False`.
- `assertRaises(exception, func, *args)` – Ensures an exception is raised.

Example:

```python
def divide(a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero")
    return a / b

class TestDivision(unittest.TestCase):

    def test_divide(self):
        self.assertEqual(divide(10, 2), 5)
        self.assertRaises(ValueError, divide, 10, 0)
```

---

## Running Tests

You can run tests using the command line:

```bash
python -m unittest test_module.py
```

Run all tests in a directory:

```bash
python -m unittest discover
```

---

## Organizing Tests

1. Store test files in a dedicated `tests/` directory.
2. Use consistent naming conventions (`test_*.py`).
3. Separate unit tests from integration tests.
4. Use mock objects to isolate dependencies.

Example project structure:

```
my_project/
│-- src/
│   ├── calculator.py
│-- tests/
│   ├── test_calculator.py
│-- main.py
```

---

## Mocking in Tests

Mocking allows us to simulate dependencies that are expensive, slow, or have side effects, like database calls or API requests.

### Using `unittest.mock`

```python
from unittest.mock import MagicMock

class APIClient:
    def fetch_data(self):
        return {"key": "value"}

def process_data(api_client):
    data = api_client.fetch_data()
    return data["key"]

def test_process_data():
    mock_client = APIClient()
    mock_client.fetch_data = MagicMock(return_value={"key": "mocked_value"})
    assert process_data(mock_client) == "mocked_value"
```

---

## Test Coverage

Test coverage measures how much of your code is executed by tests. A popular tool to check test coverage in Python is `coverage`.

### Install Coverage:

```bash
pip install coverage
```

### Run Coverage:

```bash
coverage run -m unittest discover
```

### Generate Coverage Report:

```bash
coverage report
coverage html
```

---

## Other Testing Frameworks

While `unittest` is built into Python, other frameworks offer additional features:

### 1. **pytest**
- More concise syntax.
- Powerful fixtures for setup and teardown.
- Rich plugin ecosystem.

Example with `pytest`:

```python
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
```

Run tests with:

```bash
pytest
```

### 2. **doctest**
Allows embedding tests in docstrings.

```python
def square(x):
    """
    Returns the square of x.

    >>> square(3)
    9
    >>> square(-4)
    16
    """
    return x * x
```

Run doctests:

```bash
python -m doctest -v script.py
```

---

## Continuous Integration (CI)

Automating tests using CI tools ensures code quality with every commit. Popular CI services:

- GitHub Actions
- GitLab CI/CD
- Jenkins
- Travis CI

Example GitHub Actions workflow for running tests:

```yaml
name: Python Tests

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.10'
      - name: Install dependencies
        run: pip install -r requirements.txt
      - name: Run tests
        run: pytest
```

---

## Best Practices for Writing Tests

1. **Write Tests Before Code (TDD)** – Helps define expected behavior early.
2. **Keep Tests Independent** – Avoid dependencies between tests.
3. **Use Meaningful Test Names** – Clearly describe the purpose of the test.
4. **Test Edge Cases** – Consider all possible input variations.
5. **Run Tests Frequently** – Ensure regular testing to catch issues early.

---

## Practice Exercises

1. Write unit tests for a function that checks if a number is prime.
2. Create a test case to verify that a function correctly handles empty inputs.
3. Implement a mock test for an API call using `unittest.mock`.

---

Unit testing is crucial for writing maintainable, error-free code. Mastering testing frameworks and techniques ensures software reliability and performance.