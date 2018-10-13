# 廖雪峰Git教程

Git is a distributed version control system.
Git is free software.

## 创建版本库

- 初始化Git仓库，用 git init 命令。
- 添加文件到Git仓库
    1. git add file1.txt file2.txt，追踪文件。 <!-- 没有stage？ -->
    1. git commit 提交变更。

## 时光机穿梭

- git status 查看工作区状态。
- git diff 查看修改内容。

### 版本回退 rollback

- git reset --hard HEAD^ 回退到上一个版本
- git reset --hard HEAD~n 回退到前n个版本
- git reset --hard `commit_id` 回到指定id的版本
- git log 查看<b>当前版本之前</b>的提交历史，以便确定要回退到哪个版本
- git reflog 查看命令历史，可以看到所有提交版本的记录

### 工作区和暂存区

- 工作区：workspace, working directory
- 暂存区：stage
- 版本库：repository

@import "workspace_repository.png"

@import "git_add.png"

@import "git_commit.png"

- git add 命令实际上是把要提交的所有修改放到暂存区——stage。
- git commit 则把暂存区的内容全部提交到`分支`

### 管理修改

- Git 管理和跟踪的是"修改"，而不是文件本身。没有跟踪(staged)的修改，版本库不会将其记录在内。
- 没有 `git add` 到 stage 的修改不会被加入到 `commit`中。

### 撤销修改

1. 撤销工作区某个文件被修改但没有stage的内容：git checkout -- file.txt
1. 撤销已经stage的修改：
    1. git reset HEAD file.txt
    1. git checkout -- file.txt

### 删除文件

- 从版本库中删除文件
  1. git rm file.txt
  1. git commit <!-- 删除后要提交 -->
- 从版本库恢复工作区中被删除文件
  - git checkout -- file.txt

`git checkout`其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。

ssh-keygen -t rsa -b 4096 -C "buffalo_d@163.com"
