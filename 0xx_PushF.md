# git push -f

- What is `git push -f`?

You cannot push if someone pushed some commits on the same branch before you because Git cannot guess how to fix the conflict.

`git push -f` will withdraw your colleagues commits and replace the whole history with yours. This should never be used.

- What are the differences between `git push -f` and `git push`?

- How to disable `git push -f` or prevent `git push -f`?

If you have the appropriate permissions on your "central" git repository, you can disable force push by git config --system receive.denyNonFastForwards true.

For Github Enterprise, you can follow instructions on this page to disable force push.

For other Github repositories (the ones that most of us use daily), there are no ways to disable force push. Some workarounds include:

- Limiting the group of people will push privileges. Other contributions will have to come in as Pull Requests.
- Set up an intermediate repo on your side with a pre-receive hook to prevent force push.
