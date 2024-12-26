### Additional Steps for Connecting a Local Repository to GitHub

Assuming you created a local repo, do `git init` and perform all necessary edits or commits. Then follow these steps:

1. Create a new repository on GitHub.
2. Give your repository a name.
3. Do not initialize with a README.md file.
4. Create your repository.
5. Add the remote origin:
   ```bash
   git remote add origin <repository-link>
   ```
6. Verify the remote:
   ```bash
   git remote -v
   ```
7. Check the branch:
   ```bash
   git branch
   ```
8. Rename the master branch to main:
   ```bash
   git branch -M main
   ```
9. Push the repository to GitHub:
   ```bash
   git push -u origin main
   ```
   *(Then in the future, you will only need to type the following command to push changes:)*
   ```bash
   git push
   ```
10. Check all commits:
    ```bash
    git log
    ```
    *(Type `q` to quit the log view.)*

Now you can create a new file in your local directory, such as `README.md`. Edit and commit changes as needed.
   ```bash
   git push -u origin main
   ```
   *(Then in the future, you will only need to type the following command to push changes:)*
   ```bash
   git push