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
- Copy the following commands. After copying each command, right-click on the PowerShell window to paste it then press Enter:
  - ```ps
    scoop install git python
    ```
  - ```ps
    python3 -m pip install pytest
    ```

# 2. Set up Visual Studio Code

## 2.1 Install Visual Studio Code

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

## 2.2 Set up Settings Sync in Visual Studio Code

- Open Visual Studio Code
- Click on the ![Accounts](/img/account.svg) Accounts tab
- Click "Turn on Settings Sync"
![Settings Sync configuration](img/vscode04.png)
- Click to sign in with your Microsoft account
  - Use your school email address and password to log in
  - Do **NOT** use your personal email address

If you use Visual Studio Code on a different computer, you will be able to repeat this process on it to use the same settings for all your computers.