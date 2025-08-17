# 🔍 Git Diff Exercise - Terminal Session

> **Practical terminal session** demonstrating Git diff commands with band lineup comparisons

📅 **Date:** August 15, 2025  
🎯 **Objective:** Master Git diff through hands-on practice with Queen and Fleetwood Mac repositories

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📂 Part 1: Repository Setup & Branch Navigation

### 🚀 **Initial Status Check**

```powershell
# Navigate to exercise repository and check status
PS > cd "c:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise"
PS > git status

On branch current
Your branch is up to date with 'origin/current'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   fleetwoodmac.txt
        modified:   queen.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

### 🌿 **Branch Discovery**

```powershell
# Check all available branches
PS > git branch -a
* current
  remotes/origin/1970s
  remotes/origin/HEAD -> origin/current
  remotes/origin/current
```

### 🔄 **Reset and Switch to 1970s Branch**

```powershell
# Reset any uncommitted changes to start fresh
PS > git restore .

# Switch to 1970s branch to begin exercise
PS > git switch 1970s
branch '1970s' set up to track 'origin/1970s'.
Switched to a new branch '1970s'
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔍 Part 2: Git Diff Commands Practice

### 📊 **Task 1: Compare All Files Between Branches**

```powershell
# Compare 1970s vs current across all files
PS > git diff 1970s current

diff --git a/fleetwoodmac.txt b/fleetwoodmac.txt
index 6f44367..653b184 100644
--- a/fleetwoodmac.txt
+++ b/fleetwoodmac.txt
@@ -1,5 +1,5 @@
-Lead Vocals: Jeremy Spencer        # ← 1970s lineup
-Lead Guitar: Lindsey Buckingham
+Lead Vocals: Stevie Nicks         # ← Current lineup
+Lead Guitar: Mike Campbell
 Bass: John McVie
 Drums: Mick Fleetwood
-Keyboard: None
+Keyboard: Christine McVie

diff --git a/queen.txt b/queen.txt
index 2ab2d04..0e0fa0d 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Freddie Mercury      # ← Classic Queen era
+Lead Vocals: Adam Lambert         # ← Modern Queen lineup
 Lead Guitar: Brian May
-Bass: Mike Grose
+Bass: Neil Fairclough
 Drums: Roger Taylor
```

**✅ Result:** Shows evolution of both bands from 1970s to current era

### 📄 **Task 2: Compare Specific File Between Branches**

```powershell
# Focus only on Queen lineup changes
PS > git diff 1970s current queen.txt

diff --git a/queen.txt b/queen.txt
index 2ab2d04..0e0fa0d 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Freddie Mercury      # ← Legendary frontman
+Lead Vocals: Adam Lambert         # ← Current touring vocalist
 Lead Guitar: Brian May
-Bass: Mike Grose
+Bass: Neil Fairclough
 Drums: Roger Taylor
```

**✅ Result:** Isolated view of Queen's lineup evolution only

### 🕒 **Task 3: Compare Current HEAD with Previous Commit**

```powershell
# Switch to current branch
PS > git switch current
Switched to branch 'current'
Your branch is up to date with 'origin/current'.

# Compare with previous commit
PS > git diff HEAD~1

diff --git a/queen.txt b/queen.txt
index f7f4a33..0e0fa0d 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
 Lead Vocals: Adam Lambert
 Lead Guitar: Brian May
-Bass: John Deacon                 # ← Previous bassist
+Bass: Neil Fairclough            # ← Current bassist
 Drums: Roger Taylor
```

**✅ Result:** Shows the most recent change was updating the bass player

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ✏️ Part 3: Working Directory & Staging Practice

### 📝 **Task 4 & 5: Create Staged and Unstaged Changes**

```powershell
# Stage modified queen.txt (after changing Adam Lambert to "Vinicius Ares")
PS > git add queen.txt
```

### 🔍 **Task 6: View Unstaged Changes Only**

```powershell
# Show only unstaged modifications
PS > git diff

diff --git a/fleetwoodmac.txt b/fleetwoodmac.txt
index 653b184..8c384c0 100644
--- a/fleetwoodmac.txt
+++ b/fleetwoodmac.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Stevie Nicks         # ← Original
+Lead Vocals: Stevie Chicks        # ← Fun modification (unstaged)
 Lead Guitar: Mike Campbell
 Bass: John McVie
 Drums: Mick Fleetwood
```

**✅ Result:** Only shows unstaged Fleetwood Mac changes

### 📋 **Task 7: View Staged Changes Only**

```powershell
# Show only staged modifications
PS > git diff --staged

diff --git a/queen.txt b/queen.txt
index 0e0fa0d..5f562c1 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Adam Lambert         # ← Original
+Lead Vocals: Vinicius Ares        # ← Personal modification (staged)
 Lead Guitar: Brian May
 Bass: Neil Fairclough
 Drums: Roger Taylor
```

**✅ Result:** Only shows staged Queen changes

### 🎯 **Task 8: View All Changes Since Last Commit**

```powershell
# Show both staged and unstaged changes
PS > git diff HEAD

diff --git a/fleetwoodmac.txt b/fleetwoodmac.txt
index 653b184..8c384c0 100644
--- a/fleetwoodmac.txt
+++ b/fleetwoodmac.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Stevie Nicks         # ← Unstaged change
+Lead Vocals: Stevie Chicks
 Lead Guitar: Mike Campbell
 Bass: John McVie
 Drums: Mick Fleetwood

diff --git a/queen.txt b/queen.txt
index 0e0fa0d..5f562c1 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Adam Lambert         # ← Staged change
+Lead Vocals: Vinicius Ares
 Lead Guitar: Brian May
 Bass: Neil Fairclough
 Drums: Roger Taylor
```

**✅ Result:** Shows both staged (Queen) and unstaged (Fleetwood Mac) changes

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Summary

### ✅ **Commands Successfully Demonstrated:**

```bash
git diff branch1 branch2              # Branch comparison (all files)
git diff branch1 branch2 filename     # Branch comparison (specific file)
git diff HEAD~1                       # Compare with previous commit
git diff                              # Show unstaged changes
git diff --staged                     # Show staged changes
git diff HEAD                         # Show all changes since last commit
```

### 📚 **Key Learning Outcomes:**

- **🌿 Branch Evolution** - Tracked band lineup changes across decades
- **📄 File-Specific Analysis** - Focused diff output on particular files
- **🕒 Commit History** - Understood recent changes in repository
- **📋 Staging Workflow** - Distinguished between staged and unstaged modifications
- **🎯 Working Directory Management** - Practiced different change states

### 🎵 **Real-World Application:**

This exercise demonstrated how Git diff helps with:
- **Code reviews** - Understanding what changed between versions
- **Debugging** - Tracking down when issues were introduced  
- **Feature development** - Comparing branch differences before merging
- **History analysis** - Understanding project evolution over time

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Success!** Mastered Git diff commands through practical band lineup scenarios. These skills are essential for professional development workflows! 🎸 