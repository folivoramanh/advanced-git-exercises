PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout exercise3
Switched to a new branch 'exercise3'
branch 'exercise3' set up to track 'origin/exercise3'.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat .git/HEAD
ref: refs/heads/exercise3
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git branch
  exercise2
* exercise3
  master
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git show-ref --heads
43388fee19744e8893467331d7853a6475a227b8 refs/heads/exercise2
e348ebc1187cb3b4066b1e9432a614b464bf9d07 refs/heads/exercise3
43388fee19744e8893467331d7853a6475a227b8 refs/heads/master
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git cat-file -p 43388fee19744e8893467331d7853a6475a227b8
tree 581caa0fe56cf01dc028cc0b089d364993e046b6
author Nina Zakharenko <nina@nnja.io> 1507168309 -0700
committer Nina Zakharenko <nina@nnja.io> 1507168309 -0700

Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git cat-file -p e348ebc1187cb3b4066b1e9432a614b464bf9d07
tree cbcdf5dda7853d595fe0b1942cb0d1d72eb910f3
parent 43388fee19744e8893467331d7853a6475a227b8
author Nina Zakharenko <nina@nnja.io> 1507168872 -0700
committer Nina Zakharenko <nina@nnja.io> 1507168872 -0700

Testing the emergency git-casting system
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git tag my-exercise3-tag
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  git show-ref --tags
e348ebc1187cb3b4066b1e9432a614b464bf9d07 refs/tags/my-exercise3-tag
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git tag --points-at e348ebc
my-exercise3-tag
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git tag -a "exercise3-annotated-tag" -m "This is my annotated tag for exercise 3"
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git show exercise3-annotated-tag
tag exercise3-annotated-tag
Tagger: Mai Anh <11219260@st.neu.edu.vn>
Date:   Mon Aug 28 23:49:56 2023 +0700

This is my annotated tag for exercise 3

commit e348ebc1187cb3b4066b1e9432a614b464bf9d07 (HEAD -> exercise3, tag: my-exercise3-tag, tag: exercise3-annotated-tag, origin/exercise3)
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 19:01:12 2017 -0700

    Testing the emergency git-casting system

diff --git a/hello.txt b/hello.txt
index 980a0d5..b31a35b 100644
--- a/hello.txt
+++ b/hello.txt
@@ -1 +1,2 @@
 Hello World!
+This is a test of the emergency git-casting system.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
e348ebc (HEAD -> exercise3, tag: my-exercise3-tag, tag: exercise3-annotated-tag, origin/exercise3) Testing the emergency git-casting system
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD, master, exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout e348ebc
Note: switching to 'e348ebc'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at e348ebc Testing the emergency git-casting system
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat .git/HEAD
e348ebc1187cb3b4066b1e9432a614b464bf9d07
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "This is a test file" > dangle.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add dangle.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "This is a dangling commit"
[detached HEAD 61af247] This is a dangling commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 dangle.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
61af247 (HEAD) This is a dangling commit
e348ebc (tag: my-exercise3-tag, tag: exercise3-annotated-tag, origin/exercise3, exercise3) Testing the emergency git-casting system
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD, master, exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat .git/HEAD
61af247b43f8bc11cf68683f5f8cac87d5b3d9da
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout exercise3
Warning: you are leaving 1 commit behind, not connected to
any of your branches:

  61af247 This is a dangling commit

If you want to keep it by creating a new branch, this may be a good time
to do so with:

 git branch <new-branch-name> 61af247

Switched to branch 'exercise3'
Your branch is up to date with 'origin/exercise3'.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>    