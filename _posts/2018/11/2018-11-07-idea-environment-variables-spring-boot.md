---
layout: post
title:  "IntelliJ IDEA SpringBoot 项目读取系统环境变量"
description: "现在很多项目为了在本地和线上部署方便，都采用了从系统环境变量读取 MySQL 等配置信息的，然而，在 macOS 中，却怎么也读不到系统环境变量，怎么办呢？"
category: "macOS"
tags: ["macOS"]
date:   2018-11-07 13:00:00 +0800
---

### 情景再现

现在很多项目为了在本地和线上部署方便，都采用了从系统环境变量读取 MySQL 等配置信息的

就像这样👇

```
spring.datasource.driver-class-name=com.mysql.jdbc.Driver
spring.datasource.url=jdbc:mysql://${MYSQL_HOST}:${MYSQL_PORT}/test?useSSL=false&characterEncoding=utf8&autoReconnect=true
spring.datasource.username=${MYSQL_USER}
spring.datasource.password=${MYSQL_PASSWORD}
```

设置了环境变量，在命令行中也能 echo

但是就是 IntelliJ IDEA 读不到

### 解决办法

方法1：通过bash命令 open /Applications/xxx.app启动 IDEA。

方法2：不在环境变量中设置，在 IDEA 中设置 Application 的启动环境

在运行的按钮处，选择 Edit Configurations

![](/assets/Screen Shot 2018-11-08 at 3.36.13 PM.png)

接下来我们展开 Environment 选项，发现有个 Environment variables.我们点开进行修改

![](/assets/Screen Shot 2018-11-08 at 3.38.21 PM.png)

改成下面的样子就可以了

![](/assets/Screen Shot 2018-11-08 at 3.39.52 PM.png)

运行 -> 成功 ！！！ 

### 参考

-[mac上ide中无法获取环境变量的问题](https://blog.csdn.net/kobe1110/article/details/50524220)
-[IntelliJ Idea中设置和使用环境变量？](https://cloud.tencent.com/developer/ask/32339)