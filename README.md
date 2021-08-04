# branch-cheat-sheet

- local branch= branch only on your computer
- remote branch= branch on github

## Branching and Merging

$ git branch                                     - show list of all branches (* is active)
$ git checkout -b branch-name                     # create a new branch named "branch-name" and checkout

- git checkout master                             # go back to master branch
git checkout branch-name                        # go back to branch-name
git merge branch-name                           # merge changesets from branch-name
git pull . branch-name                          # merge changesets from branch-name
git branch -m branch-name new-name              # rename branch
git branch -m new-name                          # rename current branch

## Tracking and Submitting Changes
git add .                                       # tracks changes of current directory
git commit -m "comment"                         # captures changes that need to be committed to the remote branch with a message
git commit -am "comment                         # (same as git add . and git commit -m "comment" but in one command)
git push                                        # pushes changed to the remote branch
git push --set-upstream origin branch-name      # if local branch doesn't have an upstream remote branch then this will create and upstream remote branch and push the changes


### Delete Project
git branch -d branch-name  	                    # deletes local branch
git push origin :branch-name	                  # deletes remote branch
git remote prune branch-name	                  # update local/remote sync


### Merging Upstream

git remote -v 									                # Get list of remote branches
git remote add upstream <upstream github url>	  # Add original as upstream
git remote -v 									                # Check upstream

git fetch upstream 								              # Get original repo
git checkout development						            # Switch to main branch in local fork
git merge upstream/development					        # Merge original with fork

git diff --name-only main branch-name		        # Lists names of files with differences from the main remote branch and local branch
  
  
  
