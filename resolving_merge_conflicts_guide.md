# Resolving Merge Conflicts in Git

An event that takes place when Git is unable to automatically resolve differences in code between two branches.

---

## Example Scenario

- **main branch**: In the 2nd line, you added `{button}`. After this, you add and commit the changes, then checkout to the feature branch.
- **feature1 branch**: In the 2nd line, you added `{dropdown}`. After this, you add and commit the changes.

---

## Steps to Resolve Conflicts

1. **Check the difference between the two branches**:
   ```bash
   git diff main  # Since we are in the feature1 branch and checking difference with main branch
   ```

2. **Merge the main branch into the feature branch**:
   ```bash
   git merge main # Since we are in the feature1 branch hence merging feature1 branch with main branch
   ```

3. **Handle conflicts in Visual Studio Code**:
   - **Accept Current Change**: Keep the changes from the feature1 branch.
   - **Accept Incoming Change**: Keep the changes from the main branch.
   - **Accept Both Changes**: Keep both changes if they are on different lines.

4. **Alternatively, resolve conflicts manually**:
   - Open the conflicting file(s).
   - Remove conflict markers (`====`, `>>>>`, `HEAD`).
   - Decide which changes to keep or merge.

5. **Save the file and proceed**:
   ```bash
   git status  # Check the status
   git add .   # Add the resolved file
   git commit -m "Resolve merge conflicts"  # Commit the changes
   ```

6. **Verify the resolution**:
   ```bash
   git diff main
   ```

7. **Switch to the main branch and complete the merge**:
   ```bash
   git checkout main
   git merge feature1
   git push
   ```

---

## Notes

- Resolving conflicts manually gives you complete control over the final changes.
- Always verify the resolved file(s) to ensure they meet your requirements.
- Use `git log` to review commit history and confirm successful conflict resolution.
