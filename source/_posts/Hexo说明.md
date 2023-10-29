---
title: Hexo说明
date: 2022-08-08 20:03:03
categories: 
- Hexo
tags: 
- Hexo
- Github
- 搭建
top: 
---
# hexo常用命令
hexo new "name"       # 新建文章
hexo new page "name"  # 新建页面
hexo g                # 生成页面
hexo d                # 部署
hexo g -d             # 生成页面并部署
hexo s                # 本地预览
hexo clean            # 清除缓存和已生成的静态文件
hexo help             # 帮助
<!--more-->
# 文件夹目录说明：
node_modules: 依赖包
public：存放生成的页面
scaffolds：生成文章的一些模板
source：用来存放你的文章
themes：主题
文件_config.yml: 博客的配置文件
# 博客菜单显示中文的设置方法：
1、在博客根目录的_config.yml文件中，找到language项改为zh-CN。
2、主题目录的_config.yml文件中，找到language项改为zh-CN。
注：部分主题的_config.yml文件中没有language项的设置。