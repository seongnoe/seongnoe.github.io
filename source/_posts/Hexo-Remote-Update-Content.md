---
title: Hexo+Git远程更新内容
date: 2023-8-25 09:04:01
categories: 博客记录
tags:
---

更新与发布博文 依然在 Git Shell 中进入 Hexo文件夹，执行下面几条命令，将博客部署到 GitHub 上：

<!--more-->

```c#
hexo clean (也可以hexo cl)
hexo generate (若要本地预览就先执行 hexo server) 
hexo deploy
```



快捷命令：

~~~javascript
```hexo c == hexo clean \# 清除缓存 
hexo g == hexo generate \# 生成静态文件
hexo d == hexo deploy \# 部署到github中，更新网页端的内容 
hexo s == hexo server \# 通过启动本地服务器，预览文章效果 
hexo n == hexo new ```
~~~



还能组合使用，如：

```hexo d -g ```刷新个人博客，一般使用如下命令来刷新博客。

`hexo clean && hexo g && hexo d`

