# Git

This page follows the class handout **Version Control Tools: Git and GitHub** (Prof. Neeta Nain, MNIT Jaipur, 12 October 2026).

## 1. Version control
Version control records changes to files over time. It helps track history, compare versions, and collaborate.

## 2. Git and GitHub
- **Git** is a distributed version control system.
- **GitHub** is a hosting and collaboration platform for Git repositories.

## 3. Install and verify on macOS
```bash
brew install git
git --version
```

## 4. Configure Git
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global --list
```

## 5. Create a repository
```bash
mkdir my-project
cd my-project
git init
```

## 6. Basic workflow
Git uses a working directory, staging area, and repository:
```bash
git status
git add filename
git add .
git commit -m "Add project files"
```

## 7. History and differences
```bash
git log
git log --oneline
git diff
git diff --staged
git diff HEAD
git ls-files
```

## 8. Ignore files
Create `.gitignore` and list patterns Git should ignore:
```gitignore
.DS_Store
*.log
build/
```

## 9. Move and remove
```bash
git mv old.py new.py
git rm filename
```

## 10. Restore and revert
```bash
git restore --staged filename
git restore filename
git revert COMMIT_ID
```
`git restore --staged` unstages a file. `git restore filename` discards unstaged changes in that file. `git revert` creates a new commit that reverses a selected commit's changes. Check the target before discarding work.

## 11. Connect to GitHub
Create an empty GitHub repository, then:
```bash
git remote add origin REPOSITORY_URL
git remote -v
git branch -M main
git push -u origin main
```

## 12. Clone, fetch, and pull
```bash
git clone REPOSITORY_URL
git fetch origin
git pull
```
`clone` creates a local copy; `fetch` downloads remote updates without integrating them into the current branch; `pull` fetches and integrates remote updates.

## 13. Branches
```bash
git branch
git branch feature-login
git switch feature-login
git switch main
git switch -c feature-login
```
A branch provides a separate line of development.

## 14. Merge and rebase
```bash
git merge feature-login
git rebase main
```
Merge integrates another branch into the current branch. Rebase reapplies commits on top of another base commit.

## 15. Tags
```bash
git tag
git tag -a v1.0.0 -m "Version 1.0.0"
git show v1.0.0
git push origin v1.0.0
```

## 16. GitHub collaboration terms
- **Pull request**: proposes changes for review and merging.
- **Fork**: creates your own GitHub-side copy of another repository.
- **Issue**: tracks a bug, task, or discussion.
- **Project**: organizes work.
- **Release**: publishes a named version.

## 17. Quick command practice
Run in a disposable folder:
```bash
mkdir git-practice
cd git-practice
git init
echo "First line" > notes.txt
git status
git add notes.txt
git commit -m "Add notes"
echo "Second line" >> notes.txt
git diff
git add notes.txt
git diff --staged
git commit -m "Update notes"
git log --oneline
```

The class handout also covers merge conflicts, pull requests, forks, tags, releases, issues, projects, common errors, and security/best practices. Some commands require a configured remote and authentication.
