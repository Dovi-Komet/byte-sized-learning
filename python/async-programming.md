---
layout: default
title: "Async Programming"
order: 73
---

The `asyncio` module enables asynchronous programming in Python.

### Basics of `asyncio`

Example:

```python
import asyncio

async def greet():
    print("Hello")
    await asyncio.sleep(1)
    print("World")

asyncio.run(greet())
```

### Expected Output

```plaintext
Hello
World
```

### Concurrent Tasks

Example:

```python
async def task1():
    await asyncio.sleep(1)
    print("Task 1 complete")

async def task2():
    await asyncio.sleep(2)
    print("Task 2 complete")

async def main():
    await asyncio.gather(task1(), task2())

asyncio.run(main())
```

### Expected Output

```plaintext
Task 1 complete
Task 2 complete
```

Asynchronous programming is useful for I/O-bound tasks, such as web scraping or API requests.
