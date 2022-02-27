---
title: Set up your programming environment
---

# 1. Fast install

- Open Terminal
- Copy the following block of commands
  - Debian, Ubuntu, Mint, ChromeOS
    - ```bash
      sudo apt install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev git
      
      git clone https://github.com/pyenv/pyenv.git ~/.pyenv
      echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
      echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
      echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.bashrc
      ~/.pyenv install 3.10:latest
      ~/.pyenv global 3.10:latest
      pip -m install pytest

      wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
      sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
      sudo apt update
      sudo apt install code

      code --install-extension OnslowCollege.onslow-college-dit-extensions
      code
      echo "Done"
      ```
- Paste the commands into Terminal
- Press Enter, then wait for Visual Studio Code to open

# 2. Step-by-step instructions

## 2.1 Install developer tools

- Open Terminal
- Copy and paste the following commands (dependant on your distribution) and press Enter after each:
  - Ubuntu, Debian, ChromeOS with Linux Beta
    - ```bash
      sudo apt install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev git
      ```
  - Fedora, RedHat
    - ```bash
      sudo dnf groupinstall "Development Tools" -y
      ```
    - ```bash
      sudo dnf install zlib-devel bzip2 bzip2-devel readline-devel sqlite sqlite-devel openssl-devel xz xz-devel libffi-devel findutils -y
      ```

## 2.2 Install pyenv

- If it is not open already, open Terminal
- Copy and paste the following commands and press Enter after each:
  - ```bash
    git clone https://github.com/pyenv/pyenv.git ~/.pyenv
    ```
  - ```bash
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
    ```
  - ```bash
    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
    ```
  - ```bash
    echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.bashrc
    ```
  - ```bash
    exec "$SHELL"
    ```

## 2.3 Install Python

- If it is not open already, open Terminal
- Copy and paste the following commands and press Enter after each:
  - ```bash
    pyenv install 3.10:latest
    ```
  - ```bash
    pyenv global 3.10:latest
    ```
  - ```bash
    python3 -m pip install pytest
    ```

## 2.4 Install Visual Studio Code

- [Download Visual Studio Code](https://code.visualstudio.com)
  - Debian-based (Ubuntu, Mint, ChromeOS): download and install the ``.deb`` package
  - Fedora-based: download and install the ``.rpm`` package
-  Open the package and install it

## 2.5 Install the Visual Studio Code extensions

- If it not open already, open Terminal
- Copy the following command:
  - ```bash
    code --install-extension OnslowCollege.onslow-college-dit-extensions
    ```
- Paste the command in to the Terminal
- Press Enter

## 2.6 Set up Settings Sync in Visual Studio Code

- Open Visual Studio Code
- Click on the ![Accounts](/img/account.svg) Accounts tab
- Click "Turn on Settings Sync"
![Settings Sync configuration](img/vscode04.png)
- Click to sign in with your Microsoft account
  - Use your school email address and password to log in
  - Do **NOT** use your personal email address

If you use Visual Studio Code on a different computer, you will be able to repeat this process on it to use the same settings for all your computers.
