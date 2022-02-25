---
title: Set up your programming environment
---

# 1. Set up dependencies

## 1.1 Install command-line tools

You will require Apple's command-line tools installed. There are two options:

1. Install [Xcode](https://apps.apple.com/nz/app/xcode/id497799835?mt=12) from the App Store, **OR**
2. Install *just* the command-line tools using the following instructions:

- Open Terminal (``/Applications/Terminal.app``)
- Copy the following command:
  - ```zsh
    xcode-select --install
    ```
- Paste the command in to the Terminal
- Press Enter
- Click to install the command-line tools
- Wait until they have finished installing before you continue

## 1.2 Install Homebrew

- If it is not open already, open Terminal (``/Applications/Terminal.app``)
- Copy the following command:
  - ```zsh
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
- Paste the command in to the Terminal
- Press Enter

# 2. Install Python

## 2.1 Install Python 3.10

- If it is not open already, open Terminal (``/Applications/Terminal.app``)
- Copy and paste the following commands into the Terminal then press Enter. 
  - ```bash
    brew install pyenv
    ```
  - ```bash
    pyenv install 3.10:latest
    ```
  - ```
    pyenv global 3.10:latest
    ```

# 3. Set up Visual Studio Code

To edit your Python code, you will use Visual Studio Code. This is an integrated development environment that makes it easy to manage your Python files, test code, and get helpful suggestions when you're editing code.

## 3.1 Install Visual Studio Code

- If it is not open already, open Terminal (``/Applications/Terminal.app``)
- Copy the following command:
  - ```zsh
    brew install --cask visual-studio-code
    ```
- Paste the command in to the Terminal
- Press Enter

## 3.2 Set up extensions for Visual Studio Code

- Open Visual Studio Code (``/Applications/Visual Studio Code.app``)
  - When you first open it, you will see a window like this:
  - ![First-run screen for Visual Studio Code](img/vscode01.png)
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
  - Click on the option for Python 3.10.2
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
