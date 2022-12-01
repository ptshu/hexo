---
title: 我的HEXO博客
date: 2022-11-07 19:58:41
categories: 
- hexo
tags:
top: 2
---
#  HEXO博客信息
博客仓库名：ptshu.github.io
备份仓库名：hexo
绑定域名：www.ptsh.cf
管理地址：https://github.com/ptshu/
#  Hexo连接 Github(博客)
<!--more-->
设置用户名和邮箱：
git config --global user.name "ptshu"
git config --global user.email "zskang@qq.com"
创建 SSH 密匙：
(如果已经创建了，可以跳过直接用户旧的密匙)
ssh-keygen -t rsa -C  "zskang@qq.com"
验证连接：
ssh -T git@github.com

hexo常用命令
hexo new "name"       # 新建文章
hexo new page "name"  # 新建页面
hexo g                # 生成页面
hexo d                # 部署
hexo g -d             # 生成页面并部署
hexo s                # 本地预览
hexo clean            # 清除缓存和已生成的静态文件
hexo help             # 帮助


#  Git连接 Github(备份)
设置用户名、邮箱和仓库：
git config --global user.name "ptshu"
git config --global user.email "zskang@qq.com"
git remote set-url origin https://ghp_W42ArMmNdN9PROqD2ZAF和谐一下RaWXGwCyiY0l95jI@github.com/ptshu/hexo.git

上传命令：
git add .
git commit -m "新备份"
git push

其他常用命令：
查看当前git的配置
git config -l 
