---
title: "The Terminal"
order: 3
---

# The Terminal

The terminal (or command line) is a powerful tool that allows you to interact with your computer directly using text commands. You'll often use it while working with Python for running scripts, managing files, and installing packages.

## What is the Terminal?

The terminal is a text-based interface where you can:
- Navigate your file system.
- Run programs and scripts.
- Perform administrative tasks.
- Manage packages and environments.

### Common Terminal Names:
- **Windows**: Command Prompt or PowerShell.
- **macOS**: Terminal.
- **Linux**: Terminal or Shell.

## Opening the Terminal

- **Windows**: Press `Win + R`, type `cmd`, and press Enter, or search for "PowerShell" in the Start menu.
- **macOS**: Press `Cmd + Space`, type `Terminal`, and press Enter.
- **Linux**: Look for "Terminal" in your applications menu or press `Ctrl + Alt + T`.

## Basic Commands

Here are some essential terminal commands:

| Command            | Description                                    |
|--------------------|------------------------------------------------|
| `pwd`              | Print the current working directory.          |
| `ls` (Linux/macOS) or `dir` (Windows) | List files and directories in the current directory. |
| `cd <directory>`   | Change to a specific directory.               |
| `mkdir <name>`     | Create a new directory.                       |
| `rm <file>`        | Remove a file.                                |
| `rmdir <directory>`| Remove an empty directory.                    |
| `touch <file>`     | Create a new file (Linux/macOS).              |

### Example:
```bash
# Navigate to Desktop
cd Desktop

# Create a folder called "python_course"
mkdir python_course

# Change into the folder
cd python_course

# Create a file
touch hello.py
```

## Running Python in the Terminal

Once Python is installed, you can use the terminal to run Python code.

1. Open the terminal.
2. Type `python` (or `python3` on some systems) and press Enter.
3. You'll see the Python interactive shell:
   ```
   Python 3.x.x (default, ...)
   Type "help", "copyright", "credits" or "license" for more information.
   >>>
   ```
4. Type Python commands directly, like:
   ```python
   >>> print("Hello, Python!")
   Hello, Python!
   ```

To exit the Python shell, type:
```bash
exit()
```

## Running Python Scripts

Instead of typing code interactively, you can run Python scripts saved in files:
1. Save your script (e.g., `script.py`).
2. Navigate to its location in the terminal using `cd`.
3. Run the script with:
   ```bash
   python script.py
   ```

## Practice Exercises

1. Open the terminal and navigate to your Desktop.
2. Create a folder called `python_practice`.
3. Inside the folder, create a file called `hello_world.py`.
4. Write a Python script to print "Hello, World!" and run it using the terminal.

With these basics, you're ready to use the terminal like a pro!
