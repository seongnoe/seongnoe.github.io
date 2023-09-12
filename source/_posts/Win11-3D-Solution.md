---
title: Win11投影误触3D模式导致黑屏无法连接解决办法
date: 2023-8-28 13:21:54
categories: 博客记录
tags: Win11
---

#### 问题描述：
今天在公司帮业务部同事用公司笔记本连接投屏，因连接之后桌面图标不显示，遂进入系统屏幕设置中，结果误触了3D模式，突然屏幕跳动，然后投影仪检测不到信号。<!--more-->

***是否解决：已经解决***

* 系统：Win11
* 查询网站：CSDN 、知乎[^1] 、哔哩哔哩

==============================================================================

#### 解决办法1
 1.把下面注册表路径内的子项删掉就行【不要删除主文件夹 需要一个一个删除】

`HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\GraphicsDrivers\Configuration
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\GraphicsDrivers\Connectivity
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\GraphicsDrivers\ScaleFactors`

==============================================================================

#### 解决办法2

**通过directx 修复工具解决**

下载链接：
[DirectX修复工具  v4.2.0.40217 中文版下载](https://www.onlinedown.net/soft/120082.htm?t=1536963605416)


* 下载完成后将DirectX Repair解压出来，打开文件夹，双击 DirectX_Repair ；

* DirectX修复工具 ，然后在工具栏中点击【工具】--【选项】按钮；

* 在选项界面点击【DirectX 加速】

* 在下面找到 DirectDraw 加速、Direct3D加速 ，点击后面的【禁用】即可！

【备注】第五步我只点了禁用directdraw加速，direct3d不能点，显示部分禁用，然而同样有效，重启后一切恢复正常了。

#### 总结

方法应该有很多，目前只测试了这两种方法，方法二是有效果的。第一种方法操作重启后，仍然看不到3D模式恢复。

#### 参考链接
* [^1]:[知乎问题：win10的3D显示模式怎么关闭?](https://www.zhihu.com/question/454082578)
