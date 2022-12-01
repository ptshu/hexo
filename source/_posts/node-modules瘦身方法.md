---
title: node_modules瘦身方法
date: 2022-08-19 20:25:00
categories: 
- Github使用
tags:
top:
---
首先，说明下node_modules文件夹的作用：下载了npm或gulp的一些插件后，打开node_modules可以发现，里面有很多的文件夹，会导致我们将项目拷贝给别人的时候，传输速度会很慢。在拷贝给别人项目的时候，node_modules这个文件夹是不需要一起拷贝的，因为有package.json、package-lock.json。
<!--more-->
package.json记录当前项目所依赖模块的版本信息，更新模块时锁定模块的大版本号（版本号的第一位）。package-lock.json记录了node_modules目录下所有模块的具体来源和版本号以及其他的信息，就不做详细讲解了（相信写代码的一看就能大概明白），也可以参考：https://blog.csdn.net/qq_34295211/article/details/103858589
详细步骤如下：(初次尝试时 请先备份！请先备份！请先备份！)
npm install rimraf -g   		//安装rimraf工具
rimraf node_modules     		//使用rimraf删除node_modules文件
npm cache clean --force		//清除缓存
npm config set registry https://registry.npm.taobao.org	//设置国内镜像，防止下载缓慢卡住
npm  install			//初始化项目

每次上传项目至服务器备份时，删除node_modules文件夹，要修改项目时再重新初始化项目，安装依赖包。

另外，npm prune 命令的功能是根据package.json里的依赖项，删除不需要的模块文件。
执行npm audit fix，可以查看是否少了什么组件

