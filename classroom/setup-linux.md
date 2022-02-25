---
title: Set up your programming environment
---

# 1. Set up dependencies

## 1.1 Install developer tools

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

# 2 Install Python

## 2.1 Install pyenv

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

## 2.2 Install Python

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

# 3. Set up Visual Studio Code

## 3.1 Install Visual Studio Code

- [Download Visual Studio Code](https://code.visualstudio.com)
  - Debian-based (Ubuntu, Mint, ChromeOS): download and install the ``.deb`` package
  - Fedora-based: download and install the ``.rpm`` package
-  Open the package and install it

## 3.2 Install the Visual Studio Code extensions

- If it not open already, open Terminal
- Copy the following command:
  - ```bash
    code --install-extension OnslowCollege.onslow-college-dit-extensions
    ```
- Paste the command in to the Terminal
- Press Enter

## 3.5 Set up Settings Sync in Visual Studio Code

- Open Visual Studio Code
- Click on the ![Accounts](/img/account.svg) Accounts tab
- Click "Turn on Settings Sync"
![Settings Sync configuration](img/vscode04.png)
- Click to sign in with your Microsoft account
  - Use your school email address and password to log in
  - Do **NOT** use your personal email address

If you use Visual Studio Code on a different computer, you will be able to repeat this process on it to use the same settings for all your computers.
