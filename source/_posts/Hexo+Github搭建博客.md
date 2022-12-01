---
title: Hexo+Github搭建博客
date: 2022-08-08 20:03:03
categories: 
- Github使用
tags: 
- Hexo
- Github
- 搭建
top: 
---
# 使用Hexo+Github搭建博客
使用 Hexo+GitHub 搭建个人免费博客教程（小白向）
https://zhuanlan.zhihu.com/p/60578464
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
** _config.yml: 博客的配置文件**
# 教程2：连接github的命令
git config --global user.name "ptshu"
git config --global user.email "zskang@qq.com"
输入 ssh-keygen -t rsa -C "zskang@qq.com"，然后一路回车。

报错信息hexo YAMLException: can not read a block mapping entry; a multiline key may not be an implicit key
报错信息是提示hexo的yml配置文件 冒号后面少了空格
解决方案：到提示行将对应的空格补上即可
https://blog.csdn.net/qq_39026548/article/details/104729964

# 教程3：添加分类及标签
Hexo使用攻略-添加分类及标签
https://www.jianshu.com/p/e17711e44e00

# 首字母大小写而 404
Hexo 改变 tag 因为大小写问题而 404 的解决方法
https://blog.zhheo.com/p/5511910d.html
hexo d 上传后about首字母变大写的原因：第一次上传时是大写，覆盖上传还就按第一次的大写写入。解决方法：把文件夹about重命名为其他（如：about2），hexo d 上传，然后再重命名回about，再hexo d 上传就完美解决了。

# 评论系统-Valine
为你的Hexo加上评论系统-Valine
https://blog.csdn.net/blue_zy/article/details/79071414

# [REMOTE REJECTED] MASTER
GIT PULL 错误：[REMOTE REJECTED] MASTER -> MASTER (PRE-RECEIVE HOOK DECLINED)
解决办法：关闭分支的保护机制
https://www.freesion.com/article/7986556587/

# 博客菜单显示中文的设置方法：
1、在博客根目录的_config.yml文件中，找到language项改为zh-CN。
2、主题目录的_config.yml文件中，找到language项改为zh-CN。
注：部分主题的_config.yml文件中没有language项的设置。