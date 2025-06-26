# Development Environment Setup for Designers (Mac)

This guide will help you set up a basic development environment for managing your Cursor project using Git on macOS. It is tailored for designers who are new to coding workflows.

If you prefer to use a graphical user interface, [GitHub Desktop](https://github.com/apps/desktop) is also available.

## 1. Install Homebrew (Recommended)
Homebrew is a package manager for macOS that makes it easy to install software.

Open the Terminal app and run:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 2. Install Git
After installing Homebrew, install Git by running:

```
brew install git
```

To verify Git is installed, run:

```
git --version
```

## 3. Configure Git
Set your name and email (used for your commits):

```
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

## 4. Basic Git Workflow

### a. Initialize a Repository
If your project is not already a Git repository, run:

```
git init
```

### b. Check Status
See which files have changed:

```
git status
```

### c. Add Files
Add all changes to be tracked:

```
git add .
```

### d. Commit Changes
Save your changes with a message:

```
git commit -m "Describe your change"
```

## 5. Using git

[Git Tutorial for Beginners](https://www.youtube.com/watch?v=CvUiKWv2-C0)
[GitHub Desktop for Beginners](https://www.youtube.com/watch?v=8Dd7KRpKeaE)

**Common Commands**

- `git status` — Check the status of your working directory
- `git pull` — Get the latest changes from GitHub
- `git push` — Upload your changes to GitHub
- `git checkout -b <branch-name>` — Create a new branch
- `git checkout <branch-name>` — Switch to a different branch
