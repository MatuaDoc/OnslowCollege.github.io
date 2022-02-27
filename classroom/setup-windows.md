---
title: Set up your programming environment
---

# 1. Fast install

<iframe width="100%" height="315" src="https://www.youtube.com/embed/5l0Q8hOMRU4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- Open Windows PowerShell
- Copy the following block of commands
  - ```ps
    Set-ExecutionPolicy RemoteSigned -scope CurrentUser -Force
    iwr -useb get.scoop.sh | iex

    scoop install git python
    python3 -m pip install pytest

    scoop bucket add extras
    scoop install vscode

    code --install-extension OnslowCollege.onslow-college-dit-extensions
    
    code
    echo Done
    ```
- After copying, right-click on the PowerShell window to paste it
- Press Enter, then wait for Visual Studio Code to open

# 2. Step-by-step install

## 2.1 Install Scoop

- Open Windows PowerShell
- Copy the following commands. After copying each command, right-click on the PowerShell window to paste it then press Enter. 
  - ```ps
    Set-ExecutionPolicy RemoteSigned -scope CurrentUser -Force
    ```
  - ```ps
    iwr -useb get.scoop.sh | iex
    ```

## 2.2 Install git and python

- If it is not open already, open Windows PowerShell
- Copy the following commands. After copying each command, right-click on the PowerShell window to paste it then press Enter:
  - ```ps
    scoop install git python
    ```
  - ```ps
    python3 -m pip install pytest
    ```

## 2.3 Install Visual Studio Code

- If it is not open already, open Windows PowerShell
- Copy the following commands. After copying each command, right-click on the PowerShell window to paste it then press Enter. 
  - ```ps
    scoop bucket add extras
    ```
  - ```ps
    scoop install vscode
    ```
  - ```ps
    code --install-extension OnslowCollege.onslow-college-dit-extensions
    ```

## 2.4 Set up Settings Sync in Visual Studio Code

- Open Visual Studio Code
- Click on the ![Accounts](/img/account.svg) Accounts tab
- Click "Turn on Settings Sync"
![Settings Sync configuration](img/vscode04.png)
- Click to sign in with your Microsoft account
  - Use your school email address and password to log in
  - Do **NOT** use your personal email address

If you use Visual Studio Code on a different computer, you will be able to repeat this process on it to use the same settings for all your computers.
