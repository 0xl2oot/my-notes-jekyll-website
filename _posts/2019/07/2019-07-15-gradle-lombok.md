---
layout: post
title:  "解决Gradle+Lombok报错"
description: "解决Gradle+Lombok报错"
category: "springboot"
tags: ["springboot", "gradle", "lombok", "Gradle", "Lombok", "plugin"]
---

一般情况下，直接在dependencies里写如下配置就可以：

```
dependencies {
    compileOnly 'org.projectlombok:lombok'
    annotationProcessor 'org.projectlombok:lombok'
}

```

但是我在test中也用到了lombok，结果在运行 `./gradlew build` 的时候就报错了，说找不到 `build lombok.extern.slf4j`

解决办法比较简单，也很清晰，只需要写上testCompileOnly和testAnnotationProcessor就可以了，如下：

```
dependencies {
    compileOnly 'org.projectlombok:lombok'
    annotationProcessor 'org.projectlombok:lombok'

    testCompileOnly 'org.projectlombok:lombok'
    testAnnotationProcessor 'org.projectlombok:lombok'
}

```