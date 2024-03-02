### git命令

```shell
git add file
```

```
git init
```

将文件添加到暂存区



```shell
git status(gs)
```

查看文件状态



```shell
git commit
```

提交文件



```shell
git log
```

查看日志（提交文件时间）：

```shell
$ git log
commit 74feb4fcbffb0dc9e64c5f9af4c5eef9e3bbbd98 (HEAD -> master)
Author: Mortis <471917017@qq.com>
Date:   Sun Jan 21 19:52:42 2024 +0800

74fe..是哈希值
 git log --all --graph --decorate --oneline
 (其被改成gla)
```

**head**是指针，在这个文件时，查看文件，其内容是这个文件提交的内容，在其他提交活动时，查看文件内容是当时提交的内容



```shell
git checkout head/master/74feb4（即哈希值）
```

改变head的位置(改变工作目录):

```
$ git checkout master
Switched to branch 'master'

sourcookie@cool- MINGW64 /d/play/demo (master)
$ cat animal.py
切换工作目录，cat快照，就会显示之前的快照
想要显示修改后的快照，需要切换工作目录（git checkout),再cat
文件。前提：修改后的文件需要git add再 git commit 形成快照才行
```





```shell
git diff df1868 head
git diff
```

查询df1868（哈希值）到与head此时在的提交记录的差别：

```shell
$ git diff df1868ca56ad2886 head
diff --git a/hello.txt b/hello.txt
index c7e799d..8b3d116 100644
--- a/hello.txt
+++ b/hello.txt
@@ -1,2 +1,3 @@
 hello
 we fkman
+fk man

增加了fk man
第一行是command
```





```
vim animal.py/she.sh
查看文件并进行修改，修改后在Normal模式下用Ctrl+:进行指令输入
wq是修改后退出，q是退出，q！是不保存修改退出  

```





```
git merge  合并分支
git merge --abort 上一个命令的撤销动作
git branch 创建分支
git branch -vv 分支所有信息
git checkout -b dog 创建dog分支并切换到dog上
```

```
git add file 先添加文件再
git merge --continue 告诉git解决了合并冲突
```





```
git remote 远程仓库
git remote add name（远程仓库）URL    与远程仓库连接
```





```
git push <remote> <local branch>:<remote branch>
:
git push origin(远程仓库名) master:master
git push -f origin master:master
//本地文件强制覆盖远程

将本地的merge push到remote的master上

简便：
git branch --set-upstream-to=origin/master

eg:
$ git branch --set-upstream-to=origin/master
branch 'master' set up to track 'origin/master'.

sourcookie@cool- MINGW64 /d/play/demo (master)
$ git branch -vv
  cat    e6e6d84 fix it
  dog    c39808e add dog()
* master 26496ab [origin/master: ahead 1] x
本地的master和origin（远程仓库即remote）/master绑定
下次只要git push而不用
git push origin/master:master
```



```
git clone <url> <folder name>
```



```
git fetch     push后远程仓库用来更新仓库内容
```

在这之后remote中：

```
git pull     将origin/master合成到master

eg：

* 26496ab (origin/master, origin/HEAD) x
*   f0852b5 (HEAD -> master) Merge branch 'dog'

git pull后：
* 26496ab (HEAD -> master, origin/master,
origin/HEAD) x
*   f0852b5 Merge branch 'dog'
```

