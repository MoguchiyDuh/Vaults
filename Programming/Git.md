---
tags:
  - programming
  - git
related:
  - '[[00 - Programming MOC]]'
---
## Core Concepts
- **Repository**: Project folder tracked by Git
- **Commit**: Snapshot of changes
- **Branch**: Independent line of development
- **Remote**: Cloud repository (GitHub, GitLab, etc.)

---
### Local Setup
```bash
git init                    # Initialize new repo
git clone <url>             # Clone existing repo
git config --global user.name "name"
git config --global user.email "email"
```

---
## Basic Workflow
```bash
git status                 # Check changes
git add <file>             # Stage specific file
git add .                  # Stage all changes
git commit -m "message"    # Commit staged changes
git commit --amend         # Edit the last commit
git commit -a              # Stage files and commit at the same time
git log --oneline --graph  # View commit history
```

---
## Branch Management
```bash
git branch                  # List branches
git branch <name>          # Create new branch
git checkout <branch>      # Switch branch
git checkout -b <branch>   # Create and switch
git merge <branch>         # Merge branch into current**
```

---
## Remote Operations
```bash
git remote add origin <url>    # Add remote
git push -u origin master      # First push
git push                       # Push changes
git pull                       # Fetch and merge
git fetch                      # Download without merge
```

---
## Advance
```bash
git diff                    # See unstaged changes
git stash                   # Temporary save changes
git rebase -i HEAD~3        # Interactive rebase
```

---
## Revert, reset
```bash
git reset --hard HEAD       # Discard all changes, replace/delete current files
git reset --soft HEAD       # Discard all changes, keep current files
git restore <file>          # Discard unstaged changes
git revert <commit>         # Safe undo (new commit)
```

---
## Cherry-pick
```bash
git cherry-pick <commit-hash>          # Pick single commit
git cherry-pick <hash1> <hash2>        # Pick multiple commits
git cherry-pick <start-hash>^..<end-hash>  # Pick range
```

---

## See Also
- [[00 - Programming MOC]] - Programming overview
