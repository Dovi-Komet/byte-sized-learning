---
layout: default
title: "Virtual Environments"
order: 89
---

Python's `venv` module helps you create isolated environments for projects.

### Creating a Virtual Environment

Example:

```plaintext
python -m venv myenv
```

### Activating the Environment

- On Windows:

```plaintext
myenv\Scripts\activate
```

- On macOS/Linux:

```plaintext
source myenv/bin/activate
```

### Deactivating the Environment

Run:

```plaintext
deactivate
```

Virtual environments are essential for managing dependencies separately for each project.
