# Tricks on removing remote branches

This issue happened to Bitbucket but it may happen to others as well.

Here is the full description on this issue:

- Worked in a team with Bitbucket
- Created many feature branches
- Removed all remote feature branches through Bitbucket UI (didn't see any of them on the Bitbucket UI)
- However, them still showed up in sourcetree or with the command `git branch -r` or `git branch -a`

Tried `git push origin -d <feature/brian>` and got error "it doesn't exist"

Solution:

`git remote prune origin`
