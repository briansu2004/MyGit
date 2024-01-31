# How to recover deleted git local branch?

## Scenario

- Wanted to clean up local branches
- Accidentally removed a local branch that I still need it for a while

## Solution

- git reflog | findstr 823

```text
070fb5bc HEAD@{7}: commit: JIRA-823: blah
```

- git checkout -b feature/brian-823-1 <sha>

```text
Switched to a new branch 'feature/brian-823'
```
