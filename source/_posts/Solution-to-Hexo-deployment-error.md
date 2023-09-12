---
title: Hexo d部署报错解决办法
date: 2023-8-25 
categories: 博客记录
tags: Hexo
---

##### 方法一：***在博客文件夹中删除.deploy_git文件***

在博客文件夹中删除.deploy_git 文件
命令行(terminal)[不推荐使用cmd, 使用 git bash 等] 中输入 git config --global core.autocrlf false把git加入系统环境变量
重新执行hexo c hexo g hexo d
部署成功。

##### 方法二：***修改Repo 找到_config.yml文件***


**格式如下:**
找到_config.yml文件，翻到最后面根据格式修改如下内容
Repo:https://github.com/YourName/YourName.github.io.git(不要使用这个)
  		  git@github.com:YourName/YourName.github.io.git(用这个)
部署成功。
【注】YourName是你的GitHub用户名

[Hexo Github Action 自动部署 在线编辑文章 新建文章](https://hexo-delta-khaki.vercel.app/posts/3.html)
