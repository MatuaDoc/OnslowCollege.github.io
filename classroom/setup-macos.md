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
  - ```zsh
    brew install pyenv
    ```
  - ```zsh
    pyenv install 3.10:latest
    ```
  - ```zsh
    pyenv global 3.10:latest
    ```
  - ```zsh
    python3 -m pip install pytest
    ```

# 3. Set up Visual Studio Code

To edit your Python code, you will use Visual Studio Code. This is an integrated development environment that makes it easy to manage your Python files, test code, and get helpful suggestions when you're editing code.

## 3.1 Install Visual Studio Code

- If it is not open already, open Terminal (``/Applications/Terminal.app``)
- Copy and paste the following commands and press Enter after each:
  - ```zsh
    brew install --cask visual-studio-code
    ```
  - ```zsh
    code --install-extension OnslowCollege.onslow-college-dit-extensions
    ```
- Paste the command in to the Terminal
- Press Enter

## 3.5 Set up Settings Sync in Visual Studio Code

- Click on the ![Accounts](/img/account.svg) Accounts tab
- Click "Turn on Settings Sync"
![Settings Sync configuration](img/vscode04.png)
- Click to sign in with your Microsoft account
  - Use your school email address and password to log in
  - Do **NOT** use your personal email address

If you use Visual Studio Code on a different computer, you will be able to repeat this process on it to use the same settings for all your computers.
