# Github Classroom

Throughout the year, you will demonstrate your understanding of complex programming techniques such as object-oriented programming by completing Github Classroom assignments.


# 1. Create a school Github account

To participate in Github Classroom, you will need to create a school Github account by signing up with your school Microsoft account. You may already have received an invitation from your teacher to your school email account, so please check in [Outlook Online](https://office.com/outlook).

**Note: Do not use a personal Github account**. If you forget your login details or your account, you may not have any recourse and risk **failing your assessment**; by creating a school account, we may be able to help in case of a problem. If you wish to transfer your work to a personal account after you have submitted, you can fork it at the end of the year.


# 2. Accept your assignment

You can access your assignments by:

1. visiting [Github Classroom](https://classroom.github.com/) and finding the relevant assignment in the relevant class, or…
2. visit the assignment invitation link at the bottom of a lesson's ``.md`` file


# 3. Clone the assignment repository in Visual Studio Code

- [Using the Github Classroom extension](#using-the-github-classroom-extension)
- [Using ``git`` manually](#using-git-manually)

## Using the Github Classroom extension

In Visual Studio Code, make sure that you have the [Github Classroom](https://marketplace.visualstudio.com/items?itemName=GitHub.classroom) extension installed.

1. In the sidebar, click on the Github icon.
2. Your classes and accepted assignments show in the list at the top. If not, click on the Refresh button.
3. Click on the folder icon next to the assignment. Your repository will open automatically in the Explorer.

## Using ``git`` manually

1. Visit [Github.com](https://github.com/).
2. In the Repositories section at the left, click on the ``Onslow-College`` repository for your accepted assignment. For example: ``Onslow-College/13dtc-intro-to-oop-YourUserName``.
3. Click on the green **Code** button, then click on the clipboard icon to copy the repository URL.
4. In the sidebar, click on the Source Control icon (third icon down).
5. Click the **…** icon next to the Source Control heading then click **Clone**.
6. At the top of the screen, a command palette will ask you to provide a repository URL. Paste the repository URL you copied in step 3.
    - You may be required to log in to Github using your school account credentials.


# 4. Commit your work regularly

As you work on the code contained in the assignments, be sure to commit your code. This is a record of what you changed.

1. In the sidebar, click on the Source Control icon (third icon down).
2. Under the Changes list, click the + next to files that you have modified and whose changes you wish to preserve.
    - Only click on the files for which your commit message in step 3 will relate. For example, if your commit message is about fixing a particular
3. In the Message box, enter a short commit message that describes the changes you've made.
    - Commit messages start with a **subject**. This is a brief description of what changes you made. It is 50 characters or fewer and it does not end with a full-stop.
    - Add a blank line under the subject.
    - Any other comments you wish to make should be made here. Explain **what and why**, not **how**.
    - Example commit message:
        ```
        Fixed kumara total price calculation

        Previously, the kumara price was the item price multiplied by the quantity. I adjusted it to also account for GST.
        ```
4. When you have written your commit message, click on the tick icon.
5. Click on the **…** icon and click Push. Your code will be sent to Github.
