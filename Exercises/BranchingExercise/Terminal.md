# 💻 Branching Exercise - Terminal Session

> **Real terminal commands and outputs** - Step-by-step execution of the Harry Potter Patronus exercise

📅 **Exercise Completed:** August 12, 2025  
👤 **Author:** Vinícius Ares  
📧 **Email:** vinicius.ares12@gmail.com

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Overview

This document shows the actual terminal commands executed during the Branching Exercise, demonstrating branch creation, switching, and management with magical Harry Potter themes.

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📄 Step 1: Initial Commit - Empty Patronus File

**Command executed:**
```bash
git add BranchingExercise/Patronus/patronus.txt
git commit -m "add empty patronus file"
```

**Git response:**
```
[main 3a2cbfb] add empty patronus file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 BranchingExercise/Patronus/patronus.txt
```

**Analysis:**
- ✅ **Empty file created** - Starting point for all branches
- 📊 **Git output** - Shows file creation with no content changes
- 🎯 **Clean baseline** - All branches will start from this point

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🌿 Step 2: Creating Multiple Branches

**Commands executed:**
```bash
git branch harry
git branch snape
git branch
```

**Git response:**
```
  harry
* main
  snape
```

**Analysis:**
- ✅ **Two branches created** - `harry` and `snape` based on main
- 🎯 **Current branch** - Asterisk (*) shows we're still on `main`
- 📊 **Branch list** - Shows all available branches in alphabetical order

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🦌 Step 3: Harry's Stag Patronus Branch

**Commands executed:**
```bash
git switch harry
git add BranchingExercise/Patronus/patronus.txt
git commit -m "add harry's stag patronus"
```

**Git response:**
```
Switched to branch 'harry'
[harry 32f5d92] add harry's stag patronus
 1 file changed, 26 insertions(+)
```

**Analysis:**
- 🔄 **Branch switch successful** - Now working on `harry` branch
- 📝 **Large content addition** - 26 lines of ASCII art added
- 🎯 **Branch-specific commit** - Changes only exist on `harry` branch

**Note:** First attempt with `git add patronus.txt` failed - needed full path!

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🦌 Step 4: Snape's Doe Patronus Branch

**Commands executed:**
```bash
git checkout snape
git add BranchingExercise/Patronus/patronus.txt
git commit -m "add snape's doe patronus"
```

**Git response:**
```
Switched to branch 'snape'
[snape 5530835] add snape's doe patronus
 1 file changed, 16 insertions(+)
```

**Analysis:**
- 🔄 **Used older command** - `git checkout` instead of `git switch`
- 📝 **Different content** - 16 lines of doe ASCII art
- 🎯 **Independent branch** - Completely different from `harry` branch

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🌸 Step 5: Lily's Doe Patronus Branch

**Commands executed:**
```bash
git branch lily
git switch lily
git add BranchingExercise/Patronus/patronus.txt
git commit -m "add lily's doe patronus"
```

**Git response:**
```
Switched to branch 'lily'
[lily 4031b1a] add lily's doe patronus
 1 file changed, 1 insertion(+), 1 deletion(-)
```

**Analysis:**
- 🌿 **Branch created from `snape`** - Inherits Snape's doe patronus
- ✏️ **Minor modification** - Only changed the title line
- 📊 **Git output** - Shows 1 insertion, 1 deletion (title change)

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📊 Step 6: Final Branch Management

**Commands executed:**
```bash
git branch
git branch -d snape
```

**Git response:**
```
  harry
* lily
  main
  snape

Deleted branch snape (was 5530835).
```

**Analysis:**
- ✅ **4 branches total** - `harry`, `lily`, `main`, `snape`
- 🎯 **Current position** - On `lily` branch (marked with *)
- 🗑️ **Safe deletion** - Used `-d` flag to delete merged branch
- 💀 **Poor Snape** - Branch successfully removed!

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎓 Key Learnings from This Session

- 🌿 **Branch isolation** - Each branch maintains independent file content
- 🔄 **Two switch methods** - Both `git switch` (new) and `git checkout` (older) work
- 📂 **File path importance** - Need correct path when not in the file's directory
- 🎯 **Branch inheritance** - New branches inherit content from their parent
- 🗑️ **Safe deletion** - Use `-d` for merged branches, `-D` for force delete

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔧 Commands Used in This Session

```bash
git branch branch-name                    # Create new branch
git branch                               # List all branches
git switch branch-name                   # Switch to branch (newer command)
git checkout branch-name                 # Switch to branch (older command)
git add file-path                        # Stage specific file
git commit -m "message"                  # Commit with message
git branch -d branch-name                # Delete branch (safe)
```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Success!** This terminal session demonstrates the magic of **Git branching** - multiple parallel development paths! ⚡✨
