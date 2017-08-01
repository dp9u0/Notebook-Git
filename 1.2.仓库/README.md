> **主要内容** : 如何在本地建立一个仓库: 通过直接在本地建立一个新的仓库的方式 或者通过克隆已有的远程仓库到本地的方式

版本库又叫做仓库(repository),可以理解为一个目录,该目录里面所有文件都被Git管理,Git会记录所有文件的变更历史等信息.

# 创建本地仓库

```
$ mkdir Git-Test
$ cd Git-Test
λ  pwd
C:\Users\guodp\Git-Test
$ git init
Initialized empty Git repository in C:/Users/guodp/Git-Test/.git/
$ ls -al
total 20
drwxr-xr-x 1 guodp 197609 0 Aug  1 14:37 .
drwxr-xr-x 1 guodp 197609 0 Aug  1 14:37 ..
drwxr-xr-x 1 guodp 197609 0 Aug  1 14:37 .git
```

# 克隆远程仓库

假设已经有一个远程仓库地址,并且有权限访问,可以将远程仓库clone到本地作为一个本地仓库进行操作

关于远程仓库的创建会在[2.4.Git服务](../2.4.Git服务/README.md)章节介绍.

git 传输协议有git https 和本地文件路径几种,这个会在[2.6.Git原理](../2.6.Git原理/README.md)章节介绍。这里只需要知道,远程仓库会有一个地址来表示就可以.

```
$ git clone https://github.com/dp9u0/Notebook.git # 地址
Cloning into 'Notebook'...
remote: Counting objects: 26, done.
remote: Compressing objects: 100% (18/18), done.
remote: Total 26 (delta 12), reused 16 (delta 8), pack-reused 0
Unpacking objects: 100% (26/26), done.

$ cd Notebook\

$ pwd
/c/Users/guodp/Notebook
```

通过上述两种方式就建立了本地仓库.

> 有兴趣的同学可以了解一下这个命令: git init --bare,这个命令可以创建一个空的仓库,这个仓库只能作为远程仓库使用,不可以直接进行提交等操作.


