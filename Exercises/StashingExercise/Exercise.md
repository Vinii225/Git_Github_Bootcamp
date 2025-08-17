# 📦 Git Stashing Exercise

> **Hands-on practice** with Git stash for managing uncommitted changes during context switching

📅 **Date:** August 17, 2025  
🎯 **Objective:** Master Git stash commands through a dramatic workplace scenario

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📝 Exercise Overview

This exercise demonstrates the **power of Git stash** through a humorous workplace scenario. You'll learn to quickly save uncommitted work when urgent context switches are needed.

**🎭 Scenario:** You're working on your honest thoughts when your boss unexpectedly approaches. Use Git stash to quickly hide your work and maintain your professional image!

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🚀 Part 1: Repository Setup

### 📂 **Step 1: Initialize Repository**

```bash
# Create and initialize a new Git repository
mkdir stash-exercise
cd stash-exercise
git init
```

### 📄 **Step 2: Create Initial File**

Create a file called `diary.txt` with the following content:

```text
I love my boss
```

### 💾 **Step 3: Initial Commit**

```bash
# Add and commit the initial content
git add diary.txt
git commit -m "Add initial diary entry"
```

**✅ Status:** Repository initialized with professional diary entry on `main` branch.

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🌿 Part 2: Branch Creation & Truth Telling

### 🔀 **Step 4: Create Truth Branch**

```bash
# Create and switch to new branch for honest thoughts
git switch -c the-truth
```

### ✏️ **Step 5: Express True Feelings**

Edit `diary.txt` to contain your honest thoughts:

```text
I HATE MY BOSS
I HATE MY BOSS
I HATE MY BOSS
I HATE MY BOSS
I HATE MY BOSS
```

### 💾 **Step 6: Save the File**

Save your changes but **DO NOT COMMIT YET!**

**⚠️ Critical moment:** Your work is saved but uncommitted - perfect stash scenario!

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🚨 Part 3: Emergency Context Switch

### 😱 **Step 7: Boss Alert!**

**OH NO!** Your boss is walking towards you! Quick action needed!

```bash
# Emergency switch to main branch
git switch main
```

**🔥 Problem:** Git shows your uncommitted changes and won't let you switch cleanly!

### 📦 **Step 8: Emergency Stash**

**QUICK!** Stash your honest thoughts before your boss sees:

```bash
# Stash uncommitted changes immediately
git stash -m "hiding true feelings from boss"
```

### ✅ **Step 9: Verify Safety**

Check that `diary.txt` now shows only:

```text
I love my boss
```

**🎭 Success:** Your professional image is preserved!

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 😇 Part 4: Playing the Part

### 📝 **Step 10: Add More Professional Content**

While your boss is watching, enhance your professional image by editing `diary.txt`:

```text
I love my boss
I love my boss
I love my boss
```

### 💾 **Step 11: Commit Professional Changes**

```bash
# Commit the professional content
git add diary.txt
git commit -m "Add more positive thoughts about management"
```

**🎯 Boss Status:** Impressed with your dedication and positive attitude!

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🕵️ Part 5: Return to Truth

### 🔄 **Step 12: Boss Has Left**

Now that your boss has left, it's safe to return to your honest work:

```bash
# Switch back to the truth branch
git switch the-truth
```

### 📦 **Step 13: Retrieve Stashed Truth**

Restore your honest thoughts from the stash:

```bash
# Retrieve stashed changes
git stash pop
```

**Expected result:** Your true feelings are restored in `diary.txt`

### 💾 **Step 14: Commit the Truth**

```bash
# Commit your honest thoughts
git add diary.txt
git commit -m "Document true feelings about management"
```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Validation

### ✅ **Success Criteria:**

Verify your exercise completion:

```bash
# Check commit history on main branch
git switch main
git log --oneline

# Check commit history on truth branch  
git switch the-truth
git log --oneline

# Verify stash is empty
git stash list
```

**Expected results:**
- ✅ **Main branch:** 2 commits with professional content
- ✅ **Truth branch:** 2 commits with honest content  
- ✅ **Stash list:** Empty (stash was popped)
- ✅ **File contents:** Different on each branch

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 💡 Key Learning Outcomes

### 🔧 **Commands Mastered:**

```bash
git stash -m "message"            # Save uncommitted work with description
git stash pop                     # Apply and remove stash
git stash list                    # View all stashes
git switch <branch>               # Quick branch switching
```

### 📚 **Concepts Reinforced:**

- **🚨 Emergency stashing** - Quick uncommitted work preservation
- **🔄 Context switching** - Managing multiple work streams
- **🌿 Branch isolation** - Keeping different work separate
- **📦 Temporary storage** - Using stash as intermediate workspace
- **💾 Commit timing** - Strategic saving of work states

### 🎭 **Real-World Applications:**

This scenario mirrors real development situations:
- **Urgent bug fixes** while working on features
- **Code reviews** requiring clean working directory
- **Meetings interrupting** active development
- **Experimental work** that needs temporary hiding

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Congratulations!** You've mastered Git stash through workplace drama. These skills are essential for **professional development workflows** and **emergency context switching**! 🎭
