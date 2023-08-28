PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  echo "Bad data" > hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.template
Bad data
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout -- hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.template
[greeting] [noun]!
This is a test of the emergency git-casting system.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --name-status --follow --oneline hello.template
f631487 (HEAD -> exercise6) add file
A       hello.template
f77f2f9 deleted:    hello.template
D       hello.template
4b2b90e (upstream/exercise6) Replacing greeting with tokens for i18n
R073    hello.txt       hello.template
fec9e7b Changing Hello to Hola
M       hello.txt
afa34a6 Changing World to Mundo
M       hello.txt
e348ebc (tag: my-exercise3-tag, tag: exercise3-annotated-tag, upstream/exercise3, exercise3) Testing the emergency git-casting system
M       hello.txt
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, exercise2, refs/bisect/good-43388fee19744e8893467331d7853a6475a227b8) Initial commit
A       hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout fec9e7b -- hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.txt
Hola World!
This is a test of the emergency git-casting system.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git reset HEAD hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git rm hello.template
rm 'hello.template'
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Deleting hello.template"
diff: unknown option -- staged
diff: Try 'diff --help' for more information.
[exercise6 31b6f4a] Deleting hello.template
 1 file changed, 2 deletions(-)
 delete mode 100644 hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --diff-filter=D --oneline -- hello.template
31b6f4a (HEAD -> exercise6) Deleting hello.template
f77f2f9 deleted:    hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout 31b6f4a^ -- hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.template
[greeting] [noun]!
This is a test of the emergency git-casting system.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git clean --dry-run
Would remove hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git clean -f
Removing hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git reset -- hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
31b6f4a (HEAD -> exercise6) Deleting hello.template
f631487 add file
f77f2f9 deleted:    hello.template
4b2b90e (upstream/exercise6) Replacing greeting with tokens for i18n
ff91b70 (upstream/exercise5, exercise5) Merging in mundo branch
fec9e7b Changing Hello to Hola
4582f72 Merge branch 'exercise3' into exercise4
afa34a6 Changing World to Mundo
7ea8b01 Merge branch 'exercise3' into exercise4
e348ebc (tag: my-exercise3-tag, tag: exercise3-annotated-tag, upstream/exercise3, exercise3) Testing the emergency git-casting system
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, exercise2, refs/bisect/good-43388fee19744e8893467331d7853a6475a227b8) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> rm hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.template
cat : Cannot find path 'C:\Users\LENOVO\OneDrive - National Economics University\Manh and
DSEB\advanced-git-exercises\hello.template' because it does not exist.
At line:1 char:1
+ cat hello.template
+ ~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (C:\Users\LENOVO...\hello.template:String) [Get-Content], ItemNotFoundEx
   ception
    + FullyQualifiedErrorId : PathNotFound,Microsoft.PowerShell.Commands.GetContentCommand

PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git reset 4b2b90e -- hello.template
Unstaged changes after reset:
D       hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.template
cat : Cannot find path 'C:\Users\LENOVO\OneDrive - National Economics University\Manh and
DSEB\advanced-git-exercises\hello.template' because it does not exist.
At line:1 char:1
+ cat hello.template
+ ~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (C:\Users\LENOVO...\hello.template:String) [Get-Content], ItemNotFoundEx
   ception
    + FullyQualifiedErrorId : PathNotFound,Microsoft.PowerShell.Commands.GetContentCommand

PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git reset --hard HEAD
HEAD is now at 31b6f4a Deleting hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log -2 --oneline
31b6f4a (HEAD -> exercise6) Deleting hello.template
f631487 add file
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git reset 4b2b90e
Unstaged changes after reset:
D       hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log -1 --oneline
4b2b90e (HEAD -> exercise6, upstream/exercise6) Replacing greeting with tokens for i18n
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git reset ORIG_HEAD
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log -1 --oneline
31b6f4a (HEAD -> exercise6) Deleting hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git revert 31b6f4a
[exercise6 946dd83] Revert "Deleting hello.template"
 1 file changed, 2 insertions(+)
 create mode 100644 hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>