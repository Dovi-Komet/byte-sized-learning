---
layout: default
title: "User Input"
order: 10
---

In many programs, you will need to get input from the user. Python makes this easy with the `input()` function.

### Getting Input from the User

The `input()` function allows you to ask the user for information.

Example:

```python
name = input("What is your name? ")
print("Hello, " + name + "!")
```

### Expected Output (if the user enters "Alice")

```plaintext
What is your name? Alice
Hello, Alice!
```

### Converting Input

By default, the `input()` function returns the input as a string. If you need a number, you must convert it using `int()` or `float()`.

Example:

```python
age = input("How old are you? ")
age = int(age)  # Convert the input to an integer
print("You are " + str(age) + " years old!")
```

### Expected Output (if the user enters "25")

```plaintext
How old are you? 25
You are 25 years old!
```