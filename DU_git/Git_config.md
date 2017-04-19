# Git config 配置

### 目标
- 在刚刚git clone到本地的github仓库zhangshiyinrunwithcc/playground配置git config username和email
- 检查本地的desktop/playground)git config的username和email

### 命令行
`git config --list`
`git config user.name`
`git config user.email`

### 前置
1. 从Github上git clone了zhangshiyinrunwithcc/playground远程仓库到本地desktop的目录下
2. 之前在其他仓库曾经使用过命令 `git config --global user.name "zhangshiyinrunwithcc"` 和`git config --global user.email "981318360@qq.com"

### 命令行以及终端返回

```
zhangshingdeAir:desktop zhangshiying$ cd playground
zhangshingdeAir:playground zhangshiying$ git config --list
core.excludesfile=~/.gitignore
core.legacyheaders=false
core.quotepath=false
core.pager=less
mergetool.keepbackup=true
push.default=simple
color.ui=auto
color.interactive=auto
repack.usedeltabaseoffset=true
alias.s=status
alias.a=!git add . && git status
alias.au=!git add -u . && git status
alias.aa=!git add . && git add -u . && git status
alias.c=commit
alias.cm=commit -m
alias.ca=commit --amend
alias.ac=!git add . && git commit
alias.acm=!git add . && git commit -m
alias.l=log --graph --all --pretty=format:'%C(yellow)%h%C(cyan)%d%Creset %s %C(white)- %an, %ar%Creset'
alias.ll=log --stat --abbrev-commit
alias.lg=log --color --graph --pretty=format:'%C(bold white)%h%Creset -%C(bold green)%d%Creset %s %C(bold green)(%cr)%Creset %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative
alias.llg=log --color --graph --pretty=format:'%C(bold white)%H %d%Creset%n%s%n%+b%C(bold blue)%an <%ae>%Creset %C(bold green)%cr (%ci)' --abbrev-commit
alias.d=diff
alias.master=checkout master
alias.spull=svn rebase
alias.spush=svn dcommit
alias.alias=!git config --list | grep 'alias\.' | sed 's/alias\.\([^=]*\)=\(.*\)/\1\     => \2/' | sort
include.path=~/.gitcinclude
include.path=.githubconfig
include.path=.gitcredential
diff.exif.textconv=exif
credential.helper=osxkeychain
user.name=zhangshiyinrunwithcc
user.email=981318360@qq.com
github.user=zhangshiyingrunwithcc
credential.helper=osxkeychain
core.excludesfile=/Users/zhangshiying/.gitignore_global
difftool.sourcetree.cmd=opendiff "$LOCAL" "$REMOTE"
difftool.sourcetree.path=
mergetool.sourcetree.cmd=/Applications/SourceTree.app/Contents/Resources/opendiff-w.sh "$LOCAL" "$REMOTE" -ancestor "$BASE" -merge "$MERGED"
mergetool.sourcetree.trustexitcode=true
commit.template=/Users/zhangshiying/.stCommitMsg
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
core.ignorecase=true
core.precomposeunicode=true
remote.origin.url=git@github.com:zhangshiyinrunwithcc/playground.git
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
branch.master.remote=origin
branch.master.merge=refs/heads/master
zhangshingdeAir:playground zhangshiying$ git config user.name
zhangshiyinrunwithcc
zhangshingdeAir:playground zhangshiying$ git config user.email
981318360@qq.com
```

### 检验
1. 使用`git config user.name` 终端返回 zhangshiyinrunwithcc(本人githubID)
2. 使用`git config user.email` 终端返回 981318360@qq.com（本人邮箱）
证明配置正确, 可以进行下一步

### 参考

[1](http://blog.csdn.net/joe_007/article/details/7276195)
[2](http://blog.csdn.net/skysky01/article/details/51678692)
[3](http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)

Timelog 构思 + 记录 +发布 26mins
