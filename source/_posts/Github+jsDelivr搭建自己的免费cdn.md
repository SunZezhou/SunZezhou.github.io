---
title: Github+jsDelivr搭建自己的免费cdn
author: 聿舟
avatar: /images/avatar.jpg
authorLink: 'https://sunzezhou.github.io'
comments: false
date: 2020-08-21 16:54:16
authorAbout:
authorDesc:
categories: Tech
tags: Blog
keywords:
description:
photos: /images/cdn.jpg
---

## Github+jsDelivr搭建自己的免费cdn

由于我才搭好个人博客，就看到了 https://cungudafa.gitee.io/post/2a9.html 这篇文章教搭cdn， 我就照🐯画🐱照着操作一遍，并留个备忘。

## 上传

1. 新建Github repo, 名字最好叫cdn
2. 将自己的img和js素材放进去（据说支持20M以内的图片、视频、js、css等）
3. push以后点击releases， 按要求发布

## 下载

使用jsDelivr引用

- 模版
`https://cdn.jsdelivr.net/gh/你的用户名/你的仓库名@发布的版本号/文件路径`

eg: `https://cdn.jsdelivr.net/gh/SunZezhou/cdn/images/wallpaper.jpg`

- 其中版本号不是必需的，是为了区分新旧资源，如果不使用版本号，将会直接引用最新资源
- 据说可以加载任何Github发布、提交或分支
- 据说可以使用某个范围内的版本，查看所有资源
- 将“.min”添加到任何JS/CSS文件中以获取缩小版本，如果不存在，将为会自动生成 `https://cdn.jsdelivr.net/gh/user/repo@version/file/file.min.js`
- 不写最后的文件名，可以获得文件列表`https://cdn.jsdelivr.net/gh/user/repo@version/file/`