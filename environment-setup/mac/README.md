# Mac Environment Setup Guide

This guide will walk you through setting up a complete development environment on macOS for software development. By the end, you'll have all the essential tools installed and configured.

## Table of Contents
1. [Installing Visual Studio Code](#1-installing-visual-studio-code)
2. [Setting Up Git and GitHub](#2-setting-up-git-and-github)
3. [Installing Python](#3-installing-python)
4. [Installing Node.js and npm](#4-installing-nodejs-and-npm)
5. [Verifying Your Setup](#5-verifying-your-setup)

## 1. Installing Visual Studio Code

Visual Studio Code (VS Code) is a lightweight but powerful source code editor.

### Installation Steps:

1. Visit the [VS Code download page](https://code.visualstudio.com/download)
2. Click on the Mac download button
3. Open the downloaded .dmg file
4. Drag VS Code to the Applications folder
5. Launch VS Code from your Applications folder or Spotlight (Cmd+Space)

### Recommended Extensions:

Install these extensions to enhance your development experience:

1. **Python** - For Python development
   - Click on the Extensions icon in the sidebar (or press `Cmd+Shift+X`)
   - Search for "Python"
   - Click "Install" on the extension by Microsoft

2. **Live Server** - For web development
   - Search for "Live Server"
   - Install the extension by Ritwick Dey

3. **ESLint** - For JavaScript linting
   - Search for "ESLint"
   - Install the extension by Microsoft

4. **Git Lens** - For enhanced Git capabilities
   - Search for "GitLens"
   - Install the extension by GitKraken

## 2. Setting Up Git and GitHub

Git is a version control system that helps you track changes in your code.

### Installing Git:

macOS might already have Git installed. To check, open Terminal and type:
```
git --version
```

If Git is not installed, you'll be prompted to install it. Alternatively, you can install it using Homebrew:

1. Install Homebrew (if not already installed):
   ```
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. Install Git using Homebrew:
   ```
   brew install git
   ```

### Setting Up GitHub:

1. Create a [GitHub account](https://github.com/join) if you don't have one
2. Configure Git with your GitHub information:
   ```
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

### Setting Up SSH Authentication (Recommended):

1. Open Terminal
2. Generate an SSH key:
   ```
   ssh-keygen -t ed25519 -C "your.email@example.com"
   ```
3. Start the SSH agent:
   ```
   eval "$(ssh-agent -s)"
   ```
4. Create or edit ~/.ssh/config file:
   ```
   touch ~/.ssh/config
   ```
5. Add the following to the config file:
   ```
   Host github.com
     AddKeysToAgent yes
     UseKeychain yes
     IdentityFile ~/.ssh/id_ed25519
   ```
6. Add your SSH key to the agent:
   ```
   ssh-add -K ~/.ssh/id_ed25519
   ```
7. Copy your public key:
   ```
   pbcopy < ~/.ssh/id_ed25519.pub
   ```
8. Go to GitHub → Settings → SSH and GPG keys → New SSH key
9. Paste your key and save

## 3. Installing Python

macOS comes with Python pre-installed, but it's recommended to install a newer version.

### Installation Steps:

1. Install Homebrew (if not already installed):
   ```
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. Install Python using Homebrew:
   ```
   brew install python
   ```

3. Verify installation:
   ```
   python3 --version
   pip3 --version
   ```

### Setting Up Virtual Environments:

Virtual environments help manage dependencies for different projects.

1. Install virtualenv:
   ```
   pip3 install virtualenv
   ```

2. Create a new virtual environment:
   ```
   virtualenv venv
   ```

3. Activate the virtual environment:
   ```
   source venv/bin/activate
   ```

4. When finished, deactivate:
   ```
   deactivate
   ```

## 4. Installing Node.js and npm

Node.js is a JavaScript runtime, and npm is a package manager for JavaScript.

### Installation Steps:

1. Install Node.js using Homebrew:
   ```
   brew install node
   ```

2. Verify installation:
   ```
   node --version
   npm --version
   ```

### Basic npm Commands:

- Initialize a new project:
  ```
  npm init
  ```
- Install a package:
  ```
  npm install package-name
  ```
- Install a package globally:
  ```
  npm install -g package-name
  ```

## 5. Verifying Your Setup

Let's make sure everything is working correctly:

1. Open VS Code
2. Open the integrated terminal (View → Terminal or `Ctrl+` `)
3. Check all tool versions:
   ```
   git --version
   python3 --version
   pip3 --version
   node --version
   npm --version
   ```

If all commands return version numbers, congratulations! Your development environment is set up correctly.

## Next Steps

Now that your environment is set up, proceed to the [Hello World](../../hello-world) project to write your first Python application.

## Troubleshooting

### Common Issues:

1. **Command not found errors**: Make sure the tool is properly added to your PATH. You might need to restart your terminal after installation.

2. **Permission errors**: You might need to use `sudo` for some commands, or fix permissions on certain directories.

3. **Homebrew issues**: If Homebrew commands fail, try running `brew doctor` to diagnose and fix problems.

4. **Python version conflicts**: macOS comes with Python 2.7 pre-installed. Make sure you're using `python3` and `pip3` commands to use the newer version.

If you encounter any issues not covered here, please check the official documentation for each tool or reach out to the Ecuacoders community for help.

---

Happy coding!
