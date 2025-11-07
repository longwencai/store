#  Git学习笔记

## 一、git本地操作的三个区域

- git仓库：最终确定的文件保存到仓库，成为一个新版本，并且对他人可见

git status

- 暂存区：暂存已经修改的文件最后统一提交到git仓库中

git commit-m"提交描述"/git status

- 工作区：添加，编辑，修改文件等动作

git add/git status



## 二、本地仓库操作

#### 仓库：即版本库，可以理解为是一个目录用于存放代码的，整个目录的所有文件都可以被git管理起来，每个文件的修改、删除等操作git都能跟踪到

1）配置git bash

桌面空白右键，点击”git bash here“以打开git命令窗口
```
$ git config --global user.name"用户名"
$ git config --global user.email"邮箱地址"
```

2）创建仓库

开始学最好是创建一个空目录，也不要是中文名目录
```
$ mkdir pro-git
```

在命令行中进入项目pro-git
```
$ cd pro-git
```

git仓库初始化（让git知道，它需要管理这个目录）

==表现==：执行之后的项目目录下创建”git“的隐藏目录，这个目录值git所创建的，不能删除，也不能随意更改其中的内容。

```
$ git init
```

3）git常用的指令操作

查看当前状态：git status
添加到缓冲区：git add 文件名

```
说明：git add指令，可以添加一个文件，也可以同时添加多个文件
语法一：git add 文件名
语法二：git add 文件名1 文件名2...
语法三：git add. 【添加当前目录到缓存区中】
```

提交至版本库：git commit-m"注释内容"

在后续对于文件（可以操作一个或多个）操作之后，重复使用git add与git commit 指令即可

## 三、git的版本回退

1）查看版本，确定需要回到的时间点	

​		指令：

​          			git log

​					  git log --pretty=oneline

2)回退操作：

​		指令：

​       				git reset --hard  提交步骤1查看到的编号

==注意==：回到过去之后，要想再回到之前最新的版本的时候，则需要使用指令去查看历史操作，以得到最新的commit id 

​		指令：git reflog新id

- 要想回到过去，必须的到commit id,然后通过git reset -hard 进行回退
- 要想回到未来，需要使用git reflog进行历史操作查看，得到最新的commit id
- 回退指令不需要写全，会自动识别，前4位即可

git status 	 查看文件状态

git add      	将文件的状态加入暂存区

git reset    	将暂存区的文件取消暂存或者切换到指定版本

git commit   将暂存区的文件修改到版本库

git log        	查看日志

## 四、远程仓库的操作

1.创建空目录，名称为shop

2.使用clone指令克隆线上仓库到本地

语法：git clone 线上仓库地址

3.在仓库上做对应操作（提交暂存区，提交本地仓库，提交线上仓库，拉去线上仓库）

git remote          			查看远程仓库

git remote add   		   添加远程仓库

git clone						 从远程仓库克隆	

git pull							从远程仓库拉取

git pull							推送到远程仓库

```
git remote add origin (库址)
git push origin master(把本地仓库的代码推送到远程仓库)
```

