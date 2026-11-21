---
date: 2026-11-03T01:10:22+08:00
draft: false
title: Git 概述与安装
weight: 2
---

## Git 是什么

Git 是一个**开源**的**分布式**版本控制系统，用于敏捷高效地处理任何或小或大的项目。

Git 是 *Linus Torvalds* 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。

Git 与常用的版本控制工具 CVS, Subversion 等不同，它采用了分布式版本库的方式，不必服务器端软件支持。

如今，Git 已经成为了世界上最常用的 VCS。

## Git 的安装

可以参考 [Git-SCM 上的安装教程](https://git-scm.com/install/)。

> 需要注意的是，许多 Linux 发行版预装了 Git。可以使用 `git --version` 来检查。

当你得到了类似这样的结果，就说明已经成功安装了 Git！

    git version 2.53.0

## Git 的基本配置

Git 中的每次提交都会记录提交者的**名字**和**邮箱**，可以使用以下命令来配置：

```bash
git config --global user.name 你的名字
git config --global user.email 你的电子邮箱
```

`core.editor` 可以配置 Git 使用哪个文本编辑器，默认情况一般是 Vi 或 Vim。  
如果你安装了 VS Code ，可以通过以下命令来设置：

```bash
git config --global core.editor "code --wait"
```

其他编辑器不再赘述。