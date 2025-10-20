# 🌐 GitHub Basics Exercise

> **Hands-on practice** - Master GitHub fundamentals through remote repositories, pushing, pulling, and branch management

📅 **Exercise Date:** October 20, 2025

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Overview

This exercise focuses on mastering GitHub operations by creating a favorites list project. You'll practice:

- 📁 Local and remote repository creation
- 🔗 Connecting local repos to GitHub
- 📤 Pushing branches to remote
- 🌿 Working with multiple branches remotely
- 🔀 Merging branches with conflict resolution
- 🔄 Syncing local and remote repositories

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📋 Step-by-Step Instructions

### 🚀 **Step 1-3: Initial Setup**

1. **Create a new repository locally** on your machine

   ```bash

   mkdir favorites-project
   cd favorites-project
   git init
   ```

2. **Create a new GitHub repository**
   - Go to GitHub.com
   - Click "New Repository"
   - Name it whatever you want (e.g., `favorites-project`)
   - **Don't** initialize with README, .gitignore, or license

3. **Connect your local repo to the GitHub repo**

   ```bash

   git remote add origin <your-github-repo-url>
   ```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🏷️ **Step 4-6: First Commit and Push**

4. **Optional: Rename the default branch** from `master` to `main`

   ```bash

   git branch -m main
   ```

5. **Make a new file** called `favorites.txt` (leave it empty). Make your first commit on the `main` branch

   ```bash

   touch favorites.txt
   git add favorites.txt
   git commit -m "add empty favorites file"
   ```

6. **Push up your `main` branch to GitHub!** Make sure you see your empty `favorites.txt` file on GitHub

   ```bash

   git push -u origin main
   ```

   **Verify:** Check GitHub - you should see the `favorites.txt` file

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🌿 **Step 7-9: Creating Feature Branches**

7. **Create two branches:** `foods` and `movies`

   ```bash

   git branch foods
   git branch movies
   ```

8. **Switch to the `foods` branch.** Add three (or more) of your favorite foods to the `favorites.txt` file. Add and commit your changes on the `foods` branch

   ```bash

   git switch foods
   # Edit favorites.txt and add your favorite foods:
   # - Pizza
   # - Sushi
   # - Tacos
   git add favorites.txt
   git commit -m "add favorite foods"
   ```

9. **Switch to the `movies` branch** and add three or more of your favorite movies to the `favorites.txt` file. Add and commit your changes on the `movies` branch

   ```bash

   git switch movies
   # Edit favorites.txt and add your favorite movies:
   # - The Matrix
   # - Inception
   # - Interstellar
   git add favorites.txt
   git commit -m "add favorite movies"
   ```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 📤 **Step 10-11: Pushing Branches to GitHub**

10. **Push up your `foods` branch to GitHub.** Make sure you see it on GitHub!

    ```bash

    git push -u origin foods
    ```

    **Verify:** Check GitHub - you should see the `foods` branch in the branches dropdown

11. **Push up your `movies` branch to GitHub.** Make sure you see it on GitHub!

    ```bash

    git push -u origin movies
    ```

    **Verify:** Check GitHub - you should see the `movies` branch in the branches dropdown

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🔀 **Step 12-13: Merging and Final Push**

12. **Merge the `foods` branch into the `main` branch.** Then merge the `movies` branch into the `main` branch. If necessary, resolve conflicts so that you end up with your favorite foods and favorite movies in the same `favorites.txt` file

    ```bash

    git switch main
    git merge foods
    git merge movies
    ```

    **⚠️ Note:** You will likely encounter a **merge conflict**! Both branches modified the same file.

    **To resolve:**
    - Open `favorites.txt`
    - Remove conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
    - Keep both your foods and movies in the file
    - Save the file

    ```bash

    git add favorites.txt
    git commit -m "merge foods and movies branches"
    ```

13. **Push up the latest work on your `main` branch to GitHub**

    ```bash

    git push origin main
    ```

    **Verify:** Check GitHub - your `main` branch should now contain both foods and movies!

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ✅ Expected Results

After completing this exercise, you should have:

- 🏗️ **1 local repository** connected to GitHub
- 🌐 **1 GitHub repository** with 3 branches (`main`, `foods`, `movies`)
- 📄 **`favorites.txt` file** with both foods and movies on `main` branch
- 🎯 **Experience** with pushing and pulling from GitHub
- 📝 **Practice** resolving merge conflicts
- 🔗 **Understanding** of remote repository workflows

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔧 Key Commands Used

```bash
git init                                      # Initialize local repository
git remote add origin <url>                   # Connect to GitHub
git branch -m main                            # Rename branch
git push -u origin branch-name                # Push and set upstream
git switch branch-name                        # Switch branches
git merge branch-name                         # Merge branches
git push origin branch-name                   # Push branch to GitHub
```

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 💡 Key Concepts Reinforced

- **🔗 Remote connections** - Linking local repos to GitHub
- **📤 Push operations** - Sending local commits to remote
- **🌿 Remote branch management** - Creating and pushing feature branches
- **🔀 Merge conflicts** - Resolving conflicting changes
- **🔄 Synchronization** - Keeping local and remote in sync

<img src="../../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Remember:** This exercise demonstrates the complete **GitHub workflow** - from local development to remote collaboration! 🚀
