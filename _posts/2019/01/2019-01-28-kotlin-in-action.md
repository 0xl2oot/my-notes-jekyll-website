---
layout: post
title:  "Kotlin 学习笔记"
description: "一步一步学习 Kotlin"
category: "kotlin"
tags: ["kotlin"]
date:   2019-01-28 10:00:00 +0800
---

### 0.Kotlin Hello World

```kotlin
fun main(args: Array<String>) {
    println("hello kotlin")
}
```

### 1.从 Java 过度到 Kotlin

从 Java 迁移到 Kotlin，下面是一段 Java 代码，转换成 Kotlin 的示例。如果是在 IntelliJ IDEA 中我们是不需要手动写的，直接从 Java 文件中复制，到 Kotlin 文件中粘贴就可以了，她会提示你自动去转换


```java
// java
import java.util.Collection;
import java.util.Iterator;

public class JavaCode {
    public String toJSON(Collection<Integer> collection) {
        StringBuilder sb = new StringBuilder();
        sb.append("[");
        Iterator<Integer> iterator = collection.iterator();
        while (iterator.hasNext()) {
            Integer element = iterator.next();
            sb.append(element);
            if (iterator.hasNext()) {
                sb.append(", ");
            }
        }
        sb.append("]");
        return sb.toString();
    }
}
```

```kotlin
// kotlin
fun toJSON(collection: Collection<Int>): String {
    val sb = StringBuilder()
    sb.append("[")
    val iterator = collection.iterator()
    while (iterator.hasNext()) {
        val element = iterator.next()
        sb.append(element)
        if (iterator.hasNext()) {
            sb.append(", ")
        }
    }
    sb.append("]")
    return sb.toString()
}
```

未完待续……