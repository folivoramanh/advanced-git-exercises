PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout exercise4
Switched to a new branch 'exercise4'
branch 'exercise4' set up to track 'origin/exercise4'.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git merge exercise3
Updating 43388fe..e348ebc
Fast-forward
 hello.txt | 1 +
 1 file changed, 1 insertion(+)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
e348ebc (HEAD -> exercise4, tag: my-exercise3-tag, tag: exercise3-annotated-tag, origin/exercise3, exercise3) Testing the emergency git-casting system
43388fe (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD, master, exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git reset --hard HEAD^
HEAD is now at 43388fe Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git merge --no-ff exercise3
Merge made by the 'ort' strategy.
 hello.txt | 1 +
 1 file changed, 1 insertion(+)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --graph
*   commit 200ead2947c9e1aa94c7e7131e62d5a4e7c164df (HEAD -> exercise4)
|\  Merge: 43388fe e348ebc
| | Author: Mai Anh <11219260@st.neu.edu.vn>
| | Date:   Mon Aug 28 23:55:02 2023 +0700
| |
| |     Merge branch 'exercise3' into exercise4
| |
| * commit e348ebc1187cb3b4066b1e9432a614b464bf9d07 (tag: my-exercise3-tag, tag: exercise3-annotated-tag, origin/exercise3, exercise3)
|/  Author: Nina Zakharenko <nina@nnja.io>
|   Date:   Wed Oct 4 19:01:12 2017 -0700
|
|       Testing the emergency git-casting system
|
* commit 43388fee19744e8893467331d7853a6475a227b8 (origin/master, origin/exercise7, origin/exercise4, origin/exercise2, origin/HEAD, master, exercise2)
  Author: Nina Zakharenko <nina@nnja.io>
  Date:   Wed Oct 4 18:51:49 2017 -0700

      Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git branch
  exercise2
  exercise3
* exercise4
  master
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout -b mundo
Switched to a new branch 'mundo'
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git branch
  exercise2
  exercise3
  exercise4
  master
* mundo
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "Hello Mundo!" > hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git status
On branch mundo
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.txt

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "change world to mundo"
[mundo e9212bd] change world to mundo
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout exercise4
Switched to branch 'exercise4'
Your branch is ahead of 'origin/exercise4' by 2 commits.
  (use "git push" to publish your local commits)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "Hola World!" > hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "change hello to hola"
[exercise4 555f21b] change hello to hola
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git config rerere.enabled true
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git merge mundo
warning: Cannot merge binary files: hello.txt (HEAD vs. mundo)
Auto-merging hello.txt
CONFLICT (content): Merge conflict in hello.txt
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git rerere diff
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git diff
diff --cc hello.txt
index 2d76b4c,80c5587..0000000
Binary files differ
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "Hola Mundo!" > hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git rerere diff
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Merging in mundo branch"
[exercise4 dd86f6e] Merging in mundo branch
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git reset --hard HEAD^
HEAD is now at 555f21b change hello to hola
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git merge mundo
warning: Cannot merge binary files: hello.txt (HEAD vs. mundo)
Auto-merging hello.txt
CONFLICT (content): Merge conflict in hello.txt
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.txt
Hola Mundo!
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  