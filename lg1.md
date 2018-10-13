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