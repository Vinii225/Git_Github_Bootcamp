# 🔍 Git Diff Exercise

> **Hands-on practice** with Git diff commands using branch comparisons and file changes

📅 **Date:** August 15, 2025  
🎯 **Objective:** Master Git diff commands through practical scenarios with Queen and Fleetwood Mac band lineups

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📝 Exercise Overview

This exercise uses a **starter repository** containing band lineup information across different time periods. You'll practice comparing changes between branches, commits, and working directory states.

**🎵 Scenario:** Working with two legendary bands:
- **Queen** - Various lineups over the years
- **Fleetwood Mac** - Different band members across decades

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🚀 Part 1: Repository Setup

### 📥 Clone the Exercise Repository

**Important:** Make sure you're **not inside a Git repository** before running these commands.

```bash
# Clone the exercise repository
git clone https://github.com/Colt/git-diff-exercise
```

### 🔧 Initial Setup Steps

```bash
# 1. Navigate to the cloned repository
cd git-diff-exercise

# 2. Check current branch (should be on 'current' by default)
git branch

# 3. Switch to the 1970s branch
git switch 1970s

# 4. Verify available branches
git branch
```

### 📂 Repository Structure

**Available branches:**
- **`current`** - Modern band lineups
- **`1970s`** - Historical band lineups from the 1970s

**Files in each branch:**
- **`queen.txt`** - Queen band member information
- **`fleetwoodmac.txt`** - Fleetwood Mac member information

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔍 Part 2: Git Diff Practice

### 🌿 1. Branch Comparison (All Files)

**Task:** Compare differences between `1970s` and `current` branches across all files.

```bash
git diff 1970s current
```

**Expected:** See all changes in both `queen.txt` and `fleetwoodmac.txt` between the two time periods.

### 📄 2. Branch Comparison (Specific File)

**Task:** Compare differences between branches for only the `queen.txt` file.

```bash
git diff 1970s current queen.txt
```

**Expected:** See only Queen band lineup changes between 1970s and current.

### 🕒 3. Commit History Comparison

**Task:** Switch to `current` branch and compare HEAD with previous commit.

```bash
# Switch to current branch
git switch current

# Compare current HEAD with parent commit
git diff HEAD~1                # Using relative reference
# OR
git diff HEAD^                 # Alternative syntax
# OR  
git diff <commit-hash>         # Using specific commit hash
```

**Expected:** See the most recent changes made on the current branch.

### ✏️ 4. Stage Changes to Queen File

**Task:** Modify `queen.txt` and stage the changes.

```bash
# Edit queen.txt - replace "Adam Lambert" with your own name
# Save the file

# Stage the changes
git add queen.txt
```

**⚠️ Important:** Do NOT commit yet!

### 📝 5. Modify Fleetwood Mac File (Unstaged)

**Task:** Edit `fleetwoodmac.txt` but keep changes unstaged.

```bash
# Edit fleetwoodmac.txt
# Change "Stevie Nicks" to "Stevie Chicks"
# Save the file but do NOT stage it
```

### 🔍 6. View Unstaged Changes Only

**Task:** Show only unstaged changes in working directory.

```bash
git diff
```

**Expected:** See only the `fleetwoodmac.txt` changes (unstaged modifications).

### 📋 7. View Staged Changes Only

**Task:** Show only staged changes ready for commit.

```bash
git diff --staged
# OR
git diff --cached
```

**Expected:** See only the `queen.txt` changes (staged modifications).

### 🎯 8. View All Changes Since Last Commit

**Task:** Show both staged and unstaged changes since previous commit.

```bash
git diff HEAD
```

**Expected:** See both `queen.txt` (staged) and `fleetwoodmac.txt` (unstaged) changes.

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Success Criteria

**You'll know you've completed the exercise successfully when:**

- ✅ **Branch diffs** show lineup changes between 1970s and current eras
- ✅ **File-specific diffs** focus only on Queen band changes
- ✅ **Commit diffs** reveal recent changes on current branch
- ✅ **Unstaged diff** shows only Fleetwood Mac changes
- ✅ **Staged diff** shows only Queen changes
- ✅ **HEAD diff** shows both staged and unstaged modifications

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 💡 Key Learning Outcomes

### 🔧 Commands Mastered

```bash
git diff branch1 branch2              # Compare branches
git diff branch1 branch2 filename     # Compare specific file across branches
git diff HEAD~1                       # Compare with previous commit
git diff                              # Show unstaged changes
git diff --staged                     # Show staged changes  
git diff HEAD                         # Show all changes since last commit
```

### 📚 Concepts Reinforced

- **🌿 Branch comparison** - Understanding evolution across time periods
- **📄 File-specific analysis** - Focusing on particular changes
- **🕒 Commit history** - Tracking recent modifications
- **📋 Staging workflow** - Distinguishing staged vs unstaged changes
- **🎯 Working directory states** - Managing different change types

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Remember:** Git diff is essential for **code review**, **debugging**, and **understanding project evolution**. Practice these commands regularly! 🎸