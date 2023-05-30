---
title: Github 
tags: Github
---

Github

生成密钥添加到github

```
ssh-keygen -t rsa -C "zhangwenlong"


注意：这里的 xxxxx@xxxxx.com 只是生成的 sshkey 的名称，并不约束或要求具体命名为某个邮箱。
现网的大部分教程均讲解的使用邮箱生成，其一开始的初衷仅仅是为了便于辨识所以使用了邮箱。
```

添加到对应的settings的ssh keys

测试命令

```
ssh -T git@gitee.com
ssh -T git@github.com
```



```
#gitee
Host gitee.com
HostName gitee.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa_gitee

# github
Host github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/id_rsa_github
```

常用的git命令

```

```

修改git的配置

```
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=D:/soft/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
http.sslverify=true
user.name=不知名程序员
user.email=1934024945@qq.com
alias.br=branch -av
alias.ca=commit --amend
alias.ci=commit
alias.co=checkout
alias.cp=cherry-pick
alias.dc=diff --cached
alias.dh=diff HEAD
alias.di=diff
alias.lg=log --pretty=format:'%h |%an |%ai |%s'
alias.lo=log --pretty=format:'%h |%an |%s' --since='4 days ago'
alias.oneline=log --pretty=oneline --since='2 days ago'
alias.onelog=log -p -1
alias.pl=pull
alias.rb=rebase
alias.rr=reset HEAD
alias.st=status
color.status=auto
color.branch=auto
color.ui=auto
color.diff=auto
color.interactive=auto
push.default=matching
rerere.autoupdate=no
http.sslverify=false
color.diff=true
color.status=true
color.branch=true
push.default=matching
pull.rebase=true
pull.ff=only
core.autocrlf=true
core.filemode=false
```

