---
title: 使用Hexo+GitHub搭建博客
date: 2022-12-02 19:58:41
categories: 
- hexo
tags:
top: 2
---
#  HEXO博客信息
博客仓库名：ptshu.github.io
备份仓库名：hexo
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
第一次关联仓库
git remote add origin https://ghp_YtdiutIzUSJw1aBftZmD和谐一下TGBQROg3Rh3pLH24@github.com/ptshu/hexo.git
或修改关联仓库
git remote set-url origin https://ghp_YtdiutIzUSJw1aBftZmD和谐一下TGBQROg3Rh3pLH24@github.com/ptshu/hexo.git

上传命令：
git add .
git commit -m "新备份"
git pull --rebase origin master    //本地与远程版本不一致（如远程上删减或修改文件），需要先用此命令合并
git push origin master

#  其他常用命令：
查看当前git的配置
git config -l 

#  github用户申请专属token(个人令牌)
Settings => Developer Settings => Personal access tokens
如：
git-to-hexo@token
ghp_YtdiutIzUSJw1aBftZmD和谐一下TGBQROg3Rh3pLH24
picx@token
ghp_ObXvJO6jrjhHcMhI和谐一下Ug8UeT9y210ZJN3O2sPM


#  Github添加密匙：

进入 [C:\Users\用户名\.ssh] 目录（要勾选显示“隐藏的项目”），用记事本打开公钥 id_rsa.pub 文件并复制里面的内容。

登陆 GitHub ，进入 Settings 页面，选择左边栏的 SSH and GPG keys，点击 New SSH key。

Title 随便取个名字，粘贴复制的 id_rsa.pub 内容到 Key 中，点击 Add SSH key 完成添加。

验证连接：

打开 Git Bash，输入 ssh -T git@github.com 出现 “Are you sure……”，输入 yes 回车确认。

显示 “Hi xxx! You've successfully……” 即连接成功。
