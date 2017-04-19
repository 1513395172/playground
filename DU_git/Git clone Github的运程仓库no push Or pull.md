# Git clone Github的运程仓库(no push/pull)

### 目标
Git clone Github的运程仓库(no push/pull)

### 命令行
`$ git clone git@github.com:zhangshiyinrunwithcc/playground.git`

### 前置步骤
1. 采用SSH与Github交互方式
2. 想要clone的仓库确实存在在Github上
3. 想要clone的仓库SSH 地址为 git@github.com:zhangshiyinrunwithcc/playground.git


### 命令行+终端返回

```
zhangshingdeAir:desktop zhangshiying$ git clone git@github.com:zhangshiyinrunwithcc/playground.git
Cloning into 'playground'...
Enter passphrase for key '/Users/zhangshiying/.ssh/id_rsa':
remote: Counting objects: 81, done.
remote: Compressing objects: 100% (60/60), done.
remote: Total 81 (delta 29), reused 70 (delta 18), pack-reused 0
Receiving objects: 100% (81/81), 20.19 KiB | 0 bytes/s, done.
Resolving deltas: 100% (29/29), done.
```

### 检验
1. 终端返回done
2. 本地查看 想要clone的仓库 的确已经存在在指定目录中
3. 且想要clone的仓库 文件与Github仓库里文件确实一致


### 参考
http://blog.csdn.net/skysky01/article/details/51678692

Timelog 
实验+记录+发布 26mins
