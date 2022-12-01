---
title: Github与Gitee的hexo连接
date: 2022-08-19 21:39:46
categories:
- Github使用
tags:
top:
---
#  连接 Github
右键 -> Git Bash Here，设置用户名和邮箱：
git config --global user.name "GitHub 用户名"
git config --global user.email "GitHub 邮箱"
查看git的配置列表：(需要时可以查看)
git config --list
创建 SSH 密匙：(如果已经创建了，可以跳过直接用户旧的密匙)
输入 ssh-keygen -t rsa -C "GitHub 邮箱"，然后一路回车。
<!--more-->
添加密匙：

进入 [C:\Users\用户名\.ssh] 目录（要勾选显示“隐藏的项目”），用记事本打开公钥 id_rsa.pub 文件并复制里面的内容。

登陆 GitHub ，进入 Settings 页面，选择左边栏的 SSH and GPG keys，点击 New SSH key。

Title 随便取个名字，粘贴复制的 id_rsa.pub 内容到 Key 中，点击 Add SSH key 完成添加。

验证连接：

打开 Git Bash，输入 ssh -T git@github.com 出现 “Are you sure……”，输入 yes 回车确认。

显示 “Hi xxx! You've successfully……” 即连接成功。

#  连接 Gitee

修改根目录_config.yml配置
deploy:
type: git
repo: https://gitee.com/ptshucn/ptshucn.git （将地址换成自己的地址）
branch: master

然后在blog的根目录执行命令：

npm install hexo-deployer-git --save # 安装git插件

git config --global user.email zskang@qq.com # 设置gitee邮箱（gitee的注册邮箱）

git config --global user.name ‘ptshucn’ # 设置用户名（git的注册昵称）

hexo deploy # 上传到gitee

然后选择gitee pages服务，然后选择开启 或 更新即可。

