---
layout: post
title:  "Vue.js 初学者可能会遇到的问题"
date:   2018-10-25 19:13:58 +0800
---

### npm 和 Yarn

Yarn [https://yarnpkg.com/zh-Hans/](https://yarnpkg.com/zh-Hans/)

npm [https://www.npmjs.com/](https://www.npmjs.com/)


npm 和 Yarn 都是 JavaScript 的管理工具，但是 Yarn 会比 npm 快的多，Yarn 会缓存它下载的每个包，所以无需重复下载。它还能并行化操作以最大化资源利用率，安装速度之快前所未有。

### npm 和 cnpm 

npm 的仓库在国外，国内用户访问会慢很多，甚至有时候影响了项目的构建。

因此出现了 cnpm 淘宝的 npm 镜像 [https://npm.taobao.org/](https://npm.taobao.org/)

可以使用淘宝定制的 cnpm (gzip 压缩支持) 命令行工具代替默认的 npm:


```shell
$ npm install -g cnpm --registry=https://registry.npm.taobao.org
```

安装完之后就可以使用 cnpm 命令了，详细的使用方法还是看官方的说明吧 [https://npm.taobao.org/](https://npm.taobao.org/)


### eslint - JavaScript 代码规范

刚开始 init Vue.js 的项目时，有关于 JavaScript 语法检查的 eslint 的选项，如果我们开了之后，会发现运行的时候可能有很多错误，但是不知道错在哪里，其实有可能不是错误，只是不符合规范。

我们可以从下面两个链接中学习一下关于 JavaScript 的规范，这个规范只是大家约定俗成的的一套规范，能够让我们开发出更加优秀的代码。虽然看着比较艰难，有些规范也有很多人争论，但这并不是我们的重点，我们的重点在如何高效率的开发出程序来。


[https://github.com/standard/standard/blob/master/docs/README-zhcn.md](https://github.com/standard/standard/blob/master/docs/README-zhcn.md)

[https://github.com/standard/standard/blob/master/docs/RULES-zhcn.md](https://github.com/standard/standard/blob/master/docs/RULES-zhcn.md)

### Yarn CLI 介绍

[https://yarnpkg.com/zh-Hans/docs/cli/](https://yarnpkg.com/zh-Hans/docs/cli/)

### Vuetify - Material Design Component Framework

https://vuetifyjs.com/

### vue-2-boilerplate - 一个 Vue.js 的脚手架

Vue 2 boilerplate for developing medium to large single page applications.

[https://github.com/petervmeijgaard/vue-2-boilerplate](https://github.com/petervmeijgaard/vue-2-boilerplate)

### 参考文献

- [知乎 - npm和yarn的区别，我们该如何选择？](https://zhuanlan.zhihu.com/p/27449990)

