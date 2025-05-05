# Windows Environment Setup Guide

This guide will walk you through setting up a complete development environment on Windows for software development. By the end, you'll have all the essential tools installed and configured.

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
2. Click on the Windows download button
3. Run the installer and follow the installation wizard
4. Launch VS Code after installation

### Recommended Extensions:

Install these extensions to enhance your development experience:

1. **Python** - For Python development
   - Click on the Extensions icon in the sidebar (or press `Ctrl+Shift+X`)
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

1. Download Git from the [official website](https://git-scm.com/download/win)
2. Run the installer with default options (you can customize if you're familiar with Git)
3. Open Command Prompt or PowerShell and verify installation:
   ```
   git --version
   ```

### Setting Up GitHub:

1. Create a [GitHub account](https://github.com/join) if you don't have one
2. Configure Git with your GitHub information:
   ```
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

### Setting Up SSH Authentication (Recommended):

1. Open Git Bash (installed with Git)
2. Generate an SSH key:
   ```
   ssh-keygen -t ed25519 -C "your.email@example.com"
   ```
3. Start the SSH agent:
   ```
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_ed25519
   ```
4. Copy your public key:
   ```
   cat ~/.ssh/id_ed25519.pub
   ```
5. Go to GitHub → Settings → SSH and GPG keys → New SSH key
6. Paste your key and save

## 3. Installing Python

Python is a versatile programming language used in web development, data science, and more.

### Installation Steps:

1. Download the latest Python installer from the [official website](https://www.python.org/downloads/windows/)
2. Run the installer
3. **Important**: Check "Add Python to PATH" before clicking Install
4. Click "Install Now"
5. Verify installation by opening Command Prompt and typing:
   ```
   python --version
   pip --version
   ```

### Setting Up Virtual Environments:

Virtual environments help manage dependencies for different projects.

1. Open Command Prompt and install virtualenv:
   ```
   pip install virtualenv
   ```
2. Create a new virtual environment:
   ```
   virtualenv venv
   ```
3. Activate the virtual environment:
   ```
   venv\Scripts\activate
   ```
4. When finished, deactivate:
   ```
   deactivate
   ```

## 4. Installing Node.js and npm

Node.js is a JavaScript runtime, and npm is a package manager for JavaScript.

### Installation Steps:

1. Download the LTS version from the [Node.js website](https://nodejs.org/)
2. Run the installer with default settings
3. Verify installation:
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
   python --version
   pip --version
   node --version
   npm --version
   ```

If all commands return version numbers, congratulations! Your development environment is set up correctly.

## Next Steps

Now that your environment is set up, proceed to the [Hello World](../../hello-world) project to write your first Python application.

## Troubleshooting

### Common Issues:

1. **Command not found errors**: Make sure the tool is properly added to your PATH. You might need to restart your computer after installation.

2. **Permission errors**: Try running Command Prompt or PowerShell as Administrator.

3. **VS Code extensions not working**: Make sure you have the correct version of the tool installed that the extension depends on.

If you encounter any issues not covered here, please check the official documentation for each tool or reach out to the Ecuacoders community for help.

---

Happy coding!
