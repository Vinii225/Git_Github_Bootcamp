git clone <url>

make sure you are not inside of a repo before cloning and you can clone also non-github repos

Register SSH key
without it, Github will prompt you every single time for your github email and password
Once configured you can connect to Github without having to supply your username/password

https://docs.github.com/pt/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

Once generated, cd to the .ssh key directory and cat the .pub version

Options
Existing Repo
If you already have an existing repo locally that you want to get on Github
- Create a new repo on Github
- Connect your local repo (add a remote)
- Push up your changes to Github

Start From Scratch
if you haven't begun work on your local repo, you can
- Create a brand new repo on Github
- Clone it down to your machine
- Do some work locally
- Push up your changes to Github

git remote -v
git remote add origin <url>

origin is a convetional Git remote name, but it is not all special. It's a name for a URL. the default remote name setup for us is called origin. You can change it. Most people leave it.

git remote rename <old> <new>
git remote remove <name>

git push <remote> <branch>

Push in detail:
To push our local developer branch up to a remote branch called hotfix we could do:
git push origin developer:hotfix

The -u option
the -u option allows us to set the upstram of the branch we are pushing. You can think of this as a link connecting our local branch to a branch on Github.
Running git push -u origin master sets the upstream of the local master branch so that it tracks the master branch on the origin repo
In the next time we push we can simply trype:
git push