# 💻 Committing Basics Exercise - Terminal Session

> **Real terminal commands and outputs** - Step-by-step execution of the shopping list exercise
  
👤 **Author:** Vinícius Ares  
📧 **Email:** vinicius.ares12@gmail.com

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Overview

This document shows the actual terminal commands executed during the Committing Basics Exercise, demonstrating selective staging and meaningful commit messages in practice.

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🥄 Step 1: Adding Groceries for Tomato Soup

**Command executed:**
```bash
git add CommittingBasicsExercise/Shopping/groceries.txt
git commit -m "add ingredients for tomato soup"
```

**Git response:**
```
[main 4cbe054] add ingredients for tomato soup
 1 file changed, 3 insertions(+)
 create mode 100644 CommittingBasicsExercise/Shopping/groceries.txt
```

**Analysis:**
- ✅ **Selective staging** - Only added `groceries.txt` 
- 📝 **Meaningful message** - Clearly describes what ingredients were added
- 📊 **Git output** - Shows 1 file changed with 3 new lines

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🌱 Step 2: Adding Yard/Garden Items

**Command executed:**
```bash
git add CommittingBasicsExercise/Shopping/yard.txt
git commit -m "add items needed for garden box"
```

**Git response:**
```
[main 9ac1f3d] add items needed for garden box
 1 file changed, 2 insertions(+)
 create mode 100644 CommittingBasicsExercise/Shopping/yard.txt
```

**Analysis:**
- ✅ **Separate commit** - Kept yard items isolated from groceries
- 🎯 **Focused change** - Only garden-related modifications
- 📊 **Git output** - Shows 1 file changed with 2 new lines

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🥔 Step 3: Adding Potato-Related Items (Both Files)

**Command executed:**
```bash
git add .
git commit -m "add items needed to grow potatoes"
```

**Git response:**
```
[main 49d67a8] add items needed to grow potatoes
 4 files changed, 43 insertions(+), 3 deletions(-)
 create mode 100644 CommittingBasicsExercise/Exercise.md
```

**Analysis:**
- 📦 **Bulk commit** - Used `git add .` to stage all changes
- 🥔 **Thematic grouping** - Both files related to potato growing
- 📊 **Git output** - Shows 4 files changed (including Exercise.md creation)

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📊 Final Commit History

**Command executed:**
```bash
git log
```

**Git response:**
```
commit 49d67a8207baa6d3f60ce1fbb7604e86e862fc6a (HEAD -> main)
Author: Vinícius Ares <vinicius.ares12@gmail.com>
Date:   Thu Jul 31 06:45:27 2025 -0300

    add items needed to grow potatoes

commit 9ac1f3d61549db30b3a1946abc3ec3425e932554
Author: Vinícius Ares <vinicius.ares12@gmail.com>
Date:   Thu Jul 31 06:43:09 2025 -0300

    add items needed for garden box

commit 4cbe054f2aeef70dfdef9175f775b18b74818d9f
Author: Vinícius Ares <vinicius.ares12@gmail.com>
Date:   Thu Jul 31 06:42:24 2025 -0300

    add ingredients for tomato soup
```

**Analysis:**
- ✅ **3 Total commits** - Exactly as planned in the exercise
- 🕐 **Chronological order** - Latest commit first (Git default)
- 🎯 **Clear progression** - Each commit builds on the previous one
- 📝 **Descriptive messages** - Easy to understand what each commit contains

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎓 Key Learnings from This Session

- 🎯 **Selective staging** allows precise control over what goes into each commit
- 📝 **Meaningful commit messages** make project history readable and useful
- 🔄 **Atomic commits** keep related changes together while separating unrelated ones
- 📊 **Git provides feedback** on every operation to confirm what happened
- 🕐 **Timestamps** show when each change was made for project timeline tracking

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔧 Commands Used in This Session

```bash
git add <specific-file>              # Stage individual files
git add .                           # Stage all changes
git commit -m "message"             # Commit with message
git log                             # View commit history
```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Success!** This terminal session demonstrates the power of **thoughtful commits** and **selective staging** in real-world Git workflows! 🚀
