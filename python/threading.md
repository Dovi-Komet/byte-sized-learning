---
layout: default
title: "Threading"
order: 71
---

The `threading` module enables parallel execution of code.

### Creating a Thread

Example:

```python
import threading

def print_numbers():
    for i in range(5):
        print(i)

thread = threading.Thread(target=print_numbers)
thread.start()
thread.join()
```

### Expected Output

```plaintext
0
1
2
3
4
```

### Using Multiple Threads

Example:

```python
def print_letters():
    for char in "ABCDE":
        print(char)

thread1 = threading.Thread(target=print_numbers)
thread2 = threading.Thread(target=print_letters)

thread1.start()
thread2.start()

thread1.join()
thread2.join()
```

### Expected Output (order may vary)

```plaintext
0
A
1
B
2
C
3
D
4
E
```

Threading helps improve performance in I/O-bound tasks.
