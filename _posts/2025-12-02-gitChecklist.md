---
layout: post
title: Git Best practices
date: 2025-12-02 21:00:00 +0530
categories: jekyll tutorial
---

### **Git** (Version Control)

> Developed by Linus Torvalds to bring developers together and collaborate remotely.

---

### **Best Practices**

#### **Sync with Remote**
- [ ] **Fork the repository on GitHub**  
      _If you don’t own it or want to contribute to someone else’s project._
- [ ] **Clone your fork or the repo:**  
      `git clone <repo-url>`
- [ ] **(If forked) Set upstream remote for original repo:**  
      `git remote add upstream <original-repo-url>`  
      _This allows you to easily sync your fork with the original repo._
- [ ] **Pull latest changes:**  
      - Direct clone:  
        `git pull origin main`  
      - If working from a fork and want updates from original:  
        `git pull upstream main`
- [ ] **Create and switch to a new branch:**  
      `git checkout -b <branch_name>`  
      _Work on a separate branch to keep features and fixes isolated._
- [ ] **Stage your changes:**  
      `git add .` _or_ `git add <file>`
- [ ] **Commit with a clear message:**  
      `git commit -m "A concise, meaningful message"`
- [ ] **Push your branch to the remote repo:**  
      - For first push of this branch:  
        `git push -u origin <branch_name>`  
      - For subsequent pushes:  
        `git push`

---

#### **Daily Workflow**
- [ ] **Check repo status:**  
      `git status`
- [ ] **See changes in files:**  
      `git diff`
- [ ] **View commit history:**  
      `git log --oneline --graph --all`
- [ ] **List branches:**  
      `git branch`
- [ ] **Create a new branch:**  
      `git branch <branch-name>`
- [ ] **Switch branch:**  
      `git checkout <branch-name>`
- [ ] **Delete a local branch:**  
      `git branch -d <branch-name>`

---

#### **Merging, Rebasing, Tags**
- [ ] **Merge a branch into the current branch:**  
      `git merge <branch-name>`
- [ ] **Rebase feature branch on main:**  
      `git checkout <feature-branch>`  
      `git rebase main`
- [ ] **Resolve conflicts then continue rebase:**  
      `git rebase --continue`
- [ ] **Create annotated tags:**  
      `git tag -a v1.0.0 -m "release v1.0.0"`
- [ ] **Push tags:**  
      `git push origin --tags`

---

#### **Fixing/Cleaning up**
- [ ] **Amend last commit message:**  
      `git commit --amend`
- [ ] **Unstage a file:**  
      `git restore --staged <file>`
- [ ] **Discard local changes to a file:**  
      `git restore <file>`
- [ ] **Stash current changes:**  
      `git stash`
- [ ] **List stash:**  
      `git stash list`
- [ ] **Reapply latest stash & keep it:**  
      `git stash apply`
- [ ] **Reapply latest stash & drop it:**  
      `git stash pop`

---

### **Explanations & Concepts**

- **Fork vs. Clone:**  
  - _Fork_: Make a copy of a repository on your own GitHub account (useful for contributing to projects you don’t own).
  - _Clone_: Download a repository from GitHub to your local computer.
- **Upstream Remote:**  
  - Allows your local/forked repo to fetch new changes from the original (main) repository.
- **Branches:**  
  - Help you work on new features or bug fixes in isolation, keeping the main branch stable.
- **Staging & Committing:**  
  - _Staging (`git add`)_ selects changes to include in your next commit.
  - _Committing (`git commit`)_ saves those staged changes with a message describing what you did.
- **Pushing:**  
  - Uploads your commits from your local machine to the remote GitHub repository.
- **Pulling:**  
  - Downloads the latest changes from the remote repository to your local copy.
- **Merge:**  
  - **Meaning:** Combines changes from one branch into another. For example, merging a feature branch into main will bring your feature code into the main branch.
  - **Practical scenario:** When your new feature is ready and tested, you merge it to main so everyone uses the improved code.
- **Rebase:**  
  - **Meaning:** Moves or combines a sequence of commits to a new base commit. It “replays” your work as if you started from the latest main branch, creating a linear history.
  - **Practical scenario:** Before merging a long-lived feature branch, you rebase it onto main to include recent updates, reducing conflicts.
- **Stash:**  
  - **Meaning:** Temporarily shelves (hides) changes you’ve made, leaving your working directory clean. You can reapply them later.
  - **Practical scenario:** You need to switch branches, but you’re not ready to commit your current work. Stash your changes, switch branches, and then reapply the stash when you return.
- **Reset:**  
  - **Meaning:** Moves your current branch pointer to a specific commit. Depending on options (`--soft`, `--hard`), it can also remove or keep changes.
  - **Practical scenario:** You made mistakes in several commits and want to undo them, or move back to a previous state.
- **Restore:**  
  - **Meaning:** Undoes changes in your working directory or staging area, restoring files or un-staging them.
  - **Practical scenario:** You edited a file but decide to revert it to the version in the last commit, or undo adding a file to the staging area.

---

**Tip:**  
You can check (tick) these boxes on GitHub’s web interface to track your progress!