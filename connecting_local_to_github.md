# Connecting a Local Repository to GitHub

Assuming you created a local repository, initialized it with `git init`, and performed all necessary edits or commits, follow these steps:

## Steps

1. **Create a new repository on GitHub:**
   - Go to your GitHub account.
   - Click on "New" to create a repository.
   - Give your repository a name.
   - Do not initialize with a README.md file.
   - Click "Create repository."

2. **Add the remote origin:**
   ```bash
   git remote add origin <repository-link>
   ```

3. **Verify the remote:**
   ```bash
   git remote -v
   ```

4. **Check the branch:**
   ```bash
   git branch
   ```

5. **Rename the `master` branch to `main`:**
   ```bash
   git branch -M main
   ```

6. **Check the status of your repository:**
   ```bash
   git status
   ```

7. **Stage your changes:**
   ```bash
   git add <file-name>
   git add . # To stage multiple files
   ```

8. **Commit your changes:**
   ```bash
   git commit -m "Add a meaningful commit message"
   ```

9. **Push the repository to GitHub:**
   ```bash
   git push -u origin main
   ```
   *(For future pushes, you only need to run the following command:)*  
   ```bash
   git push
   ```

10. **Check all commits:**
    ```bash
    git log
    ```
    *(Type `q` to quit the log view.)*

---

**Happy Coding!**