PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git branch
  exercise2
  exercise3
  exercise4
* exercise5
  master
  mundo
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "[greeting] [noun]" > hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.txt
[greeting] [noun]
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git mv hello.txt hello.template
fatal: bad source, source=hello.txt, destination=hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> mv hello.txt hello.template
mv : Cannot find path 'C:\Users\LENOVO\OneDrive - National Economics University\Manh and
DSEB\advanced-git-exercises\hello.txt' because it does not exist.
At line:1 char:1
+ mv hello.txt hello.template
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (C:\Users\LENOVO...cises\hello.txt:String) [Move-Item], ItemNotFoundExce
   ption
    + FullyQualifiedErrorId : PathNotFound,Microsoft.PowerShell.Commands.MoveItemCommand

PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git mv -f hello.txt hello.template
fatal: bad source, source=hello.txt, destination=hello.template
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git rm --cached hello.txt
rm 'hello.txt'
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add hello.templete
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit
Aborting commit due to empty commit message.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --since="yesterday"
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --name-status --follow --oneline hello.template

fatal: ambiguous argument 'hello.template': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat ls-files
cat : Cannot find path 'C:\Users\LENOVO\OneDrive
- National Economics University\Manh and
DSEB\advanced-git-exercises\ls-files' because it
does not exist.
At line:1 char:1
+ cat ls-files
+ ~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (C:
   \Users\LENOVO...rcises\ls-files:String) [Get-
  Content], ItemNotFoundException
    + FullyQualifiedErrorId : PathNotFound,Micros
   oft.PowerShell.Commands.GetContentCommand

PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --grep=i18n --author=nina --since=2.weeks
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  git log --diff-filter=R --find-renames
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --diff-filter=M --oneline
fec9e7b Changing Hello to Hola
afa34a6 Changing World to Mundo
e348ebc (tag: my-exercise3-tag, tag: exercise3-annotated-tag, origin/exercise3, exercise3) Testing the emergency git-casting system
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --grep=i18n --oneline
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git show 4b2b90e
commit 4b2b90ec4f526139ca9c81e22174ebf5b9c56b52 (origin/exercise6)
Author: Nina Zakharenko <nina@nnja.io>
Date:   Wed Oct 4 20:46:45 2017 -0700

    Replacing greeting with tokens for i18n

    Currently, hello.txt contains both Spanish and English.
    Let's replace Hola with a [greeting] token, and Mundo
    with a [noun] token. That way, we can localize hello.txt for
    any language!

diff --git a/hello.txt b/hello.template
similarity index 73%
rename from hello.txt
rename to hello.template
index 7018e35..a6c57ac 100644
--- a/hello.txt
+++ b/hello.template
@@ -1,2 +1,2 @@
-Hola Mundo!
+[greeting] [noun]!
 This is a test of the emergency git-casting system.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git branch --merged master
  exercise2
  exercise4
  master
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git branch --no-merged master
  exercise3
* exercise5
  mundo
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  