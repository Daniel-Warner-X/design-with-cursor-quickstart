# Development Environment Setup for Designers (Mac)

This guide will help you set up a basic development environment for managing your Cursor project using Git on macOS. It is tailored for designers who are new to coding workflows.

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

### e. Connect to GitHub (Optional)
If you want to back up your code or collaborate, create a repository on [GitHub](https://github.com/) and follow their instructions to connect your local project.

Example:
```
git remote add origin https://github.com/yourusername/your-repo.git
git push -u origin main
```

## 5. Common Commands
- `git pull` — Get the latest changes from GitHub
- `git push` — Upload your changes to GitHub
- `git log` — View commit history

## 6. Resources
- [GitHub Docs: Set up Git](https://docs.github.com/en/get-started/quickstart/set-up-git)
- [Atlassian Git Tutorials](https://www.atlassian.com/git/tutorials)

---

**Tip:** Commit your work often and push to GitHub regularly to keep your project safe and share progress with your team.
