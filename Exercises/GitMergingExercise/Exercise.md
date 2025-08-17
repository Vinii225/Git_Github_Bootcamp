# 🔀 Git Merging Exercise

> **Hands-on practice** with Git merging workflows and conflict resolution

📅 **Date:** August 15, 2025  
🎯 **Objective:** Master different types of Git merges through practical scenarios

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📝 Exercise Overview

This exercise is designed to help you **create your own scenarios** rather than following step-by-step instructions. You'll demonstrate understanding by generating different types of merges independently.

### 🚀 Getting Started

1. **Create a new repository** for this exercise
2. **Make a file or two** in the repo to work with
3. **Complete each part** by creating the required merge scenarios

**💡 Inspiration:** You can work with a `greetings.txt` file containing greetings in different languages, or choose your own content!

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚡ Part 1: Fast-Forward Merge

### 🎯 **Goal:** Generate a fast-forward merge

**Your mission:**
- ✅ Create a new branch
- ✅ Make changes that result in a **linear history**
- ✅ Merge the branch into `main` using fast-forward
- ✅ Verify the merge was fast-forward (no merge commit)

**Key Concept:** Fast-forward merges happen when the target branch hasn't diverged from the feature branch.

### 🧪 Challenge Steps:
1. Create and switch to a new branch
2. Make commits on the new branch (while `main` stays unchanged)
3. Switch back to `main` and merge
4. Check `git log --oneline` to confirm linear history

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔗 Part 2: Merge Commit (No Conflicts)

### 🎯 **Goal:** Generate a merge commit with NO conflicts

**Your mission:**
- ✅ Create a new branch
- ✅ Make changes on **both branches** (different files/areas)
- ✅ Merge to create a **merge commit**
- ✅ Ensure **no conflicts** occur during merge

**Key Concept:** Merge commits happen when both branches have new commits, but they don't conflict.

### 🧪 Challenge Steps:
1. Create and switch to a new branch
2. Make commits on the feature branch
3. Switch to `main` and make different commits (non-conflicting)
4. Merge the feature branch and observe the merge commit

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚠️ Part 3: Merge Conflicts

### 🎯 **Goal:** Generate and resolve merge conflicts

**Your mission:**
- ✅ Create a new branch
- ✅ Make **conflicting changes** on both branches
- ✅ Trigger a **merge conflict**
- ✅ **Resolve the conflict** manually
- ✅ Complete the merge successfully

**Key Concept:** Conflicts occur when the same lines are modified differently in both branches.

### 🧪 Challenge Steps:
1. Create and switch to a new branch
2. Modify the same lines in a file
3. Switch to `main` and modify the same lines differently
4. Attempt to merge (conflict will occur)
5. Resolve conflicts by editing the file
6. Stage resolved files and complete merge

### 🔧 Conflict Resolution Reminder:
```bash
# After conflict occurs:
git status                    # See conflicted files
# Edit files to resolve conflicts
git add .                     # Stage resolved files
git commit                    # Complete the merge
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Success Criteria

**You'll know you've succeeded when:**
- ✅ **Part 1:** `git log --oneline` shows linear history (no merge commit)
- ✅ **Part 2:** `git log --oneline` shows a merge commit with two parent commits
- ✅ **Part 3:** You successfully resolve conflicts and complete the merge