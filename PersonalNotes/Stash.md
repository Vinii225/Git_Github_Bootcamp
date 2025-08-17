# 📦 Git Stash - Temporary Storage

📅 **Updated:** August 17, 2025

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📚 Git Documentation

🔗 **Official Git Stash Documentation:** [https://git-scm.com/docs/git-stash](https://git-scm.com/docs/git-stash)

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 What is Git Stash?

**Git Stash** provides an easy way to temporarily save uncommitted changes without making unnecessary commits. It's perfect for when you need to quickly switch contexts but aren't ready to commit your current work.

### 🔧 Common Use Cases

- 🔄 **Switch branches** without committing incomplete work
- 🚨 **Handle urgent fixes** while working on features
- 🧪 **Experiment safely** without losing current changes
- 🎯 **Clean working directory** temporarily for other tasks

**Key benefit:** Stash preserves both **staged and unstaged changes** without creating commits!

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📦 Basic Stash Operations

### 💾 Saving Changes to Stash

```bash
git stash                         # Save current changes to stash
git stash -m "work in progress"   # Save with descriptive message
```

**What gets stashed:**
- ✅ **Modified tracked files** (both staged and unstaged)
- ✅ **Staged changes** ready for commit
- ❌ **Untracked files** (unless specified with `-u` flag)

### 📤 Retrieving Changes from Stash

```bash
git stash pop                     # Apply and remove from stash
git stash apply                   # Apply but keep in stash
```

**Key difference:**
- **`pop`** = Apply changes **and remove** from stash (one-time use)
- **`apply`** = Apply changes **but keep** in stash (reusable)

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📚 Advanced Stash Management

### 📋 Working with Multiple Stashes

**Git stash works like a stack** - you can add multiple stashes in order:

```bash
git stash list                    # View all stashes
```

**Example output:**
```bash
stash@{0}: WIP on main: 1234567 Latest commit
stash@{1}: WIP on feature: 8901234 Feature work
stash@{2}: On bugfix: 5678901 Bug investigation
```

### 🎯 Applying Specific Stashes

```bash
git stash apply stash@{2}         # Apply specific stash by index
git stash pop stash@{1}           # Pop specific stash by index
```

**Index system:**
- **`stash@{0}`** = Most recent stash
- **`stash@{1}`** = Second most recent
- **`stash@{2}`** = Third most recent, etc.

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🗑️ Stash Cleanup Operations

### 🔥 Removing Stashes

```bash
git stash drop stash@{2}          # Delete specific stash
git stash clear                   # Delete ALL stashes
```

**⚠️ Warning:** `git stash clear` permanently deletes all stashes - use with caution!

### 📊 Stash Information

```bash
git stash show                    # Show summary of latest stash
git stash show stash@{1}          # Show summary of specific stash
git stash show -p                 # Show full diff of latest stash
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔧 Complete Stash Command Reference

```bash
# Basic operations
git stash                         # Save current changes
git stash -m "message"            # Save with custom message
git stash -u                      # Include untracked files

# Retrieving changes
git stash pop                     # Apply latest and remove
git stash apply                   # Apply latest but keep
git stash apply stash@{1}         # Apply specific stash

# Management
git stash list                    # List all stashes
git stash show                    # Show stash summary
git stash show -p                 # Show stash diff

# Cleanup
git stash drop stash@{1}          # Delete specific stash
git stash clear                   # Delete all stashes
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 💡 Stash Best Practices

### 🎯 When to Use Stash

**✅ Good use cases:**
- Switching branches with uncommitted work
- Pulling changes when working directory isn't clean
- Temporarily testing different approaches
- Handling interruptions during development

**❌ Avoid stashing when:**
- Work is ready to be committed
- Changes are experimental and might be discarded
- Working on long-term features (use branches instead)

### 📝 Stash Tips

- 🏷️ **Use descriptive messages** with `git stash -m "message"`
- 🔍 **Check stash contents** with `git stash show` before applying
- 🧹 **Clean up regularly** with `git stash drop` for unused stashes
- 📋 **Review stash list** periodically with `git stash list`

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🚀 Common Stash Workflow

### Step-by-Step Example

```bash
# 1. Working on feature when urgent fix needed
git status                        # Check current changes
git stash -m "feature work in progress"

# 2. Switch to fix urgent issue
git switch main
# ... make urgent fixes and commit ...

# 3. Return to feature work
git switch feature-branch
git stash pop                     # Restore your work

# 4. Continue development
git status                        # Verify changes restored
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Remember:** Git stash is your **temporary workspace** for managing uncommitted changes. Use it to maintain clean workflows without losing work! 📦
