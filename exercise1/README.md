When typing tree .git, window user might be dont see all the blow of what we created

Solution: Using this command "Get-ChildItem -Path .git\objects -Recurse -Depth 2" or cheating by using "cat ls-flies -s" 
Or another cheat that you can use git log and pass the step of seeing tree and git cat file, however it might log all of trash file that you accidently create it, so, not really recommend this solution