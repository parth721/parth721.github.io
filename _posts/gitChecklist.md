---
layout: post
title: Git Best practices
date: 2025-12-02 21:00:00 +0530
categories: jekyll tutorial
---

### Git (Version Control)

> Developed by Linus Torvalds to bring developers together and collaborate remotely.

---

### Best Practices

- **Don't commit secret or redundant files:**  
  Add files like `.env` and those listed in `.gitignore` to your ignore list so they are not accidentally uploaded.

---

#### Sync with Remote

1. **Fork the repository on GitHub**  
   _If you don’t own it or want to contribute to someone else’s project._
2. **Clone your fork or the repo:**  
   ```
   git clone <repo-url>
   ```
3. **(If forked) Set upstream remote for original repo:**  
   ```
   git remote add upstream <original-repo-url>
   ```
   _Allows you to easily sync your fork with the original repo._
4. **Pull latest changes:**  
   - Direct clone:  
     ```
     git pull origin main
     ```
   - If working from a fork and want updates from original:  
     ```
     git pull upstream main
     ```
5. **Create and switch to a new branch:**  
   ```
   git checkout -b <branch_name>
   ```
   _Work on a separate branch to keep features and fixes isolated._
6. **Stage your changes:**  
   ```
   git add .
   ```
   or  
   ```
   git add <file>
   ```
7. **Commit with a clear message:**  
   ```
   git commit -m "A concise, meaningful message"
   ```
8. **Push your branch to the remote repo:**  
   - For first push:  
     ```
     git push -u origin <branch_name>
     ```
   - For subsequent pushes:  
     ```
     git push
     ```

---

#### Daily Workflow

- **Check repo status:**  
  ```
  git status
  ```
- **See changes in files:**  
  ```
  git diff
  ```
- **View commit history:**  
  ```
  git log --oneline --graph --all
  ```
- **List branches:**  
  ```
  git branch
  ```
- **Create a new branch:**  
  ```
  git branch <branch-name>
  ```
- **Switch branch:**  
  ```
  git checkout <branch-name>
  ```
- **Delete a local branch:**  
  ```
  git branch -d <branch-name>
  ```

---

#### Merging, Rebasing, Tags

- **Merge a branch into the current branch:**  
  ```
  git merge <branch-name>
  ```
- **Rebase feature branch on main:**  
  ```
  git checkout <feature-branch>
  git rebase main
  ```
- **Resolve conflicts, then continue rebase:**  
  ```
  git rebase --continue
  ```
- **Create annotated tags:**  
  ```
  git tag -a v1.0.0 -m "release v1.0.0"
  ```
- **Push tags:**  
  ```
  git push origin --tags
  ```

---

#### Fixing/Cleaning Up

- **Amend last commit message:**  
  ```
  git commit --amend
  ```
- **Unstage a file:**  
  ```
  git restore --staged <file>
  ```
- **Discard local changes to a file:**  
  ```
  git restore <file>
  ```
- **Stash current changes:**  
  ```
  git stash
  ```
- **List stash:**  
  ```
  git stash list
  ```
- **Reapply latest stash & keep it:**  
  ```
  git stash apply
  ```
- **Reapply latest stash & drop it:**  
  ```
  git stash pop
  ```

---

### Explanations & Concepts

- **Fork vs. Clone:**  
  _Fork_ creates a copy of a repository on your GitHub account (useful for contributing to projects you don’t own).  
  _Clone_ downloads a repository from GitHub to your local computer.

- **Upstream Remote:**  
  Allows your local/forked repo to fetch new changes from the original (main) repository.

- **Branches:**  
  Helps you work on new features or bug fixes in isolation, keeping the main branch stable.

- **Staging & Committing:**  
  - _Staging (`git add`)_ selects changes to include in your next commit.
  - _Committing (`git commit`)_ saves those staged changes with a message describing what you did.

- **Pushing:**  
  Uploads your commits from your local machine to the remote GitHub repository.

- **Pulling:**  
  Downloads the latest changes from the remote repository to your local copy.

- **Merge:**  
  - **Meaning:** Combines changes from one branch into another (e.g., feature branch into `main`).
  - **Scenario:** When your new feature is ready, you merge it to main so everyone gets the updated code.

- **Rebase:**  
  - **Meaning:** Moves a sequence of commits to a new base commit, making history linear.
  - **Scenario:** Before merging a long-lived feature branch, rebase onto main to fetch latest updates and reduce conflicts.

- **Stash:**  
  - **Meaning:** Temporarily shelves changes you’ve made so you can work elsewhere and reapply them later.
  - **Scenario:** Need to switch branches but aren’t ready to commit? Stash your work, switch, then bring your changes back.

- **Reset:**  
  - **Meaning:** Moves your branch back to a previous commit. Can also remove changes based on options (`--soft`, `--hard`).
  - **Scenario:** Undo several commits, or revert to a previous state after mistakes.

- **Restore:**  
  - **Meaning:** Undo changes in your working directory or staging area (unstage or revert file).
  - **Scenario:** Revert uncommitted changes or unstage files before committing.

---

- [git playground](https://learngitbranching.js.org/)
- [ohmygit](https://ohmygit.org/)