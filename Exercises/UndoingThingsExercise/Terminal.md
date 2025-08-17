PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp> ls 


    Diretório: C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
dar--l        17/08/2025     02:05                Exercises
dar--l        17/08/2025     00:38                PersonalNotes
-a---l        31/07/2025     06:25              0 .gitignore
-a---l        13/07/2025     19:51            816 purple-divisor.svg
-a---l        17/08/2025     02:28           9984 README.md


PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp> cd Exercises
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises> ls


    Diretório: C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
dar--l        17/08/2025     00:14                BranchingExercise
dar--l        31/07/2025     06:48                CommittingBasicsExercise
dar--l        17/08/2025     00:14                GitDiffExercise
dar--l        17/08/2025     00:14                GitMergingExercise
dar--l        17/08/2025     00:23                StashingExercise
dar--l        17/08/2025     02:09                UndoingThingsExercise


PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises> cd UndoingThingsExercise
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise> git clone https://github.com/Colt/yesterday-exercise
Cloning into 'yesterday-exercise'...
remote: Enumerating objects: 24, done.
remote: Counting objects: 100% (24/24), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 24 (delta 7), reused 24 (delta 7), pack-reused 0 (from 0)
Receiving objects: 100% (24/24), done.
Resolving deltas: 100% (7/7), done.
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise> ls


    Diretório: C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
dar--l        17/08/2025     14:47                yesterday-exercise
-a---l        17/08/2025     02:22           8938 Exercise.md
-a---l        17/08/2025     02:09              0 Terminal.md


PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise> cd ^C
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise> cd yesterday-exercise
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git log --oneline
f199959 (HEAD -> master, origin/master, origin/HEAD) rework final verse
8e3111c rework chorus
b88b254 rework second verse
b593444 rework first verse
cdd927c finish original lyrics
9518e20 add original chorus
9858f43 add original second verse
485a339 add original first verse
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git checkout 485a339
Note: switching to '485a339'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at 485a339 add original first verse
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git switch main
fatal: invalid reference: main
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git checkout main
error: pathspec 'main' did not match any file(s) known to git
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git branch
* (HEAD detached at 485a339)
  master
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git switch master
Previous HEAD position was 485a339 add original first verse
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git checkout cdd927c
Note: switching to 'cdd927c'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at cdd927c finish original lyrics
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git switch -c scrambled-eggs
Switched to a new branch 'scrambled-eggs'
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git switch master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git restore lyrics.txt
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git add .
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git commit -m "new lyrics"
[master 838cf09] new lyrics
 1 file changed, 7 insertions(+), 17 deletions(-)
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git -a -m "bottom part added"
unknown option: -a
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-lazy-fetch]
           [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>]
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]
           <command> [<args>]
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git -am "bottom part added"
unknown option: -am
usage: git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--no-lazy-fetch]
           [--no-optional-locks] [--no-advice] [--bare] [--git-dir=<path>]
           [--work-tree=<path>] [--namespace=<name>] [--config-env=<name>=<envvar>]
           <command> [<args>]
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git add .
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git commit -m "bottom part added"
[master c7be2e6] bottom part added
 1 file changed, 10 insertions(+), 1 deletion(-)
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git reset HEAD~2 
Unstaged changes after reset:
M       lyrics.txt
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git switch -c 404
Switched to a new branch '404'
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git add add lyrics.txt
fatal: pathspec 'add' did not match any files
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git add lyrics.txt    
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git commit -m "404 lyrics"       
[404 7f7f4bd] 404 lyrics
 1 file changed, 15 insertions(+), 16 deletions(-)
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> git switch master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> cd .
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise\yesterday-exercise> cd ..
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises\UndoingThingsExercise> cd ..
PS C:\Users\vinic\OneDrive\Documentos\Git_Github_Bootcamp\Exercises> cd ..