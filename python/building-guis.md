---
layout: default
title: "Building GUIs"
order: 85
---

Tkinter is the standard library for creating GUI applications in Python.

### Creating a Simple GUI

Example:

```python
import tkinter as tk

def on_click():
    label.config(text="Button clicked!")

root = tk.Tk()
root.title("Simple GUI")

label = tk.Label(root, text="Hello, Tkinter!")
label.pack()

button = tk.Button(root, text="Click Me", command=on_click)
button.pack()

root.mainloop()
```

### Expected Output

A simple window with a label and a button that updates the label text.

Tkinter makes it easy to create basic desktop applications.
