PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp> cd "c:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise" ; git status
On branch current
Your branch is up to date with 'origin/current'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   fleetwoodmac.txt
        modified:   queen.txt

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git branch -a
* current
  remotes/origin/1970s
  remotes/origin/HEAD -> origin/current
  remotes/origin/current
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git restore .
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git switch 1970s
branch '1970s' set up to track 'origin/1970s'.
Switched to a new branch '1970s'
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git diff 1970s current
diff --git a/fleetwoodmac.txt b/fleetwoodmac.txt
index 6f44367..653b184 100644
--- a/fleetwoodmac.txt
+++ b/fleetwoodmac.txt
@@ -1,5 +1,5 @@
-Lead Vocals: Jeremy Spencer
-Lead Guitar: Lindsey Buckingham
+Lead Vocals: Stevie Nicks
+Lead Guitar: Mike Campbell
 Bass: John McVie
 Drums: Mick Fleetwood
-Keyboard: None
\ No newline at end of file
+Keyboard: Christine McVie
\ No newline at end of file
diff --git a/queen.txt b/queen.txt
index 2ab2d04..0e0fa0d 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Freddie Mercury
+Lead Vocals: Adam Lambert
 Lead Guitar: Brian May
-Bass: Mike Grose
+Bass: Neil Fairclough
 Drums: Roger Taylor
\ No newline at end of file
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git diff 1970s current queen.txt
diff --git a/queen.txt b/queen.txt
index 2ab2d04..0e0fa0d 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Freddie Mercury
+Lead Vocals: Adam Lambert
 Lead Guitar: Brian May
-Bass: Mike Grose
+Bass: Neil Fairclough
 Drums: Roger Taylor
\ No newline at end of file
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git switch current
Switched to branch 'current'
Your branch is up to date with 'origin/current'.
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git diff HEAD~1
diff --git a/queen.txt b/queen.txt
index f7f4a33..0e0fa0d 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
 Lead Vocals: Adam Lambert
 Lead Guitar: Brian May
-Bass: John Deacon
+Bass: Neil Fairclough
 Drums: Roger Taylor
\ No newline at end of file
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git add queen.txt
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git diff
diff --git a/fleetwoodmac.txt b/fleetwoodmac.txt
index 653b184..8c384c0 100644
--- a/fleetwoodmac.txt
+++ b/fleetwoodmac.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Stevie Nicks
+Lead Vocals: Stevie Chicks
 Lead Guitar: Mike Campbell
 Bass: John McVie
 Drums: Mick Fleetwood
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git diff --staged
diff --git a/queen.txt b/queen.txt
index 0e0fa0d..5f562c1 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Adam Lambert
+Lead Vocals: Vinicius Ares
 Lead Guitar: Brian May
 Bass: Neil Fairclough
 Drums: Roger Taylor
\ No newline at end of file
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> git diff HEAD
diff --git a/fleetwoodmac.txt b/fleetwoodmac.txt
index 653b184..8c384c0 100644
--- a/fleetwoodmac.txt
+++ b/fleetwoodmac.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Stevie Nicks
+Lead Vocals: Stevie Chicks
 Lead Guitar: Mike Campbell
 Bass: John McVie
 Drums: Mick Fleetwood
diff --git a/queen.txt b/queen.txt
index 0e0fa0d..5f562c1 100644
--- a/queen.txt
+++ b/queen.txt
@@ -1,4 +1,4 @@
-Lead Vocals: Adam Lambert
+Lead Vocals: Vinicius Ares
 Lead Guitar: Brian May
 Bass: Neil Fairclough
 Drums: Roger Taylor
\ No newline at end of file
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\GitDiffExercise\git-diff-exercise> 