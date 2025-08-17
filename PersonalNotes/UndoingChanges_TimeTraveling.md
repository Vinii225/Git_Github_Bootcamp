git checkout
is like a git swiss army knife, many devs thinks it is overloaded, which is what lead to the addition of the git switch and git restore commands

we can use checkout to create branches, switch to new branhces, restore files and undo history!

git checkout commit-hash 
view a previous commit
remember of git log to view commit hashes (we need the first 7 digits of a commit hash)

detached HEAD:
Look around, make experimental changes, commit and you can discard any commits you make in this state without impacting any branches by switching back to a branch

HEAD is a pointer to a branch reference
The branch reference is a pointer to the last commit made on a particular branch

when we make a new commit, the branch pointer is updated to reflect the new commit
**the HEAD remains the same, because it's pointing at the branch reference**
when you switch branches, head is pointing at the bugfix reference
when we checkout a particular commit, HEAD points at that commit rather than at the branch pointer

DETACHED HEAD
1. examine content
2. leave and go back to wherever you were before - reattach the HEAD
git switch master/main
3. create a new branch and switch to it. You can now make and save changes, since HEAD is no longer detached
git switch -c new-branch

git checkout HEAD~1
refers to the commit before HEAD (parent)
the number means how many commits

git checkout -
go back to previous branch

Discard Changes
Suppose you've mande changes to a file but don't want to keep them, to revert the file back to whatever it looked like when you last committed, you can use
git checkout HEAD file-name
shorter version is git checkout -- file-name

Unmodifying Files with restore
git restore file-name
Suppose you've made some changes to a file since your last commit. You've saved the file but then realize you definitely do not want those changes anymore!

git checkout HEAD file-name and git restore file-name works the same

NOTE: the command above is not "undoable" if you have uncommited changes in the file, they will be lost!

git restore --source HEAD~1 file-name
restores using HEAD as the default source, but we can change that using the --source option. For example the above command will restore the contents of file-name to its state prior to HEAD. You can also use a particular commit hash as the source

Unstaging Files with Restore
If you have accidentaly added a file to your staging area with git add and you don't wish to include it in the next commit, you can use git restore to remove it from staging
git restore --staged file-name

Git Reset 
You made a couple of commits on the branch but you actually meant them on a separate branch instead. To undo those commits, you can use git reset
git reset commit-hash
This will reset the repo back to a specific commit. The commits are gone

If you want to undo both the commits and the actual changes in your files, you can use the --hard option
git reset --hard commit
This will delete the last commit and associated changes

Git Revert
creates a new commit which reverses/undos the changes from a commit. Because it results in a new commit, you will be prompted to enter a commit message.
git revert commit-hash

Which Should I Use?
If you want to reverse some commits that other people already have on their machines, you should use revert
If you want to reverse commit that you haven't shared with others, use reset and no one will ever know!