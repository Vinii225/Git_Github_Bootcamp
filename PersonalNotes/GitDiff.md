# 🔍 Git Diff - Comparing Changes

> **Understanding differences** between commits, branches, and working directory

📅 **Updated:** August 15, 2025

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📚 Git Documentation

🔗 **Official Git Diff Documentation:** [https://git-scm.com/docs/git-diff](https://git-scm.com/docs/git-diff)

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 What is Git Diff?

**Git diff** is a powerful command that allows you to view changes between different states of your repository. It's essential for understanding:

- 📝 **What changed** in your files
- 🕒 **When changes** were made
- 🔍 **How code evolved** over time
- 🎯 **Differences between** commits, branches, or working directory

### 🔧 Common Commands for Repository Analysis

**Before using `git diff`, these commands provide context:**

```bash
git status                        # Check current repository state
git log --oneline                 # View commit history
```

**Key benefit:** Git diff has **no impact** on your repository - it's read-only!

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📖 Reading Git Diff Output

### Understanding Diff Symbols

When you run `git diff`, you'll see:

```bash
# Example output format:
- This line was deleted      # ❌ Lines starting with "-"
+ This line was added        # ✅ Lines starting with "+"
  This line is unchanged     # 📄 Lines with no prefix
```

**Symbol meanings:**
- **`-`** = Line was **deleted/removed**
- **`+`** = Line was **added/new**
- No symbol = Line **unchanged**

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔧 Essential Git Diff Commands

### 📂 Basic Working Directory Diff

```bash
git diff                          # Compare working directory with staging area
```

**Use case:** See what changes you've made but haven't staged yet.

### 📋 Staged Changes Diff

```bash
git diff --staged                 # Compare staging area with last commit
git diff --cached                 # Alternative syntax (same result)
```

**Use case:** Review changes that are staged and ready to commit.

### 📄 Specific File Diff

```bash
git diff filename                 # Show changes in specific file
git diff --staged filename        # Show staged changes in specific file
```

**Use case:** Focus on changes in particular files only.

### 🕒 Commit Comparison

```bash
git diff HEAD                     # Compare working directory with last commit
git diff commit1 commit2          # Compare two specific commits
```

**Use case:** See all changes since last commit or between any two commits.

### 🌿 Branch Comparison

```bash
git diff branch1 branch2          # Compare two branches
git diff main feature-branch      # Compare main with feature branch
```

**Use case:** See differences between branches before merging.

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚡ Quick Commit Tip

### Faster Staging and Committing

```bash
git commit -am "commit message"   # Stage all tracked files AND commit
```

**What `-a` does:**
- 🔄 **Automatically stages** all modified tracked files
- ⏭️ **Skips** the `git add` step
- ⚠️ **Note:** Only works with files Git is already tracking (not new files)

**Equivalent workflow:**
```bash
# Instead of:
git add .
git commit -m "commit message"

# You can use:
git commit -am "commit message"
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Common Git Diff Workflow

### Step-by-Step Usage

1. **Check current status**
   ```bash
   git status                    # See what files have changed
   ```

2. **Review changes before staging**
   ```bash
   git diff                      # See unstaged changes
   git diff filename             # Focus on specific file
   ```

3. **Stage files**
   ```bash
   git add filename              # Stage specific files
   ```

4. **Review staged changes**
   ```bash
   git diff --staged             # Review what's about to be committed
   ```

5. **Commit changes**
   ```bash
   git commit -m "descriptive message"
   ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 💡 Pro Tips

### Best Practices

- 🔍 **Always review** changes with `git diff` before committing
- 📄 **Use specific filenames** to focus on particular changes
- 🔄 **Check staged changes** with `git diff --staged` before committing
- 🌿 **Compare branches** before merging to avoid surprises
- 📚 **Combine with `git log`** for complete understanding of repository history

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Remember:** Git diff is your **detective tool** for understanding changes in your codebase. Use it frequently to stay aware of modifications! 🕵️‍♂️
