# 🔀 Git Merging Exercise - Terminal Session

> **Practical session** demonstrating Fast-Forward Merge, Merge Commits, and Merge Conflicts

📅 **Date:** August 15, 2025  
🎯 **Objective:** Practice different Git merge scenarios with real examples

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚡ Part 1: Fast-Forward Merge

### 🎯 **Scenario:** Create branch, add content, merge back to main

```powershell
# Check initial status
PS > git status
On branch main
Your branch is up to date with 'origin/main'.
nothing to commit, working tree clean

# Create and switch to new branch
PS > git switch -c musics
Switched to a new branch 'musics'

PS > git branch
  main
* musics

# Add new file with rock songs
PS > git add GitMergingExercise\Musics\rock.txt
PS > git commit -m "Add of rock musics in text file"
[musics 6100907] Add of rock musics in text file
 1 file changed, 5 insertions(+)
 create mode 100644 GitMergingExercise/Musics/rock.txt

# Push to remote
PS > git push origin musics
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 572 bytes | 572.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Vinii225/Git-Github_Bootcamp
 * [new branch]      musics -> musics

# Switch back to main and merge
PS > git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

PS > git merge musics
Updating 902ec24..6100907
Fast-forward                    # ← FAST-FORWARD MERGE SUCCESS! ⚡
 GitMergingExercise/Musics/rock.txt | 5 +++++
 1 file changed, 5 insertions(+)
 create mode 100644 GitMergingExercise/Musics/rock.txt
```

### ✅ **Result:** Fast-Forward merge completed - no merge commit created!

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔗 Part 2: Setting Up for Merge Conflict

### 🎯 **Scenario:** Create conflicting changes on different branches

```powershell
# Clean up old branches and create new one
PS > git branch -d lua musics
Deleted branch lua (was e4755e9).
Deleted branch musics (was 6100907).

# Create pop-music branch and modify same file
PS > git switch -c pop-music
Switched to a new branch 'pop-music'

# Modify rock.txt with pop songs
PS > git add GitMergingExercise/Musics/rock.txt
PS > git commit -m "Add of pop-music"
[pop-music 4977488] Add of pop-music
 1 file changed, 3 insertions(+), 6 deletions(-)

PS > git push origin pop-music
To https://github.com/Vinii225/Git-Github_Bootcamp
 * [new branch]      pop-music -> pop-music

# Switch to main and modify SAME FILE differently
PS > git switch main
Switched to branch 'main'

# Edit same file with metal songs
PS > git add GitMergingExercise/Musics/rock.txt
PS > git commit -m "Add metal songs to rock.txt"
[main 3c50c84] Add metal songs to rock.txt
 1 file changed, 1 insertion(+), 2 deletions(-)

PS > git push
To https://github.com/Vinii225/Git-Github_Bootcamp
   6100907..3c50c84  main -> main
```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚠️ Part 3: Merge Conflict Resolution

### 🎯 **Scenario:** Attempt merge and resolve conflict

```powershell
# Attempt to merge - CONFLICT OCCURS! 🔥
PS > git merge pop-music
Auto-merging GitMergingExercise/Musics/rock.txt
CONFLICT (content): Merge conflict in GitMergingExercise/Musics/rock.txt
Automatic merge failed; fix conflicts and then commit the result.
```

### 🚨 **Conflict Detected!**

**What happened:**
- Both `main` and `pop-music` branches modified the same file
- Git cannot automatically decide which changes to keep
- Manual intervention required to resolve conflicts

### 🔧 **Next Steps to Resolve:**

```powershell
# 1. Check status
git status

# 2. Open GitMergingExercise/Musics/rock.txt
# 3. Look for conflict markers:
#    <<<<<<< HEAD
#    (main branch content)
#    =======
#    (pop-music branch content)
#    >>>>>>> pop-music

# 4. Edit file to resolve conflicts
# 5. Remove conflict markers
# 6. Stage resolved file
git add GitMergingExercise/Musics/rock.txt

# 7. Complete merge
git commit -m "Resolve merge conflict in rock.txt"
```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Summary

### ✅ **Completed Successfully:**

1. **⚡ Fast-Forward Merge** - Linear history, no merge commit
2. **🔗 Merge Setup** - Created divergent branches  
3. **⚠️ Merge Conflict** - Successfully triggered conflict scenario

### 📚 **Key Learnings:**
- **Fast-forward merges** happen when target branch hasn't changed
- **Merge conflicts** occur when same lines are modified differently
- **Conflict resolution** requires manual editing and staging

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Next Step:** Resolve the merge conflict by editing the rock.txt file and completing the merge! 🚀
