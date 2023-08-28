ex8 is about to fork repo, upstream branch and try something after fork with new branch feature
so i merge the branch feature to master/exercise8
NOTE:
when doin ex8, maybe windows-user may get this error after add remote origin and try to set upstream for the origin
"fatal: the requested upstream branch 'origin/master' does not exist"
Solution:
1. run this command first
git pull origin master --allow-unrelated-histories
2. then try the upstream command again
git branch --set-upstream-to=origin/master master
