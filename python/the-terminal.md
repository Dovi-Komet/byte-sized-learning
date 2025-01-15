---
title: "The Terminal"
order: 3
---

# The Terminal

The terminal (or command line) is a powerful tool for interacting with your computer. As a programmer, you'll often use the terminal to run Python scripts, manage files, and execute commands.

---

### What is the Terminal?

The terminal is a text-based interface where you can type commands to perform tasks instead of using a graphical interface. It's also called the **Command Prompt** on Windows or the **Terminal** on macOS and Linux.

---

### Basic Terminal Commands

Here are some common terminal commands you'll use:

1. **Navigate Directories**:
    - To list files in the current directory:
      ```bash
      ls   # macOS/Linux
      dir  # Windows
      ```
    - To change directories:
      ```bash
      cd <directory_name>
      ```
    - To go back one directory:
      ```bash
      cd ..
      ```

2. **Create a Directory**:
    ```bash
    mkdir <directory_name>
    ```

3. **Create a File**:
    ```bash
    touch <file_name>  # macOS/Linux
    echo. > <file_name>  # Windows
    ```

4. **Delete a File**:
    ```bash
    rm <file_name>  # macOS/Linux
    del <file_name>  # Windows
    ```

5. **Run a Python Script**:
    ```bash
    python <script_name>.py
    ```

---

### Practice Task

Try the following in your terminal:
1. Create a new directory called `python_practice`.
    ```bash
    mkdir python_practice
    ```
2. Navigate into the directory.
    ```bash
    cd python_practice
    ```
3. Create a file called `hello.py` and open it in your editor. Add the following code:
    ```python
    print("Hello from the terminal!")
    ```
4. Run the file in the terminal:
    ```bash
    python hello.py
    ```

You should see the output:

```plaintext
Hello from the terminal!
```

---

### Next Steps

Now that you're familiar with the terminal, we'll write and execute your first Python program in the next lesson.
