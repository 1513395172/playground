# 远程库同步git_fetch

### 目标
1. 下载远程仓库的所有变动

### 命令行
`git status`
`git fetch origin master`
`git log -p master...origin/master`
`git merge origin/master`

### 检验
1. 本地仓库playground的确更新了远程库的文件
2. 远程库现在文件和本地库一致


### 参考
[1](http://blog.csdn.net/skysky01/article/details/51678692)
[2](http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)
[3](http://blog.csdn.net/hudashi/article/details/7664457)
[4](https://ruby-china.org/topics/4768)

### 命令行以及终端返回
```
zhangshingdeAir:playground zhangshiying$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean

zhangshingdeAir:playground zhangshiying$ git fetch origin master
Enter passphrase for key '/Users/zhangshiying/.ssh/id_rsa':
remote: Counting objects: 16, done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 16 (delta 9), reused 11 (delta 4), pack-reused 0
Unpacking objects: 100% (16/16), done.
From github.com:zhangshiyinrunwithcc/playground
 * branch            master     -> FETCH_HEAD
   b1e4219..6eb5f0c  master     -> origin/master

zhangshingdeAir:playground zhangshiying$ git log -p master...origin/master
commit 6eb5f0cbfe0ef07493bd1e3c47e590b1ead41b6d
Author: zhangshiying <981318360@qq.com>
Date:   Wed Apr 19 10:51:20 2017 +0800

    Create Git_config.md

diff --git a/DU_git/Git_config.md b/DU_git/Git_config.md
new file mode 100644
index 0000000..f7ec1c1


zhangshingdeAir:playground zhangshiying$ git merge origin/master
Updating b1e4219..6eb5f0c
Fast-forward
 ...t clone Github的运程仓库no push Or pull.md | 38 +++++++++
 DU_git/Git_config.md                               | 90 ++++++++++++++++++++++
 2 files changed, 128 insertions(+)
 create mode 100644 DU_git/Git clone Github的运程仓库no push Or pull.md
 create mode 100644 DU_git/Git_config.md

zhangshingdeAir:playground zhangshiying$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean

```

### 后续思考
1. origin master明显是远程库的master分支, 那么origin/master就是本地库的master分支吗？
2. `git log -p master...origin/master`中的master是指远程库上的master分支吗？
3. 暂存区/工作区/仓库区有何不同？
4. 远程仓库同步的git pull 与 git fetch 有何不同？
5. 有没有更方便更美观的检验git status的方式？
