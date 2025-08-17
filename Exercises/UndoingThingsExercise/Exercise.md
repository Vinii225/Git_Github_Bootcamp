# ⏰ Git Undoing Things Exercise

> **Hands-on practice** with Git time travel, undoing changes, and branch management

📅 **Date:** August 17, 2025  
🎯 **Objective:** Master Git's undoing commands through a creative lyrics evolution scenario

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📝 Exercise Overview

This exercise explores **Git's time travel capabilities** using a creative scenario based on song lyric evolution. You'll practice checking out commits, creating branches from specific points in history, and undoing changes.

**🎵 Scenario:** Work with the evolution of lyrics from their original form to a modern 404 error parody, learning to navigate and manipulate Git history safely.

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🚀 Part 1: Repository Setup

### 📥 **Clone Exercise Repository**

**Important:** Make sure you're **not inside a Git repository** before running these commands.

```bash
# Clone the exercise repository
git clone https://github.com/Colt/yesterday-exercise
```

### 🔧 **Initial Exploration**

```bash
# Navigate to the cloned repository
cd yesterday-exercise

# Verify repository structure
ls                                # Should see lyrics.txt file

# Examine commit history
git log --oneline                 # View all 8 commits on master branch
```

**Expected:** You should see 8 commits showing the evolution of the lyrics.

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⏰ Part 2: Time Travel Practice

### 🕒 **Travel to First Commit**

**Task:** Go back in time to see the very beginning.

```bash
# Find the first commit hash from git log
git checkout <first-commit-hash>  # Replace with actual hash
```

**Expected results:**
- 🚨 **Detached HEAD warning** appears
- 📄 **lyrics.txt content** shows early version
- ⏰ **Time travel successful** - you're in the past!

### 🔍 **Examine and Return**

```bash
# Look at the lyrics file content
cat lyrics.txt                    # Observe early version

# Return to present (reattach HEAD)
git switch master                 # Back to modern times
```

### 🎯 **Navigate to Specific Commit**

**Task:** Find and checkout the commit with message "finish original lyrics".

```bash
# Find the specific commit
git log --oneline --grep="finish original lyrics"

# Checkout that commit
git checkout <commit-hash>        # Use the found hash

# Create new branch from this point
git switch -c scrambled-eggs      # New branch based on original lyrics
```

**✅ Result:** New branch created from historical commit point.

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🗑️ Part 3: Mistake Recovery Practice

### 🚨 **Simulate Accidental Deletion**

```bash
# Return to master branch
git switch master

# Accidentally delete all content (simulate mistake)
# Open lyrics.txt and delete everything, then save
```

**💥 Crisis:** All lyrics are gone! Time to recover.

### 🔄 **Recover Using Git Commands**

**Task:** Use Git to discard the accidental changes.

```bash
# Option 1: Modern restore command
git restore lyrics.txt

# Option 2: Legacy checkout method
git checkout HEAD lyrics.txt

# Option 3: Alternative restore syntax
git checkout -- lyrics.txt
```

**✅ Success:** Original content restored from last commit!

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎭 Part 4: Creative Parody Development

### ✏️ **Create Parody Lyrics (First Part)**

**Task:** Replace lyrics.txt content with modern 404 error parody.

Replace the entire content with:
```text
404
Guess this ain't the page you're looking for
On this website there are thousands more
With no error 404

Suddenly
This is not the page you thought you'd see
But it's not an error 403
Yes, 404s come easily
```

### 💾 **Commit First Parody Version**

```bash
# Stage and commit the parody
git add lyrics.txt
git commit -m "Add first part of 404 parody lyrics"
```

### 📝 **Add Second Parody Section**

**Task:** Append additional content to lyrics.txt.

Add to the bottom of the file:
```text
Why it has to show, I don't know
Or what it's for
You typed something wrong?
Here's no song - it's 404

404
Adding 1% to twenty score
(I put that line in 'cause it scans, no more)
"Goodbye" from error 404
```

### 💾 **Commit Complete Parody**

```bash
# Stage and commit the complete parody
git add lyrics.txt
git commit -m "Complete 404 parody lyrics"
```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔄 Part 5: Advanced Undoing - Moving Commits

### 🤔 **Change of Plans**

**Scenario:** You realize the parody commits belong on a separate branch, not master.

**Goal:** Move the last 2 commits to a new branch while keeping the changes in your working directory.

### 📍 **Strategic Reset**

**Task:** Undo the last 2 commits but keep the changes.

```bash
# Soft reset to move back 2 commits (keep changes)
git reset HEAD~2                 # Undo last 2 commits, keep changes

# Verify the reset worked
git log --oneline                # Should show 2 fewer commits
git status                       # Should show modified lyrics.txt
cat lyrics.txt                   # Should still contain 404 parody
```

**✅ Expected:** Commits undone, but 404 lyrics still in working directory.

### 🌿 **Create Dedicated Parody Branch**

```bash
# Create and switch to new branch for parody
git switch -c 404

# Commit the parody on its proper branch
git add lyrics.txt
git commit -m "Add 404 parody lyrics on dedicated branch"
```

### 🔍 **Verify Final State**

```bash
# Switch back to master
git switch master

# Verify master has original lyrics
cat lyrics.txt                   # Should show original song lyrics

# Check branch structure
git branch                       # Should show master, 404, and scrambled-eggs
git log --oneline                # Should show original commits only
```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Validation

### ✅ **Success Criteria**

Verify your exercise completion:

```bash
# Check final branch structure
git branch                       # Should have: master, 404, scrambled-eggs

# Verify master branch content
git switch master
cat lyrics.txt                   # Should contain original lyrics

# Verify 404 branch content  
git switch 404
cat lyrics.txt                   # Should contain 404 parody

# Verify scrambled-eggs branch exists
git switch scrambled-eggs
cat lyrics.txt                   # Should contain early version
```

**Expected results:**
- ✅ **Master branch:** Original lyrics preserved
- ✅ **404 branch:** Modern parody lyrics
- ✅ **Scrambled-eggs branch:** Historical version from specific commit
- ✅ **Clean history:** Parody commits moved to appropriate branch

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 💡 Key Learning Outcomes

### 🔧 **Commands Mastered:**

```bash
git checkout <commit-hash>        # Time travel to specific commit
git switch -c <branch>            # Create branch from current commit
git restore <file>                # Discard file changes (modern)
git checkout -- <file>            # Discard file changes (legacy)
git reset HEAD~n                  # Undo n commits (keep changes)
git log --oneline --grep="text"   # Search commit messages
```

### 📚 **Concepts Reinforced:**

- **⏰ Time Travel** - Navigating Git history safely
- **🚨 Detached HEAD** - Understanding and managing detached state
- **🔄 File Recovery** - Multiple methods to discard changes
- **🌿 Branch Creation** - Creating branches from specific commits
- **📍 Strategic Reset** - Moving commits while preserving work
- **🎯 History Management** - Organizing commits on appropriate branches

### 🌟 **Real-World Applications:**

- **🔍 Bug Investigation** - Checking out commits to find when issues started
- **🌿 Feature Branching** - Creating branches from specific historical points
- **🔄 Mistake Recovery** - Safely undoing accidental changes
- **📊 History Reorganization** - Moving commits to appropriate branches
- **🧪 Experimental Work** - Safe exploration of historical states

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Congratulations!** You've mastered Git's time travel and undoing capabilities through creative scenarios. These skills are essential for **professional development** and **safe repository management**! ⏰
