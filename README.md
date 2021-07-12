# learning_git

## Git Rebase

Purpose: Teaching me how to use git rebase

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
