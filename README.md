# Git & GitHub Basics for Beginners

A comprehensive guide to understanding and working with Git and GitHub for version control and collaboration. This document covers everything from setting up Git to advanced operations like branching, merging, and resolving conflicts.

---

## Table of Contents
1. [Creating a Repository on GitHub](#1-creating-a-repository-on-github)
2. [Setting Up Git](#2-setting-up-git)
3. [Cloning and Managing Repositories](#3-cloning-and-managing-repositories)
4. [Staging, Committing, and Pushing Changes](#4-staging-committing-and-pushing-changes)
5. [Initializing a Local Repository](#5-initializing-a-local-repository)
6. [Working with Branches](#6-working-with-branches)
7. [Merging Branches](#7-merging-branches)
8. [Resolving Merge Conflicts](#8-resolving-merge-conflicts)
9. [Undoing Changes](#9-undoing-changes)
10. [Forking Repositories](#10-forking-repositories)
11. [Acknowledgments](#11-acknowledgments)

---

## 1. Creating a Repository on GitHub 

1. Log in to your GitHub account and click on the **New** button to create a new repository.
2. Enter a repository name.
3. Add an optional description.
4. Choose to make the repository public or private. Public repositories are visible to everyone, while private ones are only accessible to collaborators.
5. Optionally initialize the repository with a **README.md** file for documentation.
6. Click **Create Repository**.

---

## 2. Setting Up Git

1. Install the following software based on your operating system:
   - **Windows**: [Git Bash](https://git-scm.com/)
   - **Mac**: Terminal
   - **Code Editor**: [Visual Studio Code](https://code.visualstudio.com/)

2. Verify Git installation:
   ```bash
   git --version
   ```

3. Configure Git:
   a. Set up your username and email:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your.email@example.com"
   ```

   b. Review your configuration:
   ```bash
   git config --list
   ```

---

## 3. Cloning and Managing Repositories

1. Cloning a Repository:
   a. Navigate to your GitHub repository.
   b. Click the **Code** button and copy the HTTPS link.
   c. Open a terminal in Visual Studio Code and run:
   ```bash
   git clone <repository-link>
   ```
   d. A folder containing the repository files will be created.
   e. To check the status run:
   ```bash
   git status
   ```

2. Basic Git Commands:

   - **Navigate to a folder:**
     ```bash
     cd foldername
     ```

   - **Create a new directory:**
     ```bash
     mkdir new-folder-name
     ```

   - **Check status:**
     ```bash
     git status
     ```

   - **List files:**
     ```bash
     ls
     ```

   - **Check hidden files to identify configuration or system files:**
     ```bash
     ls -a
     ```

---

## 4. Staging, Committing, and Pushing Changes

### File Status Types

- **Untracked (U):** New files not yet tracked by Git.
- **Modified (M):** Files with changes not yet staged.
- **Staged (A):** Files added to the staging area, ready for commit.
- **Committed:** Files with recorded changes.

### Commands

1. **Add Files to Staging Area:**
   ```bash
   git add <file-name>
   git add .  # Adds all files
   ```

2. **Commit Changes:**
   ```bash
   git commit -m "Commit message"
   ```

3. **Push Changes to GitHub:**
   ```bash
   git push origin main # Authorize VS code to push the changes on Github
   ```

### Conclusion: Basic Workflow

The basic Git workflow involves the following steps:

1. **GitHub Repository**
   - Start with a repository on GitHub.

2. **Clone**
   - Clone the repository to your local machine.

3. **Make Changes**
   - Make changes to the files in your local repository.

4. **Add**
   - Stage the changes using `git add`.

5. **Commit**
   - Commit the changes with a descriptive message using `git commit`.

6. **Push**
   - Push the changes to the remote repository on GitHub.

---

## 5. Initializing a Local Repository

### Steps to Start a New Project Locally

1. **Initialize a Git repository:**
   ```bash
   git init # Add .git in a new repository if not present already
   ```

2. **Add a remote origin:**
   ```bash
   git remote add origin <repository-link>
   ```

3. **Verify the remote:**
   ```bash
   git remote -v
   ```

4. **Rename the default branch to "main":**
   ```bash
   git branch -M main
   ```

5. **Push the local repository to GitHub:**
   ```bash
   git push -u origin main
   ```
   *(If you use above code, from next time onwards, you will only need to type the following command to push changes:)*
   ```bash
   git push
   ```
6. **Check all commits:**
    ```bash
    git log
    ```
    *(Type `q` to quit the log view.)*

---

## 6. Working with Branches

### Branch Commands

1. **Check current branch:**
   ```bash
   git branch #Also to check all the branches
   ```

2. **Create a new branch:**
   ```bash
   git checkout -b branch-name
   ```

3. **Switch branches:**
   ```bash
   git checkout branch-name
   ```

4. **Delete a branch:**
   ```bash
   git branch -d branch-name
   ```

5. **Push branch changes:**
   ```bash
   git push origin branch-name
   ```
---

## 7. Merging Branches

1. **compare commits, branches, files & more:**
   *(if you are on feature1 branch want to compare it with main branch then type: git diff main)*
   ```bash
   git diff branch-name 
   ```

2. **To merge a branch into main branch:**
    *(if you are on feature1 branch want to merge it with main branch then type: git merge main)*
  ```bash
  git merge branch-name
  ```

### Pull Requests

1. On GitHub, click **Compare & Pull Request**
2. Add a description of your changes.
3. Submit the pull request.
4. After review, click **Merge Pull Request**

---

## 8. Resolving Merge Conflicts

Merge conflicts occur when Git cannot automatically reconcile changes. Use the following steps in Visual Studio Code:

1. Accept the current change (your changes), incoming change (changes from the other branch), or both.
2. Edit the file to resolve conflicts manually - remove unnecessary lines and keep the ones needed.
3. Save the file, check status, then:
   ```bash
   git add .
   git commit -m "Resolve merge conflicts"
   ```
---

## 9. Undoing Changes

#### Undo Staged Changes
```bash
git reset <file-name>
```
*(for multiple file names type:)*
```bash
git reset
```

#### Undo Last Commit
```bash
git reset HEAD~1
```

#### Reset to a Specific Commit
```bash
git reset <commit-hash> # each commit has its own specific hash you need to copy hash for that commit , to find hash type git log
```

#### To remove any changes:
```bash
git reset --hard <commit-hash>
```

---

## 10. Forking Repositories

Forking creates a copy of a repository in your GitHub account.

### Steps to Fork

1. Click the **Fork** button.
2. Choose a name for the fork.
3. Select branches to include (optional).
4. Click **Create Fork**.
5. Use a pull request to propose changes to the original repository.

---

## 11. Acknowledgments
This guide was inspired by the video "[Complete Git and GitHub Tutorial for Beginners](https://www.youtube.com/watch?v=Ez8F0nW6S-w)" by [Apna College - Author (Shraddha Khapra)](https://www.youtube.com/@ApnaCollegeOfficial). Check out their channel for more amazing content!