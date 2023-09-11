---
title: Github Pages配置域名失效问题
date: 2023-8-30 09:34:59
categories: 博客记录
tags: [github,域名]
---

[![pPd6VTP.md.jpg](https://s1.ax1x.com/2023/08/30/pPd6VTP.md.jpg)](https://imgse.com/i/pPd6VTP)

#### *问题描述：*

> 这两天发现部署在github的博客明明已经配置了域名，也已经显示了“DNS check successful”
>
> 但是很奇怪第二天就发现不行了，根据域名访问显示404.进到设置页面一看，域名又没了，需要重新配置。

#### *问题排查：*

- [x] 是否添加了CNAME文件并写入域名（无问题）
- [ ] CNAME文件后缀是否正确，我的CNAME文件直接在github上面进行创建的，单独下载后发现居然是TXT格式，我怀疑是这里的问题。
- [ ] 本地source目录是否也存在CNAME文件（无）
- [ ] _congfig.yml是否在URL中设置了域名。（无）

#### *具体解决办法：*

* 重新创建CNAME文件，注意是否是否仍然有后缀（CNMAE命名必须全部大写）
* 在本地博客source目录中同样将CNAME文件复制进去
* _congfig.yml中URL中设置域名，因为之前默认了example.com

#### *结果*

无问题出现，解决成功。
