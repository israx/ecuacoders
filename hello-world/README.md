# Hello World in Python

Welcome to your first Python project! This guide will walk you through creating and running a simple "Hello World" application to verify that your Python environment is set up correctly.

## Prerequisites

Before starting, make sure you have:
- Completed the environment setup for your operating system ([Windows](../environment-setup/windows) or [Mac](../environment-setup/mac))
- Python installed and accessible from your terminal/command prompt
- Visual Studio Code (VS Code) installed

## Project Overview

In this project, you will:
1. Create a simple Python script
2. Run the script from the command line
3. Run the script from VS Code
4. Make a small modification to the script

## Step 1: Create Your First Python Script

1. Open VS Code
2. Create a new file by clicking File → New File (or press Ctrl+N on Windows, Cmd+N on Mac)
3. Save the file as `hello_world.py` in the hello-world directory (File → Save or Ctrl+S/Cmd+S)
4. Type the following code into the file:

```python
# My first Python program
print("Hello, World!")
print("Welcome to Ecuacoders!")
```

5. Save the file again (Ctrl+S/Cmd+S)

## Step 2: Run the Script from the Command Line

1. Open your terminal (Command Prompt or PowerShell on Windows, Terminal on Mac)
2. Navigate to the directory where you saved `hello_world.py`
3. Run the script with the following command:

   **Windows:**
   ```
   python hello_world.py
   ```

   **Mac:**
   ```
   python3 hello_world.py
   ```

4. You should see the following output:
   ```
   Hello, World!
   Welcome to Ecuacoders!
   ```

## Step 3: Run the Script from VS Code

1. Make sure your `hello_world.py` file is open in VS Code
2. Click on the "Run" button (the green triangle) in the top-right corner of the editor
   - Alternatively, right-click in the editor and select "Run Python File in Terminal"
   - Or use the keyboard shortcut (F5)
3. VS Code will open a terminal at the bottom of the window and run your script
4. You should see the same output as before

## Step 4: Modify Your Script

Let's make a small modification to see how changes affect the output:

1. Update your `hello_world.py` file to include the following code:

```python
# My first Python program
print("Hello, World!")
print("Welcome to Ecuacoders!")

# Get user input
name = input("What is your name? ")
print(f"Nice to meet you, {name}!")
```

2. Save the file
3. Run the script again using either method from Step 2 or Step 3
4. When prompted, enter your name and press Enter
5. You should see a personalized greeting

## Understanding the Code

Let's break down what each part of the code does:

- `# My first Python program` - This is a comment. Comments start with `#` and are ignored by Python when running the code. They're useful for adding notes to your code.

- `print("Hello, World!")` - The `print()` function displays text on the screen. The text inside the quotes is called a string.

- `name = input("What is your name? ")` - The `input()` function asks the user for input. The text inside the quotes is displayed as a prompt. The user's input is stored in the variable `name`.

- `print(f"Nice to meet you, {name}!")` - This is an f-string (formatted string). The `f` before the quotes allows us to include variables inside the string using curly braces `{}`.

## Next Steps

Congratulations on writing and running your first Python program! Here are some suggestions for what to try next:

1. Modify the program to ask for additional information (like age or favorite color)
2. Use conditional statements to make decisions based on user input
3. Create a simple calculator that performs basic operations
4. Explore Python's built-in functions and libraries

## Additional Resources

- [Official Python Documentation](https://docs.python.org/3/)
- [Python for Beginners](https://www.python.org/about/gettingstarted/)
- [W3Schools Python Tutorial](https://www.w3schools.com/python/)
- [Codecademy Python Course](https://www.codecademy.com/learn/learn-python-3)

---

Happy coding!
