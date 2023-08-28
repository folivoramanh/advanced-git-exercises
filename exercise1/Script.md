PS C:\Users\LENOVO\OneDrive - National Economics University> mkdir projects/sample


    Directory: C:\Users\LENOVO\OneDrive - National Economics
    University\projects


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         8/28/2023  11:23 PM                sample


PS C:\Users\LENOVO\OneDrive - National Economics University> cd projects/sample
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git status
fatal: not a git repository (or any of the parent directories): .git
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git init
Initialized empty Git repository in C:/Users/LENOVO/OneDrive - National Economics University/projects/sample/.git/
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> echo 'Hello World!' > hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git add hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git commit -m "Initial commit"
[master (root-commit) b4a6103] Initial commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> tree .git
Folder PATH listing for volume Windows
Volume serial number is 8CAF-4B76
C:\USERS\LENOVO\ONEDRIVE - NATIONAL ECONOMICS UNIVERSITY\PROJECTS\SAMPLE\.GIT
├───hooks
├───info
├───logs
│   └───refs
│       └───heads
├───objects
│   ├───27
│   ├───b4
│   ├───de
│   ├───info
│   └───pack
└───refs
    ├───heads
    └───tags
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample>  Get-ChildItem -Path .git\objects -Recurse -Depth 2



    Directory: C:\Users\LENOVO\OneDrive - National Economics
    University\projects\sample\.git\objects


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         8/28/2023  11:24 PM                27
d-----         8/28/2023  11:24 PM                b4
d-----         8/28/2023  11:23 PM                de
d-----         8/28/2023  11:23 PM                info
d-----         8/28/2023  11:23 PM                pack


    Directory: C:\Users\LENOVO\OneDrive - National Economics
    University\projects\sample\.git\objects\27


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-ar---         8/28/2023  11:24 PM             54 ced35ea5a655b
                                                  916ae684741b5
                                                  01a99fa75b1d


    Directory: C:\Users\LENOVO\OneDrive - National Economics
    University\projects\sample\.git\objects\b4


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-ar---         8/28/2023  11:24 PM            131 a6103def20f1c
                                                  b454e0920230b
                                                  399b55a4cb74


    Directory: C:\Users\LENOVO\OneDrive - National Economics
    University\projects\sample\.git\objects\de


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-ar---         8/28/2023  11:23 PM             42 39eb0e99467bf
                                                  70d32f98a07cc
                                                  3987d5d77093


PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git cat-file -t b4a61
commit
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git cat-file -p b4a61
tree 27ced35ea5a655b916ae684741b501a99fa75b1d
author Mai Anh <11219260@st.neu.edu.vn> 1693239845 +0700
committer Mai Anh <11219260@st.neu.edu.vn> 1693239845 +0700

Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git cat-file -t 27ced
tree
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git cat-file -p 27ced
100644 blob de39eb0e99467bf70d32f98a07cc3987d5d77093    hello.txt
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git cat-file -t de39e
blob
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git cat-file -p de39e
ÿþHello World!
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> cat .git/HEAD
ref: refs/heads/master
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> cat .git/refs/heads/master
b4a6103def20f1cb454e0920230b399b55a4cb74
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git log --oneline
b4a6103 (HEAD -> master) Initial commit
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> git branch sub_branch_ex1
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> tree .git/refs
Folder PATH listing for volume Windows
Volume serial number is 8CAF-4B76
C:\USERS\LENOVO\ONEDRIVE - NATIONAL ECONOMICS UNIVERSITY\PROJECTS\SAMPLE\.GIT\REFS
├───heads
└───tags
PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample> tree .git/refs/heads
Folder PATH listing for volume Windows
Volume serial number is 8CAF-4B76
C:\USERS\LENOVO\ONEDRIVE - NATIONAL ECONOMICS UNIVERSITY\PROJECTS\SAMPLE\.GIT\REFS\HEADS
No subfolders exist

PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample>  Get-ChildItem -Path .git\refs -Recurse -Depth 2


    Directory: C:\Users\LENOVO\OneDrive - National Economics
    University\projects\sample\.git\refs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
da---l         8/28/2023  11:29 PM                heads
da---l         8/28/2023  11:23 PM                tags


    Directory: C:\Users\LENOVO\OneDrive - National Economics
    University\projects\sample\.git\refs\heads


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a---l         8/28/2023  11:24 PM             41 master
-a----         8/28/2023  11:29 PM             41 sub_branch_ex
                                                  1


PS C:\Users\LENOVO\OneDrive - National Economics University\projects\sample>