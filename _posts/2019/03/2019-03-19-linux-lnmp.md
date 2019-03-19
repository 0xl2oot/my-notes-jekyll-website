---
layout: post
title:  "web 服务器 lnmp 的使用"
description: "web 服务器 lnmp 的使用"
category: "Linux"
tags: ["Linux"]
date: 2019-03-19 00:00:00 +0800
---

lnmp 官网 [https://lnmp.org/](https://lnmp.org/)

安装文档 [https://lnmp.org/install.html](https://lnmp.org/install.html)

很简单按照教程安装

```
wget http://soft.vpser.net/lnmp/lnmp1.5.tar.gz -cO lnmp1.5.tar.gz && tar zxf lnmp1.5.tar.gz && cd lnmp1.5 && ./install.sh lnmp
```

添加一个站点：

[https://lnmp.org/faq/lnmp-vhost-add-howto.html](https://lnmp.org/faq/lnmp-vhost-add-howto.html)


```
lnmp vhost add
```

> 注意：如果需要使用 https，则需要提前设置域名解析，最好等几分钟后在设置，这样 DNS 中才能查询得到。

FAQ [https://lnmp.org/faq.html](https://lnmp.org/faq.html)