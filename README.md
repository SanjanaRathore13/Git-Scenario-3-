## Scenario 3: Local Commit Not Visible on GitHub

### Question
You committed your code locally, but your team leader cannot see it on GitHub. What could be the reason, and how would you fix it?

### Situation
The code was committed successfully in the local Git repository, but the commit was not visible on GitHub.

### What I Did

1. Checked the local commit history using:
   `git log --oneline`

   This confirmed that the commit existed locally.

2. Checked whether the local repository was connected to a GitHub remote using:
   `git remote -v`

   There was no output, which showed that no remote repository was configured.

3. Created an empty GitHub repository named `Git-Scenario-3`.

4. Connected the local repository to the GitHub repository using:
   `git remote add origin <GitHub-Repository-URL>`

5. Pushed the local commit to GitHub using:
   `git push -u origin master`

6. Verified the GitHub repository and confirmed that the committed file and commit were visible there.

### Conclusion
The reason the team leader could not see the commit was that the commit existed only in the local Git repository and had not been pushed to GitHub.

### Proof / Evidence
- Local commit ID: `3c567ad`
- Commit message: `Commit file1 for Scenario 2`
- `git remote -v` initially returned no output.
- GitHub repository: `Git-Scenario-3`
- After `git push`, the commit became visible on GitHub.

### What I Learned
A local `git commit` saves changes in the local Git repository only. To make the commit available on GitHub, the local repository must have a remote configured and the commit must be pushed using `git push`.
