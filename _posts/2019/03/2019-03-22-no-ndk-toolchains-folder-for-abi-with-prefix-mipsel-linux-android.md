---
layout: post
title:  "ERROR: No toolchains found in the NDK toolchains folder for ABI with prefix: mipsel-linux-android"
description: "ERROR: No toolchains found in the NDK toolchains folder for ABI with prefix: mipsel-linux-android"
category: "android"
tags: ["android"]
date: 2019-03-22 00:00:00 +0800
---

在 GitHub 上看到一个安卓的项目 [https://github.com/chentao0707/SimplifyReader](https://github.com/chentao0707/SimplifyReader)

运行的时候报了个错 

```
ERROR: No toolchains found in the NDK toolchains folder for ABI with prefix: mipsel-linux-android
```

查了一下，是 NDK 更新了的原因，在 NDK r18 以后，mipsel-linux-android 被移除了，所以找不到这个包。

看一下 Android Studio 中 Project Structure，找到 NDK 路径，打开文件夹查看，发现确实没有这个文件夹

<div align="center"><img src="/assets/Screen Shot 2019-03-22 at 2.55.02 PM.png" width="600px" /> </div><br>

去 [https://developer.android.com/ndk/downloads/](https://developer.android.com/ndk/downloads/) 下载老版本的 NDK，将老版本的 NDK toolchains 文件夹中 mipsel-linux-android 复制到你的 NDK 目录中。


<div align="center"><img src="/assets/Screen Shot 2019-03-22 at 2.58.21 PM.png" width="800px" /> </div><br>
