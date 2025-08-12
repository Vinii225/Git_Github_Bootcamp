# 🌿 Branching Exercise - Harry Potter Patronus

> **Hands-on practice** - Learning Git branching fundamentals with magical themes

📅 **Exercise Date:** August 12, 2025

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Overview

This exercise focuses on mastering Git branching by creating different Patronus files for Harry Potter characters. You'll practice:
- 📁 Repository initialization 
- 🌿 Creating multiple branches
- 🔄 Switching between branches
- 📝 Making branch-specific commits
- 👀 Viewing branch lists
- 🗑️ Deleting branches

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📋 Step-by-Step Instructions

### 🚀 **Step 1-4: Repository Setup**

1. **Make a new folder** called `Patronus`
2. **Make a new git repo** inside the folder (make sure you're not in an existing repo)
3. **Create a new file** called `patronus.txt` (leave it empty for now)
4. **Add and commit** the empty file, with the message:
   ```bash
   git commit -m "add empty patronus file"
   ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🌿 **Step 5-6: Creating Branches**

5. **Create two new branches** called `harry` and `snape` (both based on the master branch):
   ```bash
   git branch harry
   git branch snape
   ```

6. **Move to the `harry` branch** using the "new" command to change branches:
   ```bash
   git switch harry
   ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🦌 **Step 7-8: Harry's Stag Patronus**

7. **In the `patronus.txt` file**, add the following:

   ```text
   HARRY'S PATRONUS
   
      /|       |\
   `__\\       //__'
      ||      ||
    \__`\     |'__/
      `_\\   //_'
      _.,:---;,._
      \_:     :_/
        |@. .@|
        |     |
        ,\.-./ \
        ;;`-'   `---__________-----.-.
        ;;;                         \_\
        ';;;                         |
         ;    |                      ;
          \   \     \        |      /
           \_, \    /        \     |\
             |';|  |,,,,,,,,/ \    \ \_
             |  |  |           \   /   |
             \  \  |           |  / \  |
              | || |           | |   | |
              | || |           | |   | |
              | || |           | |   | |
              |_||_|           |_|   |_|
             /_//_/           /_/   /_/
   ```

8. **Add and commit** the changes, with the commit message:
   ```bash
   git commit -m "add harry's stag patronus"
   ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🦌 **Step 9-11: Snape's Doe Patronus**

9. **Move over to the `snape` branch** using the "older" command to change branches:
   ```bash
   git checkout snape
   ```

10. **Put the following text** in the `patronus.txt` file:

    ```text
    SNAPE'S PATRONUS
                          .     _,
                          |`\__/ /
                          \  . .(
                           | __T|
                          /   |
             _.---======='    |
            //               {}
           `|      ,   ,     {}
            \      /___;    ,'
             ) ,-;`    `\  //
            | / (        ;||
            ||`\\        |||
            ||  \\       |||
            )\   )\      )||
            `"   `"      `""
    ```

11. **Add and commit** the changes on the `snape` branch with the commit message:
    ```bash
    git commit -m "add snape's doe patronus"
    ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🌸 **Step 12-15: Lily's Doe Patronus**

12. **Create a new branch** based upon the `snape` branch called `lily`:
    ```bash
    git branch lily
    ```

13. **Move to the `lily` branch**:
    ```bash
    git switch lily
    ```

14. **Edit the `patronus.txt` file** so that it says `LILY'S PATRONUS` at the top instead of `SNAPE'S PATRONUS` (leave the doe ascii-art alone)

15. **Add and commit** the change with the message:
    ```bash
    git commit -m "add lily's doe patronus"
    ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 📊 **Step 16-17: Branch Management**

16. **Run a git command** to list all branches (you should see 4):
    ```bash
    git branch
    ```

17. **Bonus: Delete the `snape` branch** (poor Snape):
    ```bash
    git branch -d snape
    ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ✅ Expected Results

After completing this exercise, you should have:
- 🏗️ **4 branches created** (`main`, `harry`, `snape`, `lily`)
- 📄 **Different file content** on each branch
- 🎯 **Experience** with branch creation and switching
- 📝 **Practice** with branch-specific commits
- 🗑️ **Knowledge** of branch deletion

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔧 Key Commands Used

```bash
git branch branch-name                        # Create new branch
git branch                                   # List all branches
git switch branch-name                       # Switch to branch (new command)
git checkout branch-name                     # Switch to branch (older command)
git branch -d branch-name                    # Delete branch (safe)
git branch -D branch-name                    # Delete branch (force)
git commit -m "message"                      # Commit with message
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Remember:** This exercise demonstrates **branch isolation** - each branch maintains its own version of files independently! ⚡✨