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

## Status
```bash
git remove -v
# output: origin  https://github.com/kylrmoore/learning_git (fetch)
# output: origin  https://github.com/kylrmoore/learning_git (push)
```
The above command will inform the user of what repositories it is currenctly conected 
to.  Typically, this will return the same info for fetch as well as push since we are 
pulling and pushing to the same git repo.

## Pushing to your repo
```bash
git push -u origin master            # Push origin to master and track remote branch master to origin
git push                             # If we run -u option, we should simply be able to use git push
```
Using the first command listed above will push your local 'origin' repository to the 
remote repository branch 'master'.  The '-u' option will set the repository to track 
the remote branch 'master' from 'origin', which is our local repository.  This pretty 
much just lets us say 'git push' and it will know what to do from there.

## Branching
```bash
git branch                           # Shows the available branches as well as which one you are using
# output: *master                    # The * indicates that we are currently on this branch

git checkout                         # Git checkout will be used to switch between branches
git checkout -b feature              # Adding the '-b' flag will create a new branch
```
Branching is a way to work on a feature without disturbing others who may be 
working on the same branch as you.  So what we can do is create a new branch where 
we can work on whatever we need to without effecting everyone else.  Once we are 
finished with this branch, we will want to merge back with the main branch.  

Using 'git checkout -b feature' will create a new branch named "feature". 
Typically we will want to use a more descriptive name to let everyone know what 
is going on with this branch.  It is common to see "feature-$ticket_id_number" 
or "feature-$git_issue_number" to keep track of what is being worekd on.
