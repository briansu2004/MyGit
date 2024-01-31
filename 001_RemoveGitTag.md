# How to remove the git tag?

C:\devbox>git tag deployment-pr.20231123
fatal: tag 'deployment-pr.20231123' already exists

To remove a tag in Git, you can use the following command:

```bash
git tag -d deployment-pr.20231123
```

This command deletes the local tag. If you've already pushed the tag to a remote repository, you'll also need to delete it from there. To delete the remote tag, you can use:

```bash
git push origin :refs/tags/deployment-pr.20231123
```

This command essentially pushes an "empty" reference to the remote tag, effectively deleting it.

Alternatively, you can combine both operations into one command:

```bash
git push --delete origin deployment-pr.20231123
```

After performing these steps, the tag `deployment-pr.20231123` should be removed both locally and remotely.
