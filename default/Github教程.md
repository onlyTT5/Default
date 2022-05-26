# Github教程

[TOC]

## 一、注册账号

## 二、Git初体验及常用命令

> ```
> git status
> ```
>
> 查看仓库状态



> ```
> git init
> ```
>
> 初始化Git仓库



> ```
> git add [文件名]
> ```
>
> 将文件名添加到Git仓库



> ```
> git commit 
> git commit "text commit"
>```
> 
> 将文佳佳文件添加到Git仓库



> git log
>
> 打印Git仓库日志



> ```
> git branch
> ```
>
> 查看Git仓库的分支情况
>
> ```
> git branch a
> ```
>
> 创建一个名为a的分支



> ```
> git checkout a
> ```
>
> 切换到a的分支
>
> ```
> git check b -b
> ```
>
> 创建分支的同时，直接切换到新分支



> ```
> git merge 
> git merge a 
> ```
>
> 切换到master分支将a分支合并到master分支（冲突不能直接合并）



> ```
> git branch -d & git branch -D
> ```
>
> 输入`git branch -d a`命令，删除a分支
>
> 删除不了用`git branch -D`强制删除



> ```
> git tag
> ```
>
> 输入`git tag v1.0`命令，为当前分支添加标签
>
> ```
> git checkout v1.0
> ```
>
> 可切换到该标签下代码

## 利用SSH完成Git与Github的绑定

### 生成SSHkey

> ```
> ssh
> ```
>
> 查看是否安装SSH



> ```
> ssh-keygen -t rsa
> ```
>
> 用指定RSA算法生成密钥，三次回车生成两个文件。
>
> 即密钥id_rsa和公钥id_rsa.pub



> ```
> ssh -T git@github.com
> ```
>
> 验证绑定是否成功



> ```
> git clone ...
> ```
>
> 把远程仓库clone到本地

### 第一种方法：本地没有Git仓库

> ```
> git add src/
> git commit -m "commit src file"
> ```
>
> 将文件add并commit到仓库



> ```
> git push origin master
> ```
>
> 将远程仓库push到仓库

### 第二种方法：本地有Git仓库

#### pull

> ```
> git init
> git remote add origin [链接]
> ```
>
> 关联远程仓库



> ```
> git pull origin master
> ```
>
> 同步远程仓库和本地仓库

#### push

> ```
> git add [文件]
> git commit -m "add [文件] file"
> ```
>
> 将[文件]添加并提交到仓库
>
> 在输入`git push origin master`命令，将本地仓库修改至远程仓库





