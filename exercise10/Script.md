PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  git checkout exercise10
Previous HEAD position was 88f6e28 Adding bash, python, and java code examples
Switched to a new branch 'exercise10'
branch 'exercise10' set up to track 'upstream/exercise10'.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cp pre-commit .git/hooks/pre-commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> chmod +x .git/hooks/pre-commit
chmod : The term 'chmod' is not recognized as the
name of a cmdlet, function, script file, or
operable program. Check the spelling of the name,
or if a path was included, verify that the path
is correct and try again.
At line:1 char:1
+ chmod +x .git/hooks/pre-commit
+ ~~~~~
    + CategoryInfo          : ObjectNotFound: (ch
   mod:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundExce
   ption

PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> icacls .git/hooks/pre-commit
.git/hooks/pre-commit NT AUTHORITY\SYSTEM:(I)(F)
                      BUILTIN\Administrators:(I)(F)
                      DESKTOP-S6FTGU5\LENOVO:(I)(F)

Successfully processed 1 files; Failed processing 0 files
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "Bad bash script" > test_script.sh
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add test_script.sh
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Adding a new test script"
error: cannot spawn .git/hooks/pre-commit: No such file or directory
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Adding a new test script"
No shebang found! Not allowed to commit!
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo '#!/bin/bash\n Good bash script' > test_script.sh
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add test_script.sh
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Adding a new test script"
No shebang found! Not allowed to commit!
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo '#!/bin/bash\n Good bash script' > test_script.sh
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add test_script.sh
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "sth"
diff: unknown option -- staged
diff: Try 'diff --help' for more information.
[exercise10 8502bb8] sth
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test_script.sh
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>    