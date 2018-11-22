# git_cli_learn

git 只关注内容

## clone （克隆）

克隆项目

>   git clone git@github.com:freeshineit/git_cli_learn.git

克隆项目并重命名

>   git clone git@github.com:freeshineit/git_cli_learn.git  xxxx

## 项目git初始化 

>   git init

这个命令会在当前目录下生成一个`.git`文件夹， 并创建一个`master`分支

## 添加变动的文件

使用下面命令查看`git add`的帮助

> git add --help

+   添加当前目录下所有文件变化(当把`.`换成文件文件或文件夹,则是添加这个文件夹或文件)
    >   git add .

+   添加项目所有文件变化
    > git add --all


## 查看文件状态

查看项目路径下全部已修改文件（add的文件和没有add的文件）

> git status

> git status .

## 查看与上次提交版本文件的不同



## reset

+   返回到上一次添加当前文件之前（从缓存区中移除出去）
    >   git reset HEAD .


## 添加远程源(关联远程源)

>   git remote add origin git@github.com:freeshineit/git_cli_learn.git



    
