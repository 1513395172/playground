# SSH连接Github提问

环境OS X, 当我打开终端输入`ssh -T git@github.com`时, 终端返回 `ssh: connect to host github.com port 22: Operation timed out`

我进行了如下排查

- 输入`ls -al ~/.ssh`
- 返回
```
total 24
drwx------   5 zhangshiying  staff   170 Dec  3 10:31 .
drwxr-xr-x+ 51 zhangshiying  staff  1734 Apr 17 15:26 ..
-rw-------   1 zhangshiying  staff  1766 Apr 14 11:37 id_rsa
-rw-r--r--   1 zhangshiying  staff   398 Dec  3 10:49 id_rsa.pub
-rw-r--r--   1 zhangshiying  staff  1199 Apr 14 11:23 known_hosts
```

- 输入`eval "$(ssh-agent -s)"`
- 返回
```
Agent pid 4837
```

- 输入`open ~/.ssh/config`
- 返回
```
 Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa
```
 
- 输入`ssh-add`
- 返回`Enter passphrase for /Users/zhangshiying/.ssh/id_rsa:`

- 输入 `ENTER`
- 没有返回任何东西

- 输入`ssh -T git@github.com`
- 返回`ssh: connect to host github.com port 22: Operation timed out`

- 输入`eval "$(ssh-agent -s)"`
- 返回`Agent pid 5005`

- 输入`ssh-add -l`
- 返回`The agent has no identities.`

请问 我是不是错在~/.ssh/config的文件里的`Host *`里？
