# Learning Git
The purpose of this repository is to learn git and git commands.  I hope to eventually 
also learn a little bit about git actions but, we will see when I have some time to take 
a look at this.  In the mean time, I will update this repo with new tricks that I learn 
along the way.

## First Steps
### Project already exists
```bash
git remote add origin $remote_addr    # Link local repo to remote (github)
git branch -M main                    # Create a new branch
git add .                             # Add all files to your local git repo.
git commit -m "example description"   # Add a description for the commit
git push -u origin main               # Push to remote branch "main"
```
The three commands above is what we will need to run to start a github project. The 
first portion is used to link our local repository to the remote repository.  Without 
this link, git will have no idea where to push new data.  Next step is to create a new 
branch "main".  You can call this whatever you want but it is standard to call this 
something like "main" or "master" since this is the first "Main" branch.  Then we add 
our files with the "git add ." command and commit them with a description of what 
changed.  Finally, push the contents of "origin", which is your local repo, to the 
remote repos branch "main" that we created earlier.
