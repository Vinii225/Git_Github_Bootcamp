# 📦 Git Stashing Exercise - Terminal Session

> **Practical terminal session** demonstrating Git stash for emergency context switching

📅 **Date:** August 17, 2025  
🎯 **Objective:** Master Git stash through workplace drama scenario with real commands

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📂 Part 1: Initial Setup & Professional Content

### 💾 **Initial Diary Creation**

```powershell
# Add and commit initial professional diary entry
PS > git add StashingExercise/Diary/diary.txt
PS > git commit -m "Add diary and comment about my boss"
[main ff3d1c0] Add diary and comment about my boss
 1 file changed, 1 insertion(+)
 create mode 100644 StashingExercise/Diary/diary.txt

# Push to remote repository
PS > git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 465 bytes | 465.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Vinii225/Git-Github_Bootcamp
   5535b76..ff3d1c0  main -> main
```

**✅ Result:** Professional diary entry safely committed and pushed to remote

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🌿 Part 2: Truth Branch Creation & Honest Thoughts

### 🔀 **Create Truth Branch**

```powershell
# Create new branch for honest thoughts
PS > git switch -c the-truth
Switched to a new branch 'the-truth'
```

### ✏️ **Modify Diary with True Feelings**

*[User edited diary.txt to contain honest negative thoughts about boss]*

### 🚨 **Emergency: Boss Approaching!**

```powershell
# Attempt to quickly switch back to main branch
PS > git switch main
M       StashingExercise/Diary/diary.txt        # ← Git detects uncommitted changes!
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```

**⚠️ Crisis:** Uncommitted changes follow you to main branch! Boss might see!

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📦 Part 3: Emergency Stash Operation

### 🔥 **Quick Stash to Hide Evidence**

```powershell
# Emergency stash to hide honest thoughts
PS > git stash
Saved working directory and index state WIP on main: ff3d1c0 Add diary and comment about my boss
```

**✅ Success:** Honest thoughts safely hidden in stash!

### 😇 **Add Professional Content While Boss Watches**

```powershell
# Add more professional lies to impress boss
PS > git add StashingExercise/Diary/diary.txt
PS > git commit -m "Add more comments on diary"
[main 06eae2c] Add more comments on diary
 1 file changed, 2 insertions(+)

# Push professional content to remote
PS > git push
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 462 bytes | 462.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Vinii225/Git-Github_Bootcamp
   ff3d1c0..06eae2c  main -> main
```

**🎭 Boss Status:** Impressed with dedication and positive attitude!

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🕵️ Part 4: Return to Truth & Stash Recovery

### 🔄 **Coast is Clear - Return to Truth Branch**

```powershell
# Switch back to truth branch
PS > git switch the-truth
Switched to branch 'the-truth'
```

### 📦 **Retrieve Hidden Thoughts from Stash**

```powershell
# Pop stashed changes to restore honest thoughts
PS > git stash pop
On branch the-truth
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   StashingExercise/Diary/diary.txt

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (7a881eead2dfb95307b464f680c6e5eb7bc10b21)
```

**✅ Success:** Honest thoughts restored! Stash automatically removed after pop.

### 💾 **Commit the Truth**

```powershell
# Commit honest thoughts on truth branch
PS > git add StashingExercise/Diary/diary.txt
PS > git commit -m "Add negative comments on my boss"
[the-truth 4fe8b4d] Add negative comments on my boss
 1 file changed, 5 insertions(+), 1 deletion(-)
```

### 🚀 **Push Truth Branch to Remote**

```powershell
# First push attempt shows upstream branch setup needed
PS > git push
fatal: The current branch the-truth has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin the-truth

# Set upstream and push truth branch
PS > git push origin the-truth
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 466 bytes | 466.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'the-truth' on GitHub by visiting:
remote:      https://github.com/Vinii225/Git-Github_Bootcamp/pull/new/the-truth
remote:
To https://github.com/Vinii225/Git-Github_Bootcamp
 * [new branch]      the-truth -> the-truth
```

**🎯 Final Success:** Truth branch created and pushed with honest thoughts!

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Summary

### ✅ **Mission Accomplished:**

1. **📝 Professional facade maintained** - Boss saw only positive content
2. **📦 Emergency stash successful** - Honest thoughts safely hidden
3. **🔄 Context switching mastered** - Seamless branch transitions
4. **💾 Dual reality created** - Two different versions of truth
5. **🚀 Remote synchronization** - Both branches pushed to GitHub

### 🔧 **Git Commands Successfully Demonstrated:**

```bash
git stash                         # Emergency save of uncommitted work
git stash pop                     # Retrieve and remove from stash
git switch -c branch-name         # Create and switch to new branch
git switch branch-name            # Switch between existing branches
git push origin branch-name       # Push new branch to remote
```

### 📚 **Key Learning Outcomes:**

- **🚨 Emergency workflows** - Quick response to interruptions
- **📦 Temporary storage** - Stash as intermediate workspace
- **🌿 Branch isolation** - Keeping different work contexts separate
- **🔄 Context switching** - Managing multiple work streams
- **🎭 Professional development** - Handling workplace scenarios

### 🌟 **Real-World Applications:**

This exercise demonstrates essential skills for:
- **Urgent bug fixes** during feature development
- **Code reviews** requiring clean working directory
- **Meeting interruptions** during active coding
- **Experimental work** that needs temporary hiding
- **Multi-tasking** in professional environments

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Success!** Mastered Git stash through workplace drama. These **emergency context switching** skills are essential for professional development! 🎭