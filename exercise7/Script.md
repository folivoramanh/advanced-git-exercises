PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout exercise7Switched to a new branch 'exercise7'
branch 'exercise7' set up to track 'origin/exercise7'.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> ec
                                                                                                > echo "This is the first file" > first.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "This is the second file" > second.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add first.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Committing two new files"
[exercise7 ddf27e2] Committing two new files
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 first.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add second.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit --amend
hint: Waiting for your editor to close the fi[exercise7 7ae7d52] Committing two new files
 Date: Tue Aug 29 00:25:33 2023 +0700
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 first.txt
 create mode 100644 second.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout -b exercise7-2
Switched to a new branch 'exercise7-2'
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
43388fe (HEAD -> exercise7-2, origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD, master, exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "New feature" > feature.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add feature.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Adding a new feature"
[exercise7-2 085f7fd] Adding a new feature
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 feature.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout master
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "Master has continued to change" >> hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  git commit -m "Master has continued to change"
[master b3f4963] Master has continued to change
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout exercise7-2
Switched to branch 'exercise7-2'
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git rebase master
Successfully rebased and updated refs/heads/exercise7-2.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
8dc74e4 (HEAD -> exercise7-2) Adding a new feature
b3f4963 (master) Master has continued to change
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD,
 exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "Another new feature" > another_feature.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add another_feature.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Adding another new feature"
[exercise7-2 7a75529] Adding another new feature
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 another_feature.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log -n 3 --oneline
7a75529 (HEAD -> exercise7-2) Adding another new feature
8dc74e4 Adding a new feature
b3f4963 (master) Master has continued to change
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git rebase -i HEAD~2
hint: Waiting for your editor to close the fiSuccessfully rebased and updated refs/heads/exercise7-2.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git rebase -i HEAD~2
hint: Waiting for your editor to close the fihint: Waiting for your editor to close the fi[detached HEAD 64af793] Adding two new features
 Date: Tue Aug 29 00:26:40 2023 +0700
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 feature.txt
hint: Waiting for your editor to close the fi[detached HEAD 283fb7b] Adding two new features
 Date: Tue Aug 29 00:26:40 2023 +0700
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 another_feature.txt
 create mode 100644 feature.txt
Successfully rebased and updated refs/heads/exercise7-2.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
283fb7b (HEAD -> exercise7-2) Adding two new features
b3f4963 (master) Master has continued to change
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD,
 exercise2) Initial commit