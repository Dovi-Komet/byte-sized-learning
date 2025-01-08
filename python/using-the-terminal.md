---
layout: default
title: "Using the Terminal"
order: 3
---

## Using the Terminal in VS Code

The terminal is a powerful tool that allows you to interact with your computer using text-based commands. In this lesson, you’ll learn how to open and use the terminal in Visual Studio Code (VS Code), as well as some basic commands to get started.

### What is the Terminal?

The terminal lets you:
- Run Python programs.
- Install and manage libraries.
- Interact with files and directories on your computer.

### Opening the Terminal in VS Code

To open the terminal in VS Code:
1. Open VS Code.
2. Click on the **View** menu at the top of the screen.
3. Select **Terminal** from the dropdown menu, or press ``Ctrl + ` `` (Windows/Linux) or ``Command + ` `` (macOS).

   This will open an integrated terminal at the bottom of the VS Code window.

### What is the Command Prompt?

On Windows, the terminal defaults to the Command Prompt (also called `cmd`). It’s a text-based interface where you can execute commands. For macOS or Linux, the default terminal is usually a Unix shell like Bash or Zsh. These interfaces allow similar functionality but may have slight differences in syntax for certain commands.

### Navigating the File System in the Terminal

The terminal starts in a specific directory (folder) on your computer. You can navigate and manage files using commands:

#### View the Contents of a Directory
- **Windows**: Use `dir` to list all files and folders in the current directory.
- **macOS/Linux**: Use `ls` to list all files and folders.

```bash
# Example (Windows):
dir
```

```bash
# Example (macOS/Linux):
ls
```

#### Change Directory (cd)
- Use `cd <directory-name>` to move into a folder.
- Use `cd ..` to go up one level in the directory structure.
- Use `cd /` (Linux/macOS) or `cd \` (Windows) to return to the root directory.

```bash
# Example (Windows):
cd Documents
```

```bash
# Example (macOS/Linux):
cd Documents
```

#### Check Your Current Directory
- **Windows**: Use `cd` to display the current directory path.
- **macOS/Linux**: Use `pwd` (print working directory).

```bash
# Example:
pwd
```

### Practical Examples

1. **Navigate to a Specific Folder**:
   Suppose you have a folder named `PythonProjects` in your `Documents` folder:
   ```bash
   cd Documents/PythonProjects
   ```

2. **Navigate Back to the Parent Folder**:
   If you’re in `PythonProjects` and want to return to `Documents`:
   ```bash
   cd ..
   ```

3. **Navigate Directly to a Drive (Windows)**:
   Switch to a specific drive (e.g., D:):
   ```bash
   D:
   ```

4. **List Files in the Current Directory**:
   After navigating, use `dir` (Windows) or `ls` (macOS/Linux) to confirm your location.

### Running Python Code in the Terminal

After navigating to the folder where your Python script is saved, you can run the script using:
```bash
python <script-name>.py
```

Replace `<script-name>.py` with the name of your Python file.

---

In the next lesson, you’ll write and run your very first Python program.
