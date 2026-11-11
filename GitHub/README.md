# GitHub

## What is GitHub?
GitHub is an online platform for hosting Git repositories and collaborating on software projects.

## Create a repository
1. Sign in at https://github.com/.
2. Select **New repository**.
3. Enter a repository name and optional description.
4. Choose Public or Private.
5. Select **Create repository**.

## Push a local repository
Replace `REPOSITORY_URL` with the URL shown on GitHub:
```bash
git remote add origin REPOSITORY_URL
git remote -v
git branch -M main
git push -u origin main
```

## Clone
```bash
git clone REPOSITORY_URL
```
Cloning downloads a repository and its history to your computer.

## Synchronize changes
```bash
git fetch origin
git pull
git push
```
- `fetch`: downloads remote information.
- `pull`: fetches and integrates remote changes.
- `push`: uploads local commits to the remote repository.

## Branches and pull requests
1. Create a branch for a change.
2. Make and commit the change.
3. Push the branch to GitHub.
4. Open a pull request.
5. Review the proposed changes.
6. Merge when approved.

Example:
```bash
git switch -c feature-update
# edit files
git add .
git commit -m "Update documentation"
git push -u origin feature-update
```

## Fork vs clone
- **Fork** creates a separate GitHub-side copy under your account.
- **Clone** copies a repository to your local computer.

## Issues, projects, tags, and releases
- **Issues** track bugs, tasks, and discussions.
- **Projects** organize and track work.
- **Tags** mark points in Git history.
- **Releases** package and describe a version.

## Best practices
- Write a useful `README.md`.
- Use meaningful commit messages.
- Never upload passwords, API keys, or private credentials.
- Use `.gitignore` for local-only or generated files where appropriate.
- Review changes before committing and pushing.
- Use branches and pull requests for collaboration.

> GitHub's interface can change; follow the current website and your instructor's instructions.
