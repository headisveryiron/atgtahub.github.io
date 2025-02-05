---
layout: post
title:  Git常用命令
categories: vcs
tag: git
---


* content
{:toc}


## 设置提交用户名和邮箱

```sh
git config user.name "username"

git config user.email "x@xx.com"
```

### 设置提交用户名和邮箱(全局)

```sh
git config --global user.name "username"

git config --global user.email "x@xx.com"
```


## 初始化git

```sh
git init
```


## 添加到暂存区

```sh
git add x.txt
```


## 提交到本地仓库

```sh
git commit -m "comment"
```


## 设置远程仓库地址

```sh
git remote add origin <git path>
```


## 拉取远程分支与本地分支合并

```sh
git pull origin master:master
```


## 推送到远程仓库

```sh
git push -u origin master
```


## 撤销提交记录

### 参数-soft
保留本次代码改动，撤销commit，不撤销git add
```sh
git reset --soft <commit id>
```

### 参数-hard
不保留本次代码改动，撤销commit，撤销git add
```sh
git reset --hard <commit id>
```


## 撤销本次提交记录
head^是指当前commit
```sh
git reset --soft head^

git reset --soft <commit id>
```

## 撤销指定几个commit

```sh
git reset --soft head~<1>
```


## 分支

### 新建分支

```sh
git branch <branch name>
```

### 切换分支

```sh
git checkout <branch name>
```

### 新建并切换分支

```sh
git checkout -b <branch name>
```

### 查看当前分支

```sh
git branch
```

### 删除分支

```sh
git branch -d <branch name>
```

### 合并分支
合并指定分支到当前分支
```sh
git merge <branch name>
```


## 克隆仓库

```sh
git clone <git path>
```


## 查看仓库当前的状态

```sh
git status
```


## 比较变动

```sh
git diff
```


## 查看日志

```sh
git log
```

一行输出
```sh
git log --pretty=oneline
```

- commit xx: 提交id
- Merge: xx: 合并的记录
- Author：xx：提交用户信息
- Date：xx：提交时间
- feat(posts): xxx：提交信息

```text
commit xx
Author: xx <xx@xx.com>
Date:   xx

    feat(posts): xxx

```


## 查看git-url

```sh
git ls-remote --get-url origin
```
