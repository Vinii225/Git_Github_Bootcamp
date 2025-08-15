# 🌿 Git Branches & Advanced Workflows

> **Extended learning notes** - Git branching, merging, and advanced branch management

📅 **Updated:** August 15, 2025


<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

##  Branches & HEAD in Git

### What is a Branch?

A **branch** in Git is a lightweight movable pointer to a commit. Branches let you work on different features, bug fixes, or experiments in isolation from the main codebase.

- 🏗️ **Main branch** (often called `main` or `master`) is the default branch.
- 🌱 **Feature branches** are used for new features, fixes, or experiments.
- 🔄 **Merging** brings changes from one branch into another.

### What is HEAD?

**HEAD** is a special pointer that always refers to your current branch and commit. When you make a new commit, HEAD moves forward automatically.

- 🎯 **HEAD** tells Git where you are working.
- 🔀 When you switch branches, HEAD moves to point to the new branch.

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🔧 Essential Branch Commands

**Create and switch to a new branch:**
```bash
git switch -c feature-branch      # Create and switch (recommended)
git checkout -b feature-branch    # Alternative (older method)
```

**Switch between branches:**
```bash
git switch main                   # Switch to main branch
git switch feature-branch         # Switch to feature branch
```

**List and check branches:**
```bash
git branch                        # List all branches
git status                        # See current branch and status
```

**Visual Example:**

- `main` ← HEAD (current branch)
- `feature-branch` (another branch)

When you run `git switch feature-branch`, HEAD moves to point to `feature-branch`.

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🚨 Important Branch Workflow Rule

> ⚠️ **Always remember:** Commit your changes before switching branches!

**Why this matters:**
- 🔒 **Prevents data loss** - Uncommitted changes can be lost or mixed
- 🧹 **Keeps branches clean** - Each branch maintains its own state
- 🎯 **Avoids confusion** - Clear separation between different features

**Best Practice:**
```bash
git status                    # Check for uncommitted changes
git add .                     # Stage any changes
git commit -m "save work"     # Commit before switching
git switch other-branch       # Now safe to switch
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🗑️ Deleting Branches

**Delete a branch (force delete):**

```bash
git branch -D branch-name
```

**Important prerequisites:**
- ✅ **Switch to another branch first** - You cannot delete the branch you're currently on
- ⚠️ **Use `-D` carefully** - This force deletes even unmerged branches
- 🔍 **Alternative:** Use `-d` for safe delete (only merged branches)

**Safe workflow:**
```bash
git switch main               # Switch away from target branch
git branch -d feature-branch  # Safe delete (merged only)
git branch -D feature-branch  # Force delete (any branch)
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### ✏️ Renaming Branches

**Rename the current branch:**

```bash
git branch -m new-branch-name
```

**Rename a different branch:**

```bash
git branch -m old-name new-name
```

**Common use cases:**
- 🏷️ **Fix typos** in branch names
- 📝 **Update naming convention** to match team standards
- 🎯 **Make names more descriptive** for better organization

**Example:**
```bash
git branch -m feature-login           # Rename current branch
git branch -m old-feature new-feature # Rename specific branch
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔀 Merging Branches

### What is Merging?

**Merging** is the process of incorporating changes from one branch into another. When working on features in separate branches, you can merge to bring those changes back to the main branch.

**Key Points:**
- 🌿 **We merge branches**, not specific commits
- 🎯 **We always merge TO the current HEAD branch**
- 🔄 **Switch to the target branch first**, then merge the source branch

### Basic Merge Workflow

**Step-by-step process:**

```bash
git switch main               # Switch to target branch (usually main)
git merge feature-branch      # Merge the feature branch into main
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚡ Types of Merges

### 🚀 Fast-Forward Merge

When the target branch hasn't diverged from the feature branch, Git can simply move the pointer forward.

**Characteristics:**
- 📈 **Linear history** - No merge commit created
- 🎯 **Simple** - Just moves the branch pointer
- ✅ **Clean** - Maintains a straight line of commits

### 🔀 Merge Commits

When both branches have new commits, Git creates a special merge commit that combines the changes.

**Characteristics:**
- 🌊 **Non-linear history** - Creates a merge commit
- 🔗 **Preserves context** - Shows where branches merged
- 📊 **Two parents** - Merge commit has multiple parent commits

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚠️ Merge Conflicts

### What are Merge Conflicts?

**Merge conflicts** occur when Git cannot automatically merge changes because the same lines were modified differently in both branches.

### When Conflicts Happen

- 📝 **Same file, same lines** modified differently
- 🔄 **Different changes** to the same content
- 🤝 **Manual resolution** required

### Resolving Merge Conflicts

**Step-by-step resolution:**

1. **Git warns you** in the console that it couldn't automatically merge
2. **Open the conflicted file(s)** - Git marks the conflicts
3. **Edit the file** to resolve conflicts:
   - Choose which version to keep
   - Or combine content from both branches
   - Remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
4. **Stage the resolved files** with `git add`
5. **Complete the merge** with `git commit`

**Example conflict markers:**
```text
<<<<<<< HEAD
Current branch content
=======
Feature branch content
>>>>>>> feature-branch
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Remember:** Branching and merging are fundamental Git skills that enable **parallel development**, **feature isolation**, and **collaborative workflows**! 🚀
