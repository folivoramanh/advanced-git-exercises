PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout exercise9
Switched to a new branch 'exercise9'
branch 'exercise9' set up to track 'upstream/exercise9'.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git grep -e "Python"
python_code.py:# This is a Python file
python_code.py:    print("Welcome to Python!")
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git grep --line-number --heading --break -e "Python"
python_code.py
1:# This is a Python file
4:    print("Welcome to Python!")
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> echo "More Python code" >> python_code.py
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git grep --line-number -e "Python"
Binary file python_code.py matches
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git grep --line-number --cached -e "Python"
python_code.py:1:# This is a Python file
python_code.py:4:    print("Welcome to Python!")
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add python_code.py
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git grep --line-number --cached -e "Python"
Binary file python_code.py matches
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git grep --line-number --cached -e "Python"
Binary file python_code.py matches
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  git grep --line-number -e "Python"
Binary file python_code.py matches
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git grep --line-number --cached -e "Python"
Binary file python_code.py matches
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git checkout python_code.py
Updated 0 paths from the index
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
88f6e28 (HEAD -> exercise9, upstream/exercise9) Adding bash, python, and java code examples
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, o
rigin/master, exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log exercise3 --oneline
e348ebc (tag: my-exercise3-tag, tag: exercise3-annotated-tag, upstream/exercise3, exercise3) Testing the emergency git-casting system
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git cherry-pick e348ebc
error: your local changes would be overwritten by cherry-pick.
hint: commit your changes or stash them to proceed.
fatal: cherry-pick failed
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git add .
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "update"
[exercise9 22186e0] update
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git cherry-pick e348ebc
[exercise9 04072d2] Testing the emergency git-casting system
 Author: Nina Zakharenko <nina@nnja.io>
 Date: Wed Oct 4 19:01:12 2017 -0700
 1 file changed, 1 insertion(+)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
04072d2 (HEAD -> exercise9) Testing the emergency git-casting system
22186e0 update
88f6e28 (upstream/exercise9) Adding bash, python, and java code examples
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git blame hello.txt
^43388fe (Nina Zakharenko 2017-10-04 18:51:49 -0700 1) Hello World!
04072d28 (Nina Zakharenko 2017-10-04 19:01:12 -0700 2) This is a test of the emergency git-casting system.
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises>  git rm java_code.java
rm 'java_code.java'
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git commit -m "Who uses Java anyway?"
[exercise9 d0155ea] Who uses Java anyway?
 1 file changed, 7 deletions(-)
 delete mode 100644 java_code.java
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --diff-filter=D -- java_code.java
commit d0155eafe943329a62e8b97eea2945760d2b8c40 (HEAD -> exercise9)
Author: Mai Anh <11219260@st.neu.edu.vn>
Date:   Tue Aug 29 00:44:21 2023 +0700

    Who uses Java anyway?
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git blame d0155eafe943329a62e8b97eea2945760d2b8c40^ -- java_code.java
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 1) // This is a Java file
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 2)
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 3) public class HelloWorld {
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 4)    public static void main(String[] args) {
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 5)       System.out.println("Привет от Java!");
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 6)    }
88f6e286 (Nina Zakharenko 2017-10-05 11:31:34 -0700 7) }
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git log --oneline
d0155ea (HEAD -> exercise9) Who uses Java anyway?
04072d2 Testing the emergency git-casting system
22186e0 update
88f6e28 (upstream/exercise9) Adding bash, python, and java code examples
43388fe (upstream/master, upstream/exercise7, upstream/exercise4, upstream/exercise2, upstream/HEAD, origin/master, exercise2) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git bisect start d0155ea 43388fe
Bisecting: 1 revision left to test after this (roughly 1 step)
[22186e0cee22dd0bc99975f61f05912cd638cc0c] update
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.txt
Hello World!
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git bisect bad
Bisecting: 0 revisions left to test after this (roughly 0 steps)
[88f6e2864bd0829c71654f1d19096f436a66ce07] Adding bash, python, and java code examples
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> cat hello.txt
Hello World!
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> git bisect good
22186e0cee22dd0bc99975f61f05912cd638cc0c is the first bad commit
commit 22186e0cee22dd0bc99975f61f05912cd638cc0c
Author: Mai Anh <11219260@st.neu.edu.vn>
Date:   Tue Aug 29 00:43:48 2023 +0700

    update

 python_code.py | Bin 80 -> 120 bytes
 1 file changed, 0 insertions(+), 0 deletions(-)
PS C:\Users\LENOVO\OneDrive - National Economics University\Manh and DSEB\advanced-git-exercises> 