---
layout: default
title: "Virtual Environments"
order: 56
---

Virtual environments are a way to create isolated Python environments for different projects. Each environment has its own set of libraries and dependencies, so you can avoid conflicts between different projects. This is especially useful when working on multiple projects that require different versions of libraries.

---

## Installing `virtualenv`

To create virtual environments, you'll need the `virtualenv` package. If you don't have it installed yet, you can install it using pip:

```bash
pip install virtualenv
```

Alternatively, if you’re using Python 3.3 or higher, you can use the built-in `venv` module to create virtual environments without needing to install any additional packages.

---

## Creating a Virtual Environment

Once you have `virtualenv` installed, you can create a new virtual environment by running:

```bash
python -m venv myenv
```

This will create a new directory called `myenv` (or any other name you choose) in your current directory. Inside the `myenv` folder, you'll find a complete Python environment, including the Python interpreter and the `lib` directory for installed packages.

---

## Activating the Virtual Environment

Before you can use the virtual environment, you'll need to activate it. The activation command depends on your operating system:

- **On Windows**:

```bash
myenv\Scripts\activate
```

- **On macOS/Linux**:

```bash
source myenv/bin/activate
```

Once the virtual environment is activated, you’ll see the name of the environment in your terminal prompt (e.g., `(myenv)`).

---

## Installing Packages in the Virtual Environment

With the virtual environment activated, you can install Python packages using `pip`. These packages will only be available inside the virtual environment.

For example, to install the `requests` library:

```bash
pip install requests
```

---

## Deactivating the Virtual Environment

When you're done working in the virtual environment, you can deactivate it by running:

```bash
deactivate
```

This will return you to the global Python environment.

---

## Using `requirements.txt` for Dependencies

When you’re working with a project that uses a virtual environment, it’s a good practice to list the packages and their versions in a `requirements.txt` file. This allows others to recreate the same environment.

To generate a `requirements.txt` file with all the installed packages:

```bash
pip freeze > requirements.txt
```

To install the packages from a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

---

## Key Takeaways

1. **Isolation**: Virtual environments allow you to keep your project dependencies isolated from other projects.
2. **Installing Packages**: Install packages within the virtual environment using `pip`.
3. **Deactivation**: You can deactivate the virtual environment when you're done working.
4. **`requirements.txt`**: Use this file to list and share project dependencies.

---