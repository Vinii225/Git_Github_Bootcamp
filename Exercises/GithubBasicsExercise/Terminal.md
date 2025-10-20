# 💻 GitHub Basics Exercise - Terminal Session

> **Real terminal commands and outputs** - Step-by-step execution of the GitHub favorites exercise

📅 **Exercise Completed:** October 20, 2025  
👤 **Author:** Vinícius Ares  
📧 **Email:** vinicius.ares12@gmail.com

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Overview

This document shows the actual terminal commands executed during the GitHub Basics Exercise, demonstrating remote repository operations, pushing branches, and merge conflict resolution.

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📄 Step 1: Initial Commit - Empty Favorites File

**First attempt (forgot to stage):**
```powershell
git commit -m "add empty favorites file"
```

**Git response:**
```
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Exercises/GithubBasicsExercise/favorites.txt

nothing added to commit but untracked files present (use "git add" to track)
```

**Corrected commands:**
```powershell
git add .
git commit -m "add empty favorites file"
```

**Git response:**
```
[main d802630] add empty favorites file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 Exercises/GithubBasicsExercise/favorites.txt
```

**Analysis:**
- ❌ **Common mistake** - Forgot to stage files before committing
- ✅ **Fixed immediately** - Added files and committed successfully
- 📊 **Empty file** - 0 insertions/deletions as expected

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📤 Step 2: First Push to GitHub

**Command executed:**
```powershell
git push
```

**Git response:**
```
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 431 bytes | 431.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Vinii225/Git_Github_Bootcamp
   8310b1c..d802630  main -> main
```

**Analysis:**
- ✅ **Push successful** - Main branch synced with GitHub
- 🚀 **Compression** - Git optimized data transfer
- 🔗 **Remote updated** - GitHub now has the empty favorites file

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🌿 Step 3: Creating Feature Branches

**Commands executed:**
```powershell
git branch foods
git branch movies
git branch
```

**Git response:**
```
  foods
* main
  movies
```

**Analysis:**
- ✅ **Two branches created** - `foods` and `movies`
- 🎯 **Current branch** - Still on `main` (marked with *)
- 📊 **Ready for parallel work** - Can now work on different features

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🍕 Step 4: Adding Favorite Foods

**Commands executed:**
```powershell
git switch foods
git add favorites.txt
```

**Git response:**
```
Switched to branch 'foods'
fatal: pathspec 'favorites.txt' did not match any files
```

**Problem debugging:**
```powershell
ls
cd Exercises
ls
cd ..
```

**Directory structure revealed - needed correct path!**

**Corrected commands:**
```powershell
git add .
git commit -m "add favorite foods"
```

**Git response:**
```
[foods 3953cda] add favorite foods
 1 file changed, 3 insertions(+)
```

**Analysis:**
- ❌ **Path error** - File wasn't in current directory
- 🔍 **Debugging** - Used `ls` to check directory structure
- ✅ **Fixed** - Used `git add .` to stage all changes
- 📝 **3 foods added** - 3 insertions recorded

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎬 Step 5: Adding Favorite Movies

**Commands executed:**
```powershell
git switch moveis  # Typo!
git switch movies  # Fixed
git add .
git commit -m "add favorite movies"
```

**Git response:**
```
fatal: invalid reference: moveis
Switched to branch 'movies'
[movies 15d056c] add favorite movies
 1 file changed, 3 insertions(+)
```

**Analysis:**
- ❌ **Typo** - Accidentally typed "moveis" instead of "movies"
- ✅ **Quick fix** - Corrected and switched successfully
- 📝 **3 movies added** - 3 insertions recorded
- 🎯 **Branch isolation** - Changes only on `movies` branch

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📤 Step 6: Pushing Foods Branch to GitHub

**Command executed:**
```powershell
git push origin foods
```

**Git response:**
```
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 419 bytes | 419.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
remote:
remote: Create a pull request for 'foods' on GitHub by visiting:
remote:      https://github.com/Vinii225/Git_Github_Bootcamp/pull/new/foods
remote:
To https://github.com/Vinii225/Git_Github_Bootcamp
 * [new branch]      foods -> foods
```

**Analysis:**
- ✅ **New remote branch** - `foods` now exists on GitHub
- 🔗 **Pull request suggestion** - GitHub offers PR creation link
- 📊 **Efficient transfer** - Delta compression optimized upload

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📤 Step 7: Pushing Movies Branch to GitHub

**Command executed:**
```powershell
git push origin movies
```

**Git response:**
```
Enumerating objects: 9, done.
Counting objects: 100% (9/9), done.
Delta compression using up to 12 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 450 bytes | 450.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
remote:
remote: Create a pull request for 'movies' on GitHub by visiting:
remote:      https://github.com/Vinii225/Git_Github_Bootcamp/pull/new/movies
remote:
To https://github.com/Vinii225/Git_Github_Bootcamp
 * [new branch]      movies -> movies
```

**Analysis:**
- ✅ **Second remote branch** - `movies` now exists on GitHub
- 🌐 **GitHub visibility** - All 3 branches visible on GitHub
- 🎯 **Parallel features** - Both features pushed independently

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔀 Step 8: Merging Foods Branch (Fast-Forward)

**Commands executed:**
```powershell
git switch main
git merge foods
```

**Git response:**
```
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
Updating d802630..3953cda
Fast-forward
 Exercises/GithubBasicsExercise/favorites.txt | 3 +++
 1 file changed, 3 insertions(+)
```

**Analysis:**
- ✅ **Fast-forward merge** - No merge commit needed
- 📈 **Linear history** - Main simply caught up to foods
- 🎯 **Clean merge** - No conflicts, as expected

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚠️ Step 9: Merging Movies Branch (CONFLICT!)

**Command executed:**
```powershell
git merge movies
```

**Git response:**
```
Auto-merging Exercises/GithubBasicsExercise/favorites.txt
CONFLICT (content): Merge conflict in Exercises/GithubBasicsExercise/favorites.txt
Automatic merge failed; fix conflicts and then commit the result.
```

**Analysis:**
- ⚠️ **Merge conflict detected** - Both branches modified same file
- 🔍 **Same file, same location** - Both added content to `favorites.txt`
- 🛠️ **Manual resolution needed** - Must edit file and choose what to keep
- 📝 **Next step** - Open file, resolve conflicts, then commit

**Expected conflict markers in `favorites.txt`:**
```
<<<<<<< HEAD
Pizza
Sushi
Tacos
=======
The Matrix
Inception
Interstellar
>>>>>>> movies
```

**Resolution steps:**
1. Open `favorites.txt`
2. Remove conflict markers
3. Keep both foods and movies
4. Stage the file: `git add .`
5. Commit: `git commit -m "merge foods and movies branches"`
6. Push to GitHub: `git push origin main`

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎓 Key Learnings from This Session

- 📂 **File paths matter** - Always check you're in the right directory
- 🔤 **Typos happen** - Git will catch invalid branch names
- ✅ **Stage before commit** - Common beginner mistake to forget `git add`
- 🚀 **Push creates remote branches** - `origin branch` publishes branches
- ⚡ **Fast-forward merges** - Happen when no divergent commits exist
- ⚠️ **Merge conflicts** - Inevitable when editing same file in different branches
- 🌐 **GitHub integration** - Seamless push/pull with remote repository

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔧 Commands Used in This Session

```powershell
git add .                               # Stage all changes
git commit -m "message"                 # Commit with message
git push                                # Push to default remote
git push origin branch-name             # Push specific branch
git branch branch-name                  # Create new branch
git switch branch-name                  # Switch to branch
git merge branch-name                   # Merge branch into current
ls                                      # List directory contents (PowerShell)
cd                                      # Change directory
```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🏆 Exercise Status

- ✅ **Repository created** and connected to GitHub
- ✅ **Initial file** committed and pushed
- ✅ **Two feature branches** created (`foods`, `movies`)
- ✅ **Content added** to both branches
- ✅ **Both branches pushed** to GitHub
- ✅ **First merge** completed (fast-forward)
- ⏸️ **Second merge** awaiting conflict resolution

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Almost there!** This terminal session demonstrates the complete **GitHub workflow** including the reality of **merge conflicts**! 🚀⚡
