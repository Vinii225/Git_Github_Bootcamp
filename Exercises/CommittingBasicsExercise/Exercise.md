# 🛒 Committing Basics Exercise

> **Hands-on practice** - Learning Git commit fundamentals through practical scenarios

📅 **Exercise Date:** July 31, 2025

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 Exercise Overview

This exercise focuses on mastering the basics of Git commits by creating and managing shopping lists. You'll practice:

- 📁 Repository initialization
- 📝 File creation and modification
- 📦 Staging specific changes
- 💬 Writing meaningful commit messages
- 📊 Viewing commit history

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📋 Step-by-Step Instructions

### 🚀 **Step 1-2: Repository Setup**

1. **Create a new folder** called `Shopping`
2. **Initialize a new git repo** inside the `Shopping` folder (make sure you're not already inside of a Git repo!)

> ⚠️ **Observation:** Not doing because I am already in a repo

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 📝 **Step 3-5: Initial File Creation**

1. **Make a new file** called `yard.txt`
2. **Make another new file** called `groceries.txt`
3. **Make a commit** that includes both empty files. The message should be:

   ```bash
   git commit -m "create yard and groceries lists"
   ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🌱 **Step 6-7: Adding Content to Files**

1. **In the `yard.txt` file**, add the following changes:

   ```text
   - 2 bags of potting soil
   - 1 bag of worm castings
   ```

2. **In the `groceries.txt` file**, add the following:

   ```text
   - 4 tomatoes
   - 6 shallots
   - 1 fennel bulb
   ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🥄 **Step 8-9: Selective Commits**

1. **Make a new commit**, including **ONLY the changes from the `groceries.txt` file.** The commit message should be:

   ```bash
   git commit -m "add ingredients for tomato soup"
   ```

2. **Make a second commit** including **ONLY the changes to the `yard.txt` file.** It should have the commit message:

   ```bash
   git commit -m "add items needed for garden box"
   ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 🥔 **Step 10-12: Final Modifications**

1. **Add the following line** to the end of `groceries.txt`:

    ```text
    - couple of seed potatos
    ```

2. **In the `yard.txt` file**, change the first line so that it says "**3** bags of potting soil" instead of "2 bags of potting soil":

    ```text
    - 3 bags of potting soil
    - 1 bag of worm castings
    ```

3. **Make a commit that includes the changes to BOTH files.** The message should read:

    ```bash
    git commit -m "add items needed to grow potatoes"
    ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

### 📊 **Step 13: Verify Your Work**

1. **Use a Git command to display a list of the commits. You should see 4!**

    ```bash
    git log 
    ```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ✅ Expected Results

After completing this exercise, you should have:

- 🏗️ **4 total commits** in your repository
- 📄 **2 files** (`yard.txt` and `groceries.txt`) with content
- 🎯 **Experience** with selective staging and committing
- 📝 **Practice** writing descriptive commit messages

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

> **Remember:** This exercise demonstrates the power of Git's **selective staging** - you can choose exactly which changes to include in each commit! 🚀