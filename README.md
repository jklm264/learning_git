# learning_git

## Git Merge

Purpose: Automatically add a feature (files not touched by combining branch) and will squash all commits into a single one.

- git merge --squash feature # summarize commits in feature branch into new commit in master branch that was being merged
  - This assume you run $git merge from the master branch and your feature branch is called "feature".
- git commit -m "msg"
- git log # check to make sure
- git push

Source: https://www.youtube.com/watch?v=CRlGDDprdOQ 


## Git Rebase

Purpose: Manually "merge" changes into a single branch. Commits of feature branch will show in commit history of master (unlike with $git merge).

### Method 1

Git conflict resolution - from second branch when ready to push:

- Git commit -m “msg”
- Git push origin master # Will give error: failed to push some refs….current branch is behind its remote counterpart.
- Git pull --rebase origin master # Will give “CONFLICT (content): Merge conflict”
- Git mergetool
  - In the bottom pane make corrections/definitive edits as needed then save and exit ALL windows (Vim so wq/x)
- Git rebase --continue # You are continuing with step 3. Should say “Applying: <commit msg>”
- Git long -n 2 # Will check to make sure before push
- Git push origin master

All of this was from https://www.youtube.com/watch?v=r_27MKuA9dY

### Method 2

- git checkout master
- git pull # Update local master to remote master
- git checkout feature # Switch back to feature branch
- git rebase master # "Re-anchor" feature branch against latest changes. If conflicts arise will do vimdiff (I think)
- git checkout master # switch back to master
- git rebase feature # Take commits from local feature branch and overlay on local master
- git push # Take commits on local master and move to remote master

Source: https://www.youtube.com/watch?v=f1wnYdLEpgI

Differences are enumerated here: https://stackoverflow.com/a/804156/5540115


## Changes

Here is one last change. Thanks for the memories.
