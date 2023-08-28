PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git remote -v
origin  https://github.com/nnja/advanced-git-exercises (fetch)
origin  https://github.com/nnja/advanced-git-exercises (push)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git remote rename origin upstream
Renaming remote references: 100% (11/11), done.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git remote -v
upstream        https://github.com/nnja/advanced-git-exercises (fetch)
upstream        https://github.com/nnja/advanced-git-exercises (push)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout master
Already on 'master'
Your branch is ahead of 'upstream/master' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git remote add origin https://github.com/folivoramanh/advanced-git-exercises
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git remote -v
origin  https://github.com/folivoramanh/advanced-git-exercises (fetch)
origin  https://github.com/folivoramanh/advanced-git-exercises (push)
upstream        https://github.com/nnja/advanced-git-exercises (fetch)
upstream        https://github.com/nnja/advanced-git-exercises (push)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout master
Already on 'master'
Your branch is ahead of 'upstream/master' by 1 commit.
  (use "git push" to publish your local commits)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git branch --set-upstream-to origin/master
fatal: the requested upstream branch 'origin/master' does not exist
hint:
hint: If you are planning on basing your work on an upstream
hint: branch that already exists at the remote, you may need to
hint: run "git fetch" to retrieve it.
hint:
hint: If you are planning to push out a new local branch that
hint: will track its remote counterpart, you may want to use
hint: "git push -u" to set the upstream config as you push.
hint: Disable this message with "git config advice.setUpstreamFailure false"
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git pull origin master --allow-unrelated-histories
From https://github.com/folivoramanh/advanced-git-exercises
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> origin/master
Already up to date.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git branch --set-upstream-to origin/master
branch 'master' set up to track 'origin/master'.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout -b feature
Switched to a new branch 'feature'
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "Change to local repo" > local_change.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add local_change.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Change to local repo"
[feature 22ac171] Change to local repo
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 local_change.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git pull --rebase upstream master
From https://github.com/nnja/advanced-git-exercises
 * branch            master     -> FETCH_HEAD
Current branch feature is up to date.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
22ac171 (HEAD -> feature) Change to local repo
b3f4963 (master) Master has continued to change
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>   