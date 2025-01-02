---
layout: default
title: "Multiprocessing"
order: 72
---

The `multiprocessing` module is used to run code in parallel processes.

### Creating a Process

Example:

```python
import multiprocessing

def print_numbers():
    for i in range(5):
        print(i)

process = multiprocessing.Process(target=print_numbers)
process.start()
process.join()
```

### Expected Output

```plaintext
0
1
2
3
4
```

### Using Multiple Processes

Example:

```python
def print_letters():
    for char in "ABCDE":
        print(char)

process1 = multiprocessing.Process(target=print_numbers)
process2 = multiprocessing.Process(target=print_letters)

process1.start()
process2.start()

process1.join()
process2.join()
```

### Expected Output (order may vary)

```plaintext
0
1
2
3
4
A
B
C
D
E
```

Multiprocessing is useful for CPU-bound tasks requiring separate memory spaces.
