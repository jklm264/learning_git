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

- Git conflict resolution - from second branch when ready to push:
- Git commit -m “msg”
- Git push origin master # Will give error: failed to push some refs….current branch is behind its remote counterpart.
- Git pull --rebase origin master # Will give “CONFLICT (content): Merge conflict”
- Git mergetool
  - In the bottom pane make corrections/definitive edits as needed then save and exit ALL windows (Vim so wq/x)
- Git rebase --continue # You are continuing with step 3. Should say “Applying: <commit msg>”
- Git long -n 2 # Will check to make sure before push
- Git push origin master

All of this was from https://www.youtube.com/watch?v=r_27MKuA9dY

Differences are enumerated here: https://stackoverflow.com/a/804156/5540115
