
# Branch Cheat Sheet

  - local branch= branch only on your computer
  - remote branch= branch on github

## Branching and Merging

#### $ git branch
  -- shows list of all local branches (* is active)

#### $ git checkout -b local_branch
  -- create a new local branch named "local_branch" and checkout

#### $ git checkout master                            
  -- go back to master branch

#### $ git checkout local_branch                       
  -- go back to local_branch
 
#### $ git merge local_branch                           
  -- merge changesets from local_branch

#### $ git pull . local_branch                          
  -- merge changesets local_branch

#### $ git branch -m local_branch new-name             
  -- rename branch

#### $ git branch -m new-name                          
  -- rename current branch

## Tracking and Submitting Changes

#### $ git add .                                                                 
  -- tracks changes of current directory

#### $ git commit -m "comment"                                                   
  -- captures changes that need to be committed to the remote branch with a message

#### $ git commit -am "comment                                                   
  -- (same as git add . and git commit -m "comment" but in one command)

#### $ git push                                                                  
  -- pushes changed to the remote branch

#### $ git push --set-upstream origin local_branch                                
  -- if local branch doesn't have an upstream remote branch then this will create an upstream remote branch and push the changes

#### $ git merge main
  -- if in your local branch this will update your branch to whats on the main remote branch

## Delete Project

#### $ git branch -d local_branch  	                                              
  -- deletes local branch

#### git push origin --delete remote_branch
  -- deletes remote branch

#### $ git push origin :remote_branch	                                            
  -- push a delete signal to the remote origin repository that triggers a delete of the remote branch

#### $ git remote prune local_branch 	                                            
  -- update local/remote sync

## Merging Upstream

#### $ git remote -v 									                                          
  -- Get list of remote branches

#### $ git remote add upstream <upstream github url>	                            
  -- Add original as upstream

#### $ git remote -v 									                                          
  -- Check upstream

#### $ git fetch upstream 								                                        
  -- Get original repo

#### $ git merge upstream/development					                                  
  -- Merge original with fork

#### $ git diff --name-only main local_branch 		                                  
  -- Lists names of files with differences from the main remote branch and local branch
