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

## How to 删除 github 文件/文件夹

经常需要删除 github 的文件或文件夹，如果仅删除文件可能还能在网站里删除（但是当要删除的文件较多的时候，一个一个删除简直要命～～～），但是删除文件夹该怎么办呢？

### 直接在网站里删除的方法如下：

点击文件右上角的“删除按钮”，滑到页面最下方点击“commit changes”

找到删除按钮.png

### 通过 git 的方式删除

首先我们将整个仓库 clone 到本地

git clone https://github.com/***

在 clone 下来的本地仓库里初始化

git init

选择删除文件或者文件夹

git rm FILE 删除文件

git rm -r \*\*\*删除文件夹

当然这里也可以有对应的增加操作

提交上述操作

git commit -m "log message"

推送所有文件到远程仓库

git push origin master

这时候如果再执行添加 origin 操作，会提示远程 origin 已经存在。

细心的可能会发现这地方跟添加本地项目到 github 的最后一步操作不一样，那里是 git push -u origin master

第一次添加远程 origin 时，需要语句-u

这时候我们再去 github 上查看此项目，就可以看到已经更新了刚才的操作！
