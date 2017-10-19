# Git

 Git是免费的,开源的,分布式版本控制系统.

* init
* add
* commit
* log
* diff
* status
* reflog
* reset
* checkout
* clone
* remote

 Git 是目前世界上最先进的分布式版本控制系统(没有之一)
 Git 什么是版本库呢? 版本库就是简单理解成一个目录,这个目录里面的所有文件都可以被Git管理起来
 所以，创建一个版本库非常简单，首先，选择一个合适的地方，创建一个空目录： 
 $ mkdir learngit
 $ cd learngit
 $ pwd
 /Users/michael/learngit
​	

# 时光穿梭机

我们已经成功地添加并提交了一个readme.txt文件，现在，是时候继续工作了，于是，我们继续修改readme.txt文件，改成如下内容：

```
Git is a distributed version control system.
Git is free software.
```

现在，运行`git status`命令看看结果：

```
$ git status
# On branch master
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#    modified:   readme.txt
#
no changes added to commit (use "git add" and/or "git commit -a")
```

`git status`命令可以让我们时刻掌握仓库当前的状态，上面的命令告诉我们，readme.txt被修改过了，但还没有准备提交的修改。

虽然Git告诉我们readme.txt被修改了，但如果能看看具体修改了什么内容，自然是很好的。比如你休假两周从国外回来，第一天上班时，已经记不清上次怎么修改的readme.txt，所以，需要用`git diff`这个命令看看

```
$ git diff readme.txt 
diff --git a/readme.txt b/readme.txt
index 46d49bf..9247db6 100644
--- a/readme.txt
+++ b/readme.txt
@@ -1,2 +1,2 @@
-Git is a version control system.
+Git is a distributed version control system.
 Git is free software.
```

