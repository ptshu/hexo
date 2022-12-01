---
title: HEXO添加置顶功能
date: 2022-08-16 20:47:59
categories:
- Github使用
tags:
top:
---
目前已经有修改后支持置顶的仓库，可以直接用以下命令安装。(cmd 到博客根目录，nmp运行)
$ npm uninstall hexo-generator-index
$ npm install hexo-generator-index-pin-top
然后在需要置顶的文章的Front-matter中加上top: true即可。
<!--more-->
比如下面这篇文章：
---
title: hexo+GitHub博客搭建实战
date: 2017-09-08 12:00:25
categories: 博客搭建系列
top: true
---
到目前为止，置顶功能已经可以实现了。

