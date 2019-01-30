---
layout: post
title:  "vuetifyjs 样式在生产环境失效"
description: "vuetify 按钮有一些属性，比如 info, warning, error 和 success 等，这些在 dev 模式下是正常显示的，到了生产环境却不显示了，这是什么原因呢？"
category: "vuetify"
tags: ["vuetify"]
date:   2019-01-16 12:00:00 +0800
---

vuetify 按钮有一些属性，[比如 info, warning, error 和 success 等](https://vuetifyjs.com/zh-Hans/components/buttons)，这些在 dev 模式下是正常显示的，如下图，到了生产环境却不显示了，这是什么原因呢？

- npm run dev 正常
- npm run generate 放到 Nginx 中不正常

<div align="center"><img src="/assets/Screen Shot 2019-01-19 at 12.19.20 AM.png" width="800px" /> </div><br>


我查了好久，终于在 Stack Overflow 上找到了答案

[https://stackoverflow.com/questions/50003226/vuetify-colors-are-not-showing-up](https://stackoverflow.com/questions/50003226/vuetify-colors-are-not-showing-up)

很简单，就是需要让这些内容被 v-app 标签给包起来

```vue
<v-app>
  <v-btn color="success">Success</v-btn>
  <v-btn color="error">Error</v-btn>
  <v-btn color="warning">Warning</v-btn>
  <v-btn color="info">Info</v-btn>
</v-app>
```