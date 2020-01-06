---
date: "2020-01-05"
title: Basic Git Command
---

[git中文文档](https://git-scm.com/book/zh/v2)

[阮一峰 Git 教程](https://www.bookstack.cn/read/git-tutorial/README.md)

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

```
git log
git log --oneline # 简洁版本
```

版本回退

```
git reset --hard HEAD^ # 回退到上一个版本

git reset --hard 1094a # 指定回到未来版本，1094a为版本号
```











