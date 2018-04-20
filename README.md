# learngit

## 远程
要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；

关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

----
Git支持多种协议，包括https，但通过ssh支持的原生git协议速度最快。

某些只开放http端口的公司内部就无法使用ssh协议而只能用https

----

## 分支管理

git merge dev

git merge命令用于合并指定分支dev到当前分支

Git用<<<<<<<，=======，>>>>>>>标记出不同分支的内容，我们修改后保存

git add readme.txt 

git commit -m "conflict fixed"

git log --graph命令可以看到分支合并图

合并分支时，加上--no-ff参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而fast forward合并就看不出来曾经做过合并

当手头工作没有完成时，先把工作现场git stash一下，然后去修复bug，修复后，再git stash pop，回到工作现场。

如果之前远程没有dev: git push origin dev 给远程创建了一个dev

---

你的小伙伴要在dev分支上开发，就必须创建远程origin的dev分支到本地，于是他用这个命令创建本地dev分支：

git checkout -b dev origin/dev

修改

git push origin dev // 不需要origin/dev

git branch --set-upstream dev origin/dev // 以后在dev上git pull的话 直接从origin/dev上pull

------
查看远程库信息，使用git remote -v；

本地新建的分支如果不推送到远程，对其他人就是不可见的；

从本地推送分支，使用git push origin branch-name，如果推送失败，先用git pull抓取远程的新提交；

在本地创建和远程分支对应的分支，使用git checkout -b branch-name origin/branch-name，本地和远程分支的名称最好一致；

建立本地分支和远程分支的关联，使用git branch --set-upstream branch-name origin/branch-name；

从远程抓取分支，使用git pull，如果有冲突，要先处理冲突。


