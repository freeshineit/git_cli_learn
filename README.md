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

## 查看文件状态

查看项目路径下全部已修改文件（add的文件和没有add的文件）

> git status

> git status .

## 添加变动的文件

使用下面命令查看`git add`的帮助

> git add --help

+   添加当前目录下所有文件变化(当把`.`换成文件文件或文件夹,则是添加这个文件夹或文件)
    >   git add .

+   添加项目所有文件变化
    > git add --all

## commit

把之前添加到缓存中的文件添加一个commit日志

>   git commit -m '更新代码'

提交本地的所有修改问文件(不包括新建文件)并在控制面板中添加提交日志(如果没有日志信息，不会提交日志)

>   git commit -a

修改上一次提交的日志(使用请注意，最好不要使用)

>   git commit --amend


## 查看提交日志记录

>   git log

查看指定文件提交记录（会展示文件的具体修改）
>   git log -p index.js

查看文件内容具体修改，展示每一行修改记录，记录包括时间、作者和内容（这个很有用）
>   git blame README.md

## 查看与上次提交版本文件的不同

>   git diff

>   git diff index.js

## 分支

基于当前分支新建分支
>   git branch new-branch

查看所有分支（包括远程和分支最新的`commit`）
>   git branch -av

切换分支，切换到`develop`分支
>   git checkout develop

删除本地xxx分支（不可以删除当前分支）
>   git branch -d xxx

## 标签

给当前提交打一个标签（一般用于版本好更新时）
>   git tag new-tag

发布标签
>   git push --tags

## 更新与发布

查看远程端
>   git remote -v

把本地版本推到远程
>   git push \<remote\> \<branch\>

🌰

>   git push origin develop

删除远程分支(删除的是远程跟踪, 不是删除远程分支)

>   git branch -dr <remote/branch>

🌰
>   git branch -dr origin/test

删除远程分支
>   git push origin --delete \<branch\>

🌰
>   git push origin --delete test

强制推送（发布），这样会把远程版本覆盖
>   git push origin \<branch\> -f

## 拉取

不会自动合并
>   git fetch \<remote\>

自动合并
>   git pull \<remote\> \<branch\>

## 合并


合并分支到当前分支
>   git merge \<branch\>

[fatal: refusing to merge unrelated histories](https://stackoverflow.com/questions/37937984/git-refusing-to-merge-unrelated-histories-on-rebase)

>   git merge --allow-unrelated-histories \<branch\>

## 重置

当前版本重置到分支中（请误重置已经发布的提交）
>   git rebase \<branch\>

退出重置
>   git rebase --abort

解决冲突后继续重置
>   git rebase --continue



## 撤销

放弃工作目录下的所有修改
>   git reset --hard HEAD

放弃指定文件的所有本地修改
>   git checkout HEAD \<file\>

返回到上一次添加当前文件之前（从缓存区中移除出去）
>   git reset HEAD .

返回指定comimt的提交版本
>   git reset \<commit\>

将HEAD 重置d到上一次提交的版本并抛弃该版本之后的所有修改
>   git reset --hard \<commit\>


## 添加远程源(关联远程源)

>   git remote add origin git@github.com:freeshineit/git_cli_learn.git



    
