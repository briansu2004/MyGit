# Git Submodule

## Commands

```dos
git submodule add https://github.com/briansu2004/MyAngular
git pull --recurse-submodules
git config submodule.recurse true
git submodule update --init
```

## Output

```dos
C:\Code\MyGit\SubModule>git submodule add https://github.com/briansu2004/MyAngular
Cloning into 'C:/Code/MyGit/SubModule/MyAngular'...
remote: Enumerating objects: 694, done.
remote: Counting objects: 100% (694/694), done.
remote: Compressing objects: 100% (525/525), done.
remote: Total 694 (delta 264), reused 493 (delta 123), pack-reused 0
Receiving objects: 100% (694/694), 3.05 MiB | 12.09 MiB/s, done.
Resolving deltas: 100% (264/264), done.
warning: LF will be replaced by CRLF in .gitmodules.
The file will have its original line endings in your working directory

C:\Code\MyGit\SubModule>git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   ../.gitmodules
        new file:   MyAngular

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore
        README.md

C:\Code\MyGit\SubModule>type ..\.gitmodules
[submodule "SubModule/MyAngular"]
        path = SubModule/MyAngular
        url = https://github.com/briansu2004/MyAngular
```

## Screenshot
