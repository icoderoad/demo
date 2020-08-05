# demo
本仓库主要存放路条编程公众号文章示例程序源码，目前主要包含响应式网页设计相关的代码示例。
## 获取 Git 仓库

通常有两种获取Git仓库的方式：

* 创建本地仓库，将本地目录转换为 Git 仓库；

* 克隆远程仓库，从其它服务器，clone一个已存在的Git仓库。


### 创建本地仓

1. `git init` ：在当前目录创建.git文件夹，初始化git仓库。
2. `git add`：将对指定的文件进行追踪，纳入git管理。如：`git add README.md`，`git add *.java`。
3. `git commit -m "xxx"`：将追踪的文件提交的git仓库,并用-m增加本次提交的备注。
4. `git remote add origin [url]`。将本地仓库与一个远程仓库上的空仓库连接起来：
### 克隆远程仓库

* `git clone [url]`。如：`git clone https://github.com/libgit2/libgit2`。 这个命令将会在当前目录下创建一个名为 “libgit2” 的目录，并在这个目录下初始化一个 .git 目录，将所有项目文件拉取到“libgit2“目录下。

## Git术语表
`git`: 一个开源的分布式版本控制系统
`GitHub`: 一个托管和协作管理 Git 仓库的平台
`commit 提交`: 一个 Git 对象，是你整个仓库的快照的哈希值
`branch 分支`: 一个轻型可移动的 commit 指针
`clone`: 一个仓库的本地版本，包含所有提交和分支
`remote` 远端: 一个 GitHub 上的公共仓库，所有小组成员通过它来交换修改
`fork`: 一个属于另一用户的 GitHub 上的仓库的副本
`pull request拉取请求` : 一处用于比较和讨论分支上引入的差异，且具有评审、评论、集成测试等功能的地方
`HEAD`: 代表你当前的工作目录。使用git checkout 可移动 HEAD 指针到不同的分支、标记(tags)或提交

## Git命令简介
### 配置工具
对所有本地仓库的用户信息进行配置
对你的commit操作设置关联的用户名：
```
$ git config --global user.name "[name]"
```

对你的commit操作设置关联的邮箱地址：
```
$ git config --global user.email "[email address]"
```
启用有帮助的彩色命令行输出：
```
$ git config --global color.ui auto
```

### gitignore 文件
有时一些文件最好不要用 Git 跟踪。这通常在名为 .gitignore 的特殊文件中完成。你可以在 github.com/github/gitignore 找到有用的 .gitignore 文件模板

### 分支
分支是使用 Git 工作的一个重要部分。你做的任何提交都会发生在当前“checked out”到的分支上。使用 git status 查看那是哪个分支。

创建一个新分支：
```
$ git branch [branch-name]
```

切换到指定分支并更新工作目录(working directory)：
```
$ git checkout [branch-name]
```

将指定分支的历史合并到当前分支。这通常在拉取请求(PR)中完成，但也是一个重要的 Git 操作：
```
$ git merge [branch]
```

删除指定分支：
```
$ git branch -d [branch-name]
```

### 进行更改
列出当前分支的版本历史：
```
$ git log
```

列出文件的版本历史，包括重命名：
```
$ git log --follow [file]
```

展示两个分支之间的内容差异：
```
$ git diff [first-branch]...[second-branch]
```

输出指定commit的元数据和内容变化：
```
$ git show [commit]
```

将文件加入版本控制：
```
$ git add [file]
```

提交文件，将文件快照永久地记录在版本历史中：
```
$ git commit -m "[descriptive message]"
```

### 重做提交
撤销所有 [commit] 后的的提交，在本地保存更改：
```
$ git reset [commit]
```
放弃所有历史，改回指定提交:
```
$ git reset --hard [commit]
```
### 与远程库同步
下载远端跟踪分支的所有历史：
```
$ git fetch
```

将远端跟踪分支合并到当前本地分支：
```
$ git merge
```

将所有本地分支提交上传到 GitHub：
```
$ git push
```

使用来自 GitHub 的对应远端分支的所有新提交更新你当前的本地工作分支。git pull 是 git fetch 和 git merge 的结合：
```
$ git pull
```

### 参考：
* https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository
* https://github.github.com/training-kit/downloads/zh_CN/github-git-cheat-sheet/
