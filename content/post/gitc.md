---
date: "2020-01-05"
title: Basic Git Commands
slug: git
---

[git中文文档](https://git-scm.com/book/zh/v2)

[阮一峰 Git 教程](https://www.bookstack.cn/read/git-tutorial/README.md)

初始化仓库

```
git init
```

Git 克隆

Git克隆功能类似于下载。一般常用于下载github repo。
在指定的文路径打开终端或git bash，之后找到需要下载的库的http协议或ssh协议输入如下命令，

```
git clone git@github.com:ECSTA7Y/txtnb.git
```

```
git status # 查看自己所处分支 查看改变的文件
git status -s # 加-s参数，以获得简短的结果输出
```

```
git diff # 查看文件的具体改变。git status 的结果的详细信息
git diff --stat # 显示摘要而非详细信息
```

```
git branch # 查看本地分支
git checkout -b branch2 # 创建分支
git checkout master # 切换分支
```

```
git add . # 需要提交的文件
git commit -m 'description' # 提交说明，在引号内说明你做了什么改动。-m参数用于指定提交说明。是必须的。
```
`-a`参数用于先将所有工作区的变动文件，提交到暂存区，再运行`git commit`。用了`-a`参数，就不用执行`git add .`命令了。

```
git commit -am "message" 
```

推送

如果当前分支与多个主机存在追踪关系，则可以使用-u选项指定一个默认主机，这样后面就可以不加任何参数使用git push。

```
git push origin master # 推送
git push -u origin master 
```

将别人的项目克隆到本地：

```
git clone [url]
```

查看提交历史：

`git log` 命令可以显示所有提交过的版本信息，但回退后无法看到被删除的 commit的版本信息。

```
git log
git log --oneline # 简洁版本
```

`git reflog`可以显示已经被删除的 `commit`记录和 `reset`的操作。也就是说，`git reflog` 可以查看所有分支的所有操作记录。

```
git reflog
```

版本回退

```
git reset --hard HEAD^ # 回退到上一个版本

git reset --hard 1094a # 指定回到未来版本，1094a为版本号
```
版本回退后再push[可能会出错](https://guozh.net/git-pushtijiaochenggonghouruhechexiaohuitui/)。因为当前分支的版本低于远程分支的版本，所以要想覆盖掉它，必须使用force。

```
git push origin master -–force
```




---

Linux(Ubuntu) Git Install

```
sudo add-apt-repository ppa:git-core/ppa
sudo apt-get update
sudo apt-get install git  
```
Some tips: Linux system could access Windows files, thus I could edit them. It is very convenient to use Ubuntu 18.04 to finish all tasks.  

# 将本地git仓库与远程仓库相关联

https://blog.csdn.net/qq_35246620/article/details/69668846


```
git init 
git remote add
git remote -v
git pull origin master
```
再进行push操作


