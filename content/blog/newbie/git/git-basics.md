---
date: 2026-11-21T18:17:51+08:00
draft: true
title: Git 基本操作
weight: 4
---

## git init

在终端中切换到想要创建仓库的目录，或者创建一个新目录：

```bash
mkdir example-project
cd example-project
```

然后，初始化仓库。

```
git init
```

会在当前目录下新建一个 `.git` 文件夹。

也可以在指定目录下初始化仓库：

```
git init example-project
```

这个命令会在 `example-project` 目录下新建。

## git add / git commit

想要把一个**已有**文件加入仓库中，只需要使用 `git add` 即可。

```bash
git add README.md # 添加 README.md
git add src/      # 添加 src 目录
git add *.rs      # 可以使用 GLOB 语法来匹配多个文件
git add .         # 添加当前目录（即所有文件，不包括 .git 目录）
git add -A        # 添加所有文件，等效于上一条
```

> [!NOTE]
> 使用 `git add *` 时，以 `.` 开头的文件不会被匹配，如 `.gitignore`  
> 如果需要，可以使用 `git add .` 或 `git add -A`

add 后的文件会存在**暂存区**，不会真正保存下来。

添加完所有需要的文件后，可以使用 `git commit` 指令来创建提交。

```bash
git commit
```

使用这个指令会打开配置的编辑器，要求你提供提交消息，其中以 `#` 开头的行会被忽略。  
写好后保存、关闭，即可创建一次提交。

也可以使用 `-m` 选项在命令行中指定提交消息。

```bash
git commit -m "这里是提交消息"
```

> [!NOTE]
> 提交后，暂存区会被清空，下次提交前必须再次使用 `git add`。  
> 可以在 `git commit` 中使用 `-a` 选项跳过这一步，不过不会添加未追踪的文件。