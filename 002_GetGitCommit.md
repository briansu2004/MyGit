# How to git 获取特定的 commit

`git reset --hard [commit_id]`

- Scenario

![](image/README/git_commit.png)

The commit on Dec 1, 2021 works.

But the commits after don't work :-)

I need to pick the work commit then build and deploy.

- Proof

Do a fresh glone -> retrieve the particular commit -> copy to the new branch -> build and trigger from this new branch -> test and verify -> close

Commands:

```dos
cd C:\_RepoFresh\#2

git clone https://github.com/telus/bdd-jest-merlin-cloud-bss-bridge.git

cd bdd-jest-merlin-cloud-bss-bridge

git branch

git log

git reset --hard 04ffe6a42f619527eaf4fbaead8e1ab738002cff

git log

git checkout -b v1.0

git branch

git status

git push --set-upstream origin v1.0
```

Output:

```dos
C:\Code\MyGit>cd C:\_RepoFresh\#2

C:\_RepoFresh\#2>git clone https://github.com/telus/bdd-jest-merlin-cloud-bss-bridge.git
Cloning into 'bdd-jest-merlin-cloud-bss-bridge'...
remote: Enumerating objects: 213, done.
remote: Counting objects: 100% (213/213), done.
remote: Compressing objects: 100% (138/138), done.
remote: Total 213 (delta 81), reused 191 (delta 59), pack-reused 0
Receiving objects: 100% (213/213), 277.76 KiB | 4.27 MiB/s, done.
Resolving deltas: 100% (81/81), done.

C:\_RepoFresh\#2>cd bdd-jest-merlin-cloud-bss-bridge

C:\_RepoFresh\#2\bdd-jest-merlin-cloud-bss-bridge>git branch
* main

C:\_RepoFresh\#2\bdd-jest-merlin-cloud-bss-bridge>git reset --hard 04ffe6a42f619527eaf4fbaead8e1ab738002cff
HEAD is now at 04ffe6a feat: restoring the default settings

C:\_RepoFresh\#2\bdd-jest-merlin-cloud-bss-bridge>git log
commit 04ffe6a42f619527eaf4fbaead8e1ab738002cff (HEAD -> main, tag: bdd-jest-mcb-v1.0.7)
Author: tim shao <tims.shao@telus.com>
Date:   Wed Dec 1 17:16:19 2021 -0500

    feat: restoring the default settings

C:\_RepoFresh\#2\bdd-jest-merlin-cloud-bss-bridge>git checkout -b v1.0
Switched to a new branch 'v1.0'

C:\_RepoFresh\#2\bdd-jest-merlin-cloud-bss-bridge>git branch
  main
* v1.0

C:\_RepoFresh\#2\bdd-jest-merlin-cloud-bss-bridge>git status
On branch v1.0
nothing to commit, working tree clean

C:\_RepoFresh\#2\bdd-jest-merlin-cloud-bss-bridge> git push --set-upstream origin v1.0
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'v1.0' on GitHub by visiting:
remote:      https://github.com/telus/bdd-jest-merlin-cloud-bss-bridge/pull/new/v1.0
remote:
To https://github.com/telus/bdd-jest-merlin-cloud-bss-bridge.git
 * [new branch]      v1.0 -> v1.0
Branch 'v1.0' set up to track remote branch 'v1.0' from 'origin'.
```
