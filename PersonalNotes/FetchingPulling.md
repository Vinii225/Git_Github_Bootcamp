git branch -r

remote branches
git switch <branch> to change to a remote branch in the repo

Fetching
git fetch <remote>
git fetch <remote> <branch>

Allows us to download changes from a remote repository, BUT those changes will not be automatically integrated into our working files

Pulling
git pull = git fetch + git merge
git pull <remote> <branch>

Pulls can result in merge conflicts!