---
title: 安装Vue.js
date: 2025-04-26 16:42:38
tags: 
categories: [学习]
---
## 一、安装过程
### 1.安装node.js
Vue CLI 4.x 需要Node.js 8.9 或更高版本（推荐v10+）。可以使用n、nvm或nvm-windows 在同一台机器上管理多个版本的Node。 如果你不确定系统中正在运行的 Node.js 版本是什么，请在终端窗口中运行 如下命令
：

```     bash
node -v
```
### 2.安装npm
可以通过这个命令检查是否安装了npm客户端
``` bash
npm -v
```
### 3.安装Vue CLI新软件包
``` bash
npm install -g @vue/cli
```
你可以通过以下命令检查是否安装成功
``` bash
vue --version
```
如果你和我一样不小心安装了之前版本，可以用这个命令卸载
``` bash
npm uninstall vue-cli -g
```
## 二、问题总结
其实在安装了新版本之后，我的vue依旧是安装失败的。此时有可能是npm全局路径没有添加到系统变量，所以我先通过以下命令找到npm全局安装路径
。
``` bash
npm config get prefix
```
之后我把该路径添加到了系统的PATH变量上，问题就解决了。

