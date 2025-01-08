---
layout: default
title: "First Python Program"
order: 4
---

## Writing and Running Your First Python Program

Congratulations on setting up your Python environment! Now, let’s write and run your very first Python program.

### Step 1: Open VS Code

1. Launch Visual Studio Code (VS Code).
2. Open a folder to save your Python file:
   - Click **File** > **Open Folder** (or **Open...** on macOS).
   - Choose or create a folder where you want to save your work.

### Step 2: Create a Python File

1. In VS Code, click the **Explorer** icon in the left sidebar.
2. Click the **New File** icon and name the file `first_program.py`. Make sure the file ends with `.py`, as this indicates a Python file.

### Step 3: Write Your First Python Program

Type the following code into your `first_program.py` file:

```python
# This is your first Python program
print("Hello, World!")
```

#### Code Explanation:
- **`# This is your first Python program`**: This is a comment and won't be executed. Comments are used to explain code.
- **`print("Hello, World!")`**: This command tells Python to display the text "Hello, World!" on the screen.

### Step 4: Run Your Program

1. Open the terminal in VS Code:
   - Go to **View** > **Terminal**, or press ``Ctrl + ` `` (Windows/Linux) or ``Command + ` `` (macOS).
2. Navigate to the folder where your `first_program.py` file is saved using the `cd` command in the terminal (see the previous lesson for navigating directories).
3. Run the program by typing:
   ```bash
   python first_program.py
   ```

   If you’re using macOS or Linux, you might need to type:
   ```bash
   python3 first_program.py
   ```

### Step 5: View the Output

You should see the following output in the terminal:

```plaintext
Hello, World!
```

This means your program ran successfully!

---

In the next lesson, we’ll explore the `print()` function in more detail.
