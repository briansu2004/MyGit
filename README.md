# MyGit

My Git

Very important to work in a team :-)

## How to git 撤销上一次 push 的版本!

https://blog.csdn.net/m0_37605197/article/details/110919455

可以用 git log 查看你要回到的那个版本

接着用

```
git reset --hard HEAD^ 回退到上个版本
```

or

```
git reset --hard commit_id 退到/进到 指定commit_id
```

最后将本地的修改提交到远程

```
git push origin HEAD --force
```

### Proof

This has been verified at Mar 27, 2022!

```
git log
git reset --hard 4187b33265e
git push origin HEAD --force
git log
```

### 当你回滚之后，又后悔了，想恢复到新的版本怎么办？

用 `git reflog` 打印你记录你的每一次操作记录

git reflog 可以查看所有分支的所有操作记录（包括（包括 commit 和 reset 的操作），包括已经被删除的 commit 记录，git log 则不能察看已经删除了的 commit 记录。

简单的说，它会记录所有 HEAD 的历史，也就是说当你做 reset，checkout 等操作的时候，这些操作会被记录在 reflog 中。
