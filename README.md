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

