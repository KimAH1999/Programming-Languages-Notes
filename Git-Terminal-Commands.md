# Command Terms for PC

This document provides a list of essential commands for both Git and the terminal that are commonly used for version control and file management.

## Git Commands

- **`git init`**: Initialize a new Git repository.

- **`git add <file>`**: Stage changes for the next commit.
- **`git commit -m "message"`**: Commit the staged changes to the repository.
- **`git status`**: Show the current status of the working directory.
- **`git branch`**: List, create, or delete branches.
- **`git branch -M main`**: Rename the current branch to **main**.
- **`git checkout <branch>`**: Switch branches or restore working tree files.
- **`git config user.email`**: Check the email associated with the current Git user.
- **`git config --global user.name`**: Set the name for commits in Git.
- **`git config --list`**: Show the current Git configuration (email and name).
- **`git help commit`**: Display help information for the `git commit` command.

### How to Git Pull Example (Pull info from GitHub -> Folder)
- **`git pull <remote> <branch>`**: Fetch and merge changes from the remote repository.
  
**Steps Example:**

1. **Create a New Folder then upload New Folder to GitHub:**
   ```bash
   mkdir <folderName>
   ls                  #Verify that the folder was created.
   cd <folderName>     #Navigate into the folder you just created.
   pwd                 #Ensure you are in the correct directory.
   git init            #Set up a new Git repository in this folder.
   ls                  #Confirm that the Git repository has been initialized.
   git pull <copy/paste URL from Github>

### How to Git Clone Example (Clone GitHub -> Specific Folder)
- **`git clone <repository-url>`**: Clone an existing repository into a new directory.
  
**Steps Example:**

1. **Create Clone:**
   ```bash
   cd <copy/paste folder location>
   git clone <copy/paste URL from Github HTTPS located at <> Code dropdown>
   #OR
   go to folder, right click, "GitBash here"
   git clone <copy/paste URL from Github HTTPS located at <> Code dropdown>

### How to Push (VS -> GitHub)
- **`git push <remote> <branch>`**: Upload local repository content to a remote repository.

**Steps Example:**

1. **Push Visual Studio to GitHub**

   ```bash
   Open your project in VS Code.
   Click on the Source Control icon  on the sidebar or press Ctrl+Shift+G.
   Stage your changes.
   Commit your changes.
   Push your changes.

### Testing Steps

**Steps Example:**

1. **Install packages then test run JavaScript file**

   ```bash
   ls
   npm install          #Install npm packages
   npm fileName.js      #Run Javascript file

## Terminal Commands

- **`ls`**: List directory contents.
- **`mkdir <directory-name>`**: Create a new directory.
- **`cd <directory-name>`**: Change the current directory.
- **`touch <file-name>`**: Create an empty file or update the timestamp of an existing file.
- **`pwd`**: Print the current working directory.
- **`mv <source> <destination>`**: Move or rename files and directories.
- **`rm <file>`**: Remove files or directories.
- **`rm -rf <directory>`**: Forcefully remove directories and their contents.
- **`history`**: Show command history.
- **`cmd + k`**: Clear the terminal screen (on macOS).
- **`code <file>`**: Open Visual Studio Code from the terminal.

## Usage

You can refer to this document for quick access to essential commands while working with Git and managing files in the terminal.
