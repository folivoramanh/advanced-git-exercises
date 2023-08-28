C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB>git clone https://github.com/nnja/advanced-git-exercises
Cloning into 'advanced-git-exercises'...
remote: Enumerating objects: 28, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 28 (delta 0), reused 0 (delta 0), pack-reused 25
Receiving objects: 100% (28/28), done.
Resolving deltas: 100% (1/1), done.

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB>cd advanced-git-exercises

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git checkout exercise2
Switched to a new branch 'exercise2'
branch 'exercise2' set up to track 'origin/exercise2'.

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git ls-files -s
100644 980a0d5f19a64b4b30a87d4206aade58726b60e3 0 hello.txt

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>echo "This is a test of the emergency git-casting system." >> hello.txt

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git add -p
diff --git a/hello.txt b/hello.txt
index 980a0d5..b947a3d 100644
--- a/hello.txt
+++ b/hello.txt
@@ -1 +1,2 @@
 Hello World!
+"This is a test of the emergency git-casting system."
(1/1) Stage this hunk [y,n,q,a,d,e,?]?
@@ -1 +1,2 @@
 Hello World!
+"This is a test of the emergency git-casting system."
(1/1) Stage this hunk [y,n,q,a,d,e,?]? y
<stdin>:7: trailing whitespace.
"This is a test of the emergency git-casting system."
warning: 1 line adds whitespace errors.


C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git status
On branch exercise2
Your branch is up to date with 'origin/exercise2'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   hello.txt


C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git ls-files -s
100644 b947a3df8e546de4b69357e40b75ef0a4406b834 0 hello.txt

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git reset hello.txt
Unstaged changes after reset:
M       hello.txt

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git status
On branch exercise2
Your branch is up to date with 'origin/exercise2'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.txt

no changes added to commit (use "git add" and/or "git commit -a")

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git stash save "emergency git-casting"
Saved working directory and index state On exercise2: emergency git-casting

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git status
On branch exercise2
Your branch is up to date with 'origin/exercise2'.

nothing to commit, working tree clean

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git stash list
stash@{0}: On exercise2: emergency git-casting

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git stash show stash@{0}
 hello.txt | 1 +
 1 file changed, 1 insertion(+)

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git stash apply stash@{0}
On branch exercise2
Your branch is up to date with 'origin/exercise2'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   hello.txt

no changes added to commit (use "git add" and/or "git commit -a")

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>git diff hello.txt
diff --git a/hello.txt b/hello.txt
index 980a0d5..b947a3d 100644
--- a/hello.txt
+++ b/hello.txt
@@ -1 +1,2 @@
 Hello World!
+"This is a test of the emergency git-casting system."

C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>   