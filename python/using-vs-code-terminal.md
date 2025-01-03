---
layout: default
title: "Using VS Code Terminal"
order: 3
---

The terminal is a powerful tool for interacting with your computer and running Python code. Let’s learn how to use it.

## Opening the Terminal in VS Code

1. Open VS Code.
2. Press `Ctrl + ~` (Windows/Linux) or `Cmd + ~` (Mac) to open the terminal.
3. Alternatively, go to the top menu, click on **View**, and select **Terminal**.

When the terminal opens, you will see a command prompt. This indicates your current location in the file system. For example:

```plaintext
C:\Users\YourName\Documents>  # On Windows
/Users/yourname/Documents>    # On Mac/Linux
```

The text before the `>` or `$` symbol is the current directory. You can interact with files and navigate the file system from here.

## Navigating the File System

You can move around the file system using the `cd` (change directory) command and view the contents of directories with the `ls` command.

### Viewing Directory Contents

- To list the files and folders in your current directory, type:
  ```bash
  ls
  ```
- After typing `ls`, **press the Enter key** to execute the command. You will see a list of files and folders in your current directory.

### Moving to a Different Directory

1. **Using a Relative Path**:
   - A relative path starts from your current directory. For example:
     ```bash
     cd my_folder
     ```
     This moves you into a folder named `my_folder` that is inside your current directory.

2. **Using a Full (Absolute) Path**:
   - A full path specifies the exact location of a folder, starting from the root of the file system. On Windows, for example:
     ```bash
     cd C:\Users\YourName\Documents\my_folder
     ```
     On Mac/Linux:
     ```bash
     cd /Users/yourname/Documents/my_folder
     ```
     Replace the example paths with the actual path to your folder.

3. **Moving Up a Level**:
   - To move up to the parent directory of your current location, type:
     ```bash
     cd ..
     ```
     
### Practice Navigating

Practice the following:
1. Use `ls` to view the files and folders in your current directory.
2. Navigate to a specific folder using `cd` with a relative or full path.
3. List the contents of that folder.
4. Move back to the parent directory using `cd ..`.

### Running Python Scripts (Preview)

To run a Python script, you will use the following command:
```bash
python script_name.py
```
Replace `script_name.py` with the name of the file you want to run. While we haven’t written any scripts yet, keep this command in mind for later lessons.

## When to Use `py` vs `python`

- On Windows, the `py` command is often used because it ensures the correct Python version is executed, especially if multiple versions are installed. 
- The `python` command may work the same way, but if you encounter issues (e.g., it starts the wrong version), use `py`.
- On Mac/Linux, the `python` command is typically used. If Python 2 is also installed, you might need to use `python3` to explicitly invoke Python 3.

In the next lesson, we’ll write and run our first Python program!
