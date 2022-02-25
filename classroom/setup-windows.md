---
title: Set up your programming environment
---

# 1. Set up dependencies

## 1.1 Install Scoop

- Open Windows PowerShell
- Copy the following commands. After copying each command, right-click on the PowerShell window to paste it then press Enter. 
  - ```ps
    Set-ExecutionPolicy RemoteSigned -scope CurrentUser
    ```
  - ```ps
    iwr -useb get.scoop.sh | iex
    ```

## 1.2 Install git and python

- If it is not open already, open Windows PowerShell
- Copy the following command:
  - ```ps
    scoop install git python
    ```
- Right-click on the PowerShell window to paste the command
- Press Enter

# 2. Set up Visual Studio Code

To edit your Python code, you will use Visual Studio Code. This is an integrated development environment that makes it easy to manage your Python files, test code, and get helpful suggestions when you're editing code.

## 2.1 Install Visual Studio Code

- If it is not open already, open Windows PowerShell
- Copy the following commands. After copying each command, right-click on the PowerShell window to paste it then press Enter. 
  - ```ps
    scoop bucket add extras
    ```
  - ```ps
    scoop install vscode
    ```
 
When you first open it, you will see a window like this:

![First-run screen for Visual Studio Code](img/vscode01.png)

## 2.2 Set up extensions for Visual Studio Code

- Open Visual Studio Code
- Click on the ![Extensions](/img/extensions.svg) Extensions tab
- Search for "Onslow College DIT Extensions", then click Install
 
This will download and install the following extensions:
- **Python** (by Microsoft)
  - Adds support for the Python language.
- **Pylance** (by Microsoft)
  - Improved Python language support.
- **Pip Manager** (by slightc)
  - Download Python packages from Visual Studio Code.
- **GitLens** (by GitKraken)
  - Improved Git integration.
- **GitHub Classroom** (by GitHub)
  - Integrated access to GitHub Classroom exercises.
- **Error Lens** (by Alexander)
  - Shows the line where coding errors are occurring as well as a hint on how to fix it
- **indent-rainbow** (by oderwat)
  - Shows your current indentation level using colours
- **Markdown All in One** (by Yu Zhang)
  - Preview Markdown documents in Visual Studio Code while you write them.

## 3.3 Set up Visual Studio Code to use Python 3.10.2

- Click ``View menu → Command Palette…`` or press Ctrl-Shift-P to show the Command Palette.
  - A text box will show at the top of the screen. 
  - Type "select interpreter". You will see an option called "Python: Select Interpreter" in the menu. Click on it.
    - ![Command palette](img/vscode02.png)
  - Click on the option for the latest Python that you installed earlier
    - The path should contain ``scoop``
    - ![Python interpreter selection](img/vscode03.png)

## 3.4 Set up Pytest

- After you have installed the Pip Manager extension, click on the Pip Manager icon on the left (it looks like a book or three stacked sheets of paper)
- Click the ![Add](/img/add.svg) Add button at the top
- In the Command Palette, type ``pytest`` and press Enter

## 3.5 Set up Settings Sync in Visual Studio Code

- Click on the ![Accounts](/img/account.svg) Accounts tab
- Click "Turn on Settings Sync"
![Settings Sync configuration](img/vscode04.png)
- Click to sign in with your Microsoft account
  - Use your school email address and password to log in
  - Do **NOT** use your personal email address

If you use Visual Studio Code on a different computer, you will be able to repeat this process on it to use the same settings for all your computers.
