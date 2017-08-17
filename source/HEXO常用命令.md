title: HEXO常用命令
date: 2016-10-06 00:51:07
tags: ['hexo','工具']
---


自己挖的坑，一直没有填上。我要求自己每周至少写一篇日志的，结果掉了36篇没有补上。2016年都10月份了，赶紧的把坑填上。今天更2篇。同时将一些自己常忘记的写blog命令写上一篇。


一些常用命令：

hexo new"postName" #新建文章

hexo new page"pageName" #新建页面

hexo generate #生成静态页面至public目录

hexo server #开启预览访问端口（默认端口4000，'ctrl + c'关闭server）

hexo deploy #将.deploy目录部署到GitHub


部署步骤

每次部署的步骤，可按以下三步来进行。

    hexo clean

    hexo generate

    hexo deploy
