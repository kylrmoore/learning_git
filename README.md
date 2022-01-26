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
The above command will inform the user of what repositories it is currently connected 
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
git diff branch                      # Checks what changed between two points in time
git push origin feature              # Push to the 'feature' branch
git pull                             # Create a pull request
                                     # Head over to github and have the request approved
git branch -d feature                # Be sure to delete your local branch after merging
```
Branching is a way to work on a feature without disturbing others who may be 
working on the same branch as you.  So what we can do is create a new branch where 
we can work on whatever we need to without effecting everyone else.  Once we are 
finished with this branch, we will want to merge back with the main branch.  

Using 'git checkout -b feature' will create a new branch named "feature". 
Typically we will want to use a more descriptive name to let everyone know what 
is going on with this branch.  It is common to see "feature-$ticket_id_number" 
or "feature-$git_issue_number" to keep track of what is being worked on.

## Git Merge
```bash
git merge $branch_to_merge_into      # Merges currently checked out branch into specified branch
git checkout main
git pull
git branch -d $feature_branch        # Once we merge and have been approved, we can run this command 
                                     # Which will delete our local branch
```
In order to add data from one branch to another, we need to merge our commits. 
We can do this by typing the command "git merge branch_name". This command, 
after all changes have been pushed, will merge all of our data with the 
specified branch.

## Git Reset
```bash
git reset $commit_id_number          # How to reset your repo back to a specific state
git log                              # Just in case you need the commit id
```
If you run the command above, it will reset your repo back to a specific commit.  This 
will typically warn about what files will change if you reset back to an earlier state. 
If you do not know what the commit id is, you can run "git log" to see them.
