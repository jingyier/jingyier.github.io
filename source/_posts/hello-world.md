---
title: Hello World
---
这篇博客简述一下整个博客框架的搭建流程，该文本不包括站点信息的配置。流程如下：

## 安装Node.js

首先我们应该安装Node.js,下载地址如下：[nodejs](https://nodejs.org/zh-cn/download/)；
安装完成之后我们要确保环境变量配置好，可以正常使用npm命令。

## 安装Hexo

Hexo是一个博客框架，其官方还提供了一个命令行工具，可以快速创建项目、页面、编译、部署Hexo博客，接下来我们应该安装Hexo的命令行工具。

### 安装命令如下

``` bash
$ npm install -g hexo-cli
```
安装完成后，确保环境变量配置好，可以正常使用hexo命令。

## 用hexo命令行创建项目

### 创建新项目

``` bash
$ hexo new "My New Post"
```
接下来我们进入新生成的文件夹里，调用hexo的generate命令，这样就将Hexo编译生成HTML代码，命令如下：

``` bash
$ hexo generate
```
然后我们可以通过hexo提供的serve命令使博客在本地运行起来，命令如下：


``` bash
$ hexo serve
```
### 部署
那么怎么把这个页面部署到Github Pages上面呢？hexo已经提供了一个命令可以帮助我们将博客一键部署，但是在运用这个命令之前，我们应该安装hexo-deployer-git插件,执行的安装命令如下：
``` bash
$ npm install hexo-deployer-git --save 
```
安装成功后，执行部署命令；

### 执行部署命令

``` bash
$ hexo deploy
```

这样一来我们的博客就成功部署到 Github Pages 上面了，此时我们已经可以通过访问 Github Repository 的同名链接，就能看到和本地相同的博客内容了。

## 总结

总而言之一个博客的构建并不困难，过程并非复杂繁琐，但我们仍然需要有足够的耐心去解决一个个奇奇怪怪的小问题，坚持下去就好！
