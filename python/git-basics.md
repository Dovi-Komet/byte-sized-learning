---
layout: default
title: "Git Basics"
order: 55
---

Git is a version control system that helps you track changes in your code and collaborate with others. It allows you to manage different versions of your project, keep a history of changes, and even revert to previous versions if needed.

---

## Installing Git

Before you can start using Git, you'll need to install it. You can download Git from the official website:

[Download Git](https://git-scm.com/downloads){:target="_blank"}

Follow the installation instructions for your operating system.

---

## Setting Up Git

Once Git is installed, you'll need to configure it with your name and email address. These will be associated with the commits you make.

### Configuring Your Identity

Run the following commands in your terminal to set your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Verifying Your Configuration

You can verify your configuration by running:

```bash
git config --list
```

This will display the settings you've configured, such as your name and email.

---

## Creating a New Git Repository

A Git repository (or "repo") is where your project files and their version history are stored. To create a new repository, navigate to your project folder and run:

```bash
git init
```

This will initialize a new Git repository in your project directory.

---

## Tracking Files with Git

Once you have initialized a Git repository, you can start tracking changes in your project files. Git tracks changes in files and stages them for committing.

### Adding Files to Git

To add a file to Git for tracking, use the following command:

```bash
git add <file-name>
```

For example, to add a file named `index.py`, run:

```bash
git add index.py
```

To add all files in the current directory:

```bash
git add .
```

### Committing Changes

After adding files, you can commit them to the repository with a message describing the changes:

```bash
git commit -m "Initial commit"
```

This creates a snapshot of the files in your project and saves it in the Git history.

---

## Viewing Git Status

You can check the status of your Git repository at any time by running:

```bash
git status
```

This will show you which files are staged, which are modified, and which are untracked.

---

## Viewing Git History

To view the commit history for your repository, use the following command:

```bash
git log
```

This will display a list of commits along with their commit messages, author, and date.

---

## Git Branching

Git allows you to create branches to work on different parts of your project without affecting the main version. By default, a Git repository has a branch called `master`.

### Creating a New Branch

To create a new branch, use:

```bash
git branch <branch-name>
```

For example:

```bash
git branch feature-branch
```

### Switching Branches

To switch to a different branch, use:

```bash
git checkout <branch-name>
```

For example:

```bash
git checkout feature-branch
```

---

## Pushing Changes to a Remote Repository

You can push your changes to a remote Git repository (such as GitHub, GitLab, or Bitbucket) to store your project online and share it with others.

First, create a new repository on your remote service (e.g., GitHub), then connect your local Git repository to the remote repository:

```bash
git remote add origin <repository-url>
```

For example:

```bash
git remote add origin https://github.com/yourusername/yourrepo.git
```

To push your local changes to the remote repository:

```bash
git push -u origin master
```

---

## Key Takeaways

1. **Version Control**: Git allows you to track changes in your code and collaborate with others.
2. **Commit History**: You can view the commit history with `git log`.
3. **Branching**: Git allows you to work on different features in separate branches.
4. **Remote Repositories**: Push your local changes to a remote repository to share your work.

---

In the next lesson, we’ll explore how to create and use virtual environments in Python.
