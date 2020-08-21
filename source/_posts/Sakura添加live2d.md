---
title: Sakura添加live2d
author: 聿舟
avatar: /images/avatar.jpg
authorLink: 'https://sunzezhou.github.io'
comments: false
date: 2020-08-21 17:21:07
authorAbout:
authorDesc:
categories: Tech
tags: Blog
keywords:
description:
photos:
---

# Sakura添加live2d

继续模仿（抄）live2d的配置过程，更多参看`https://cungudafa.gitee.io/post/d214.html`

1. 打开主目录/theme/Sakura/source/ 
2. git clone https://github.com/stevenjoezhang/live2d-widget.git
3. 修改`autoload.js`, 取消`const live2d_path = "/live2d-widget/";`行的注释，并注释它的上一行`const live2d_path = "https://cdn.jsdelivr.net/gh/stevenjoezhang/live2d-widget@latest/";`
4. 在`/themes/sakura/layout/_partial/head.ejs`下添加
```
<!--自定义看板娘-->
<script src="https://cdn.jsdelivr.net/npm/jquery/dist/jquery.min.js"></script>
<script src="/live2d-widget/autoload.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/font-awesome/css/font-awesome.min.css"/>
```
5. 在主目录`_config.yam`下添加
```
live2d: ##自定义看板娘动画
  enable: true
```