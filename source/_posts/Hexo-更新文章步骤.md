---
title: Hexo 更新文章步骤
date: 2022-04-21 19:39:35
categories:
tags: 博客
---

使用 VS Code 写文章，前提已经使用 [GitHub Pages](https://hexo.io/docs/github-pages) 配置好博客。

1. 用 VS Code 打开 Hexo 博客位于的文件夹
```shell
code /path
```
2. 在 code 终端里创建新文章
```shell
hexo new post "post_name"
```
3. 在文件夹 `./source/_posts`  中找到 `post_name.md`
4. 打开编辑
5. 保存后，`git add commit push` 三连
6. 发布成功


