# 🚀 Git & GitHub Study Notes & Quick Reference

> **Personal learning summary** - Essential version control commands and concepts

📅 **Updated:** August 12, 2025

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🎯 What is Git?

**Git** is a **version control system** that tracks and manages changes to files over time, allowing users to:
- ✅ Revisit earlier versions of files
- ✅ Compare changes between versions  
- ✅ Undo changes and restore previous states
- ✅ Collaborate with multiple developers
- ✅ Branch and merge code efficiently

### 📜 Brief History
In **2005**, **Linus Torvalds** (creator of Linux) became frustrated with available version control systems. They were:
- 🐌 **Slow** and inefficient
- 🔒 **Closed-source** and often paid
- ❌ **Limited** in functionality

He wanted a version control system that was **fast**, **free**, and **powerful**, so he created Git!

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 👥 Who Uses Git?

Git is used across **all industries** and **all skill levels**:

### 💻 **Technology Sector**
- **Tech Giants:** Facebook, Google, Microsoft, Apple
- **Startups:** From tiny teams to growing companies
- **Engineers & Developers:** Frontend, backend, mobile, data science

### 🎨 **Creative & Design**
- **Designers:** Managing design files and collaboration
- **Writers:** Drafting complex novels, screenplays, documentation
- **Content Creators:** Version control for creative projects

### 🏛️ **Government & Academia**
- **Government Agencies:** Managing law drafts and public documentation
- **Universities:** Research teams collaborating on projects
- **Open Source Communities:** Contributing to global projects

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🐙 GitHub vs Git

### **Git** (Version Control System)
- 🔧 **Core tool** for tracking file changes
- 💻 **Local** repository management
- 🖥️ **Command-line** based (primarily)

### **GitHub** (Cloud Service)
- ☁️ **Hosts** Git repositories in the cloud
- 🤝 **Collaboration** platform for teams
- 🌐 **Web interface** for Git operations
- 📊 **Additional features:** Issues, pull requests, project management

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚔️ Command Line vs GUI Tools

### 🖥️ **Command Line Interface**

#### ✅ **Pros:**
- **Consistency:** Commands are always the same across systems
- **Power:** Advanced Git features only available via command line
- **Speed:** Much faster once you become comfortable
- **Documentation:** All online resources refer to command-line
- **Universal:** Works on any system with Git installed

#### ❌ **Cons:**
- **Learning Curve:** Not beginner-friendly
- **Memory:** Difficult to remember commands initially
- **Intimidating:** Terminal interface can feel overwhelming

### 🖱️ **Graphical User Interface (GUI)**

#### ✅ **Pros:**
- **Visual Experience:** See changes and history graphically
- **User-Friendly:** Lower barrier of entry for beginners
- **Intuitive:** Point-and-click operations

#### ❌ **Cons:**
- **Inconsistency:** Interfaces vary across different GUI tools
- **Dependency:** Creates reliance on specific software
- **Limited Troubleshooting:** When things go wrong, hard to debug
- **Hidden Complexity:** "Magic" operations obscure Git's inner workings

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🖥️ Git Bash

**Git Bash** is a command-line interface widely used by developers that provides:
- 🐧 **Unix-style commands** on Windows
- 🚀 **Git integration** built-in
- 📁 **File navigation** and management
- 🔧 **Scripting capabilities**

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## ⚙️ Basic Configuration

**Git Log** - Get information about all commits:

```bash
git log
```

**Check Configuration:**

```bash
git config user.name    # Check if you have a name registered
git config user.email   # Check if you have an email registered
```

**Set Global Configuration:**

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@gmail.com"
```

<img src="purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 🔧 Basic Commands

**File Navigation:**

```bash
ls                           # List files and directories
ls -a                        # List all files (including hidden)
ls folder                    # List contents of specific folder
cd                           # Change directory
cd folder                    # Navigate to specific folder
cd ..                        # Go back one directory
pwd                          # Print working directory
clear                        # Clear terminal screen
open .                       # Open current directory (macOS)
start .                      # Open current directory (Windows)
```

**Git Operations:**

```bash
git --version                # Check Git version
git init                     # Initialize a new Git repository
git status                   # Check repository status
git add .                    # Add all changes to staging
git commit -m "Your message" # Commit with message
git log                      # View commit history
```

**File & Directory Management:**

```bash
touch text.txt                           # Create single file
touch test.py app.java archive.pdf       # Create multiple files
touch Documents/documentation.docx       # Create file in specific path
mkdir Folder                             # Create single directory
mkdir car bikes                          # Create multiple directories
rm text.txt                             # Remove single file
rm text.txt test.py app.java            # Remove multiple files
rm -rf foldername                       # Remove directory and contents
```

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📁 Git Repository Basics

**Repository (Repo):** A Git repository is a directory that contains your project files and the entire history of changes made to those files.

**Key Points:**

- 📂 Every project that uses Git needs a **Git repository**
- 🎯 Use `git init` to create a new repository in any project folder
- 📊 The repository tracks all file changes and maintains version history
- 🔄 One repository per project is the standard practice

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

## 📚 Key Reminders

- ✅ **Always commit with meaningful messages**
- ✅ **Pull before push** to avoid conflicts
- ✅ **Create branches** for new features
- ✅ **Review changes** before committing
- ✅ **Keep repositories organized** and documented
- ✅ **Practice command line** for better understanding
- ✅ **Backup important work** with regular pushes
- ⚠️ **Check with `git status`** to verify you're not initializing Git inside an existing repository

<img src="../purple-divisor.svg" width="100%" height="6" alt="Purple divider">

Git Branching
On large projects, we often work in multiple contexts:
1. You're working on 2 different color scheme variations for your website at the same time, unsure of which you like best
2. And also trying to fix a bug, but it is proving tough to solve
3. A teammate is also working on adding a new chat widget to present at the next meeting. it's unclear if your company will end up using it
4. Another coworker is updating the search bar autocomplete.
5. Another developer is doing an experimental radical design overhaul of the entire layout to present next month

Branches are alternative timelines for a project, they enable us to create separate contexts where we can try new things, or even work on multiple ideas in parallel.

If we make changes on one branch, they do not impact the other branches (unless we merge the changes)

> **Remember:** Git is not just about storing code, it's about **collaboration**, **history tracking**, and **professional development workflows**! 🚀
