---
title: 基于 https+免费顶级域名+github+nodejs+vuepress+图床  免费搭建个人博客
date: 2020-11-22
tags:
 - 博客搭建
categories:
  - NoteBook
sticky: 1
---

## 博客笔记地址：

https://blog.hello12345.tk/



## 环境准备

>[http://www.cnodejs.org](http://www.cnodejs.org/) 官网下载 傻瓜式安装 一直确定就行 默认安装在 C:\Program Files\nodejs

<!-- more -->

## 检测安装结果

 打开 命令行 输入 node -v 会出现node版本 输入 npm -v 会出现npm版本

## 配置npm全局环境 

在C:\Program Files\nodejs 这里新建两个文件夹 “node_global”及”node_cache” 打开cmd 用管理员 身份打开 输入命令：npm config set prefix “C:\Program Files\nodejs\node_global” 输入命令 ：npm config set cache “C:\Program Files\nodejs\node_cache”

## 配置环境变量 

在系统变量下新建”NODE_PATH”，输入”C:\Program Files\nodejs\node_global\node_modules“用户变量 用户变量”PATH”修改为“C:\Program Files\nodejs\node_global\”；



## 检查 cmd命令

 输入npm install gulp -g 然后看看 node_global文件夹有没有gulp文件

## 安装cnpm

```
npm install -g cnpm –registry=https://registry.npm.taobao.org

 cnpm install -g gulp
```

## 安装yarn

```
npm install -g yarn –registry=https://registry.npm.taobao.org
```



环境已经准备好了  我们开始搭建博客

## 番茄（qiang）软件 下载 访问谷歌 youtube哟  破解5天试用了  失效重新安装

https://wwa.lanzous.com/inOLsifnr8b
密码:420o



## 博客模板

官网地址：https://vuepress-theme-reco.recoluan.com/

```
npm install @vuepress-reco/theme-cli -g -registry=https://registry.npm.taobao.org
```

![image-20201122144456170](https://gitee.com/daixiaomao/Images/raw/master/img/image-20201122144456170.png)



# 部署博客

## Git SSL公钥密钥生成

第一次配置ssh 和ssl

```
git config --global --list 
```

查看git的配置

步骤：

git config --global user.name "mukeyeshen"  

git config --global user.email "mukeyeshen@gmail.com "

ssh-keygen -t rsa -C  "mukeyeshen@gmail.com"  

1. git config --global user.name "你的用户名 "  

2. git config --global user.email "你的邮箱 "  

3. ssh-keygen -t rsa -C  "123456@qq.com "     //  生成密钥

 4.运行命令: 生成对应的key，然后系统会有英文提示你输入文件名，密码，确认密码，可以全部ente

5.结束后，对应的key就生成到.ssh目录了

*查看秘钥文件夹位置（路径地址）*

1. 输入 cd ~/.ssh 进入到.ssh 文件夹

  2.输入 ls 查看.ssh 文件夹里面有 id_rsa id_rsa.pub known_hosts 文件

 3.查看.ssh 文件   

```
cat  id_rsa.pub
```

找到.ssh目录将生成的名为 **id_rsa.pub** 的公钥复制粘贴到GitHub上增加一串密钥



## 免费域名申请视频教程

[域名申请网站](https://www.freenom.com/zh/index.html?lang=zh)   https://www.freenom.com/zh/index.html?lang=zh

身份信息  http://www.haoweichi.com/ 

[2020年 10月最新 freenom 免费顶级域名100%注册成功教程 freenom域名](https://www.youtube.com/watch?v=76QEgUGgIr8&ab_channel=E%E5%B0%8F%E7%B1%B3)

[域名注册 | Namesilo域名购买、Freenom免费域名申请及Cloudflare域名解析/免费CDN纯小白教程](https://www.youtube.com/watch?v=jfhZpN-pn6Q&ab_channel=%E7%94%AC%E5%93%A5%E6%8E%A2%E4%B8%96%E7%95%8C)





## HTTPS设置 使用cloudflare 

官网： https://www.cloudflare.com/zh-tw/



## 博客源码地址下载

https://github.com/mukeyeshen/blog_code



使用git下载

```
git clone https://github.com/mukeyeshen/blog_code.git

```

进入blog_code下安装依赖

```
cd C:\blog_code
```

```
npm install -registry=https://registry.npm.taobao.org
```

![image-20201123120042192](https://gitee.com/daixiaomao/Images/raw/master/img/image-20201123120042192.png)

本地运行 

```
npm run dev
或者
yarn dev
```

部署

```
yarn d
```

