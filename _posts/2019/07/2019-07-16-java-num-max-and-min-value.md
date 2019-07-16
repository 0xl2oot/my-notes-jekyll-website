---
layout: post
title:  "Java 数字类型能表示的最大最小值"
description: "Java 数字类型能表示的最大最小值"
category: "java"
tags: ["java", "max", "min", "value", "integer", "long", "float", "double"]
---

| 类型 | 最大/小值 | 二进制 | 十进制 |
| -- | -- | -- |
| Integer   | 最大值 | 0x7fffffff | 2 147 483 647 |
| Integer   | 最小值 | 0x80000000 | -2 147 483 648 |
| Long      | 最大值 | 0x7fffffffffffffffL | 9 223 372 036 854 775 807 |
| Long      | 最小值 | 0x8000000000000000L | -9 223 372 036 854 775 808 |
| Float     | 最大值 | 0x1.fffffeP+127f | 3.4028235e+38f |
| Float     | 最小值 | 0x0.000002P-126f | 1.4e-45f |
| Double    | 最大值 | 0x1.fffffffffffffP+1023 | 1.7976931348623157e+308 |
| Double    | 最小值 | 0x0.0000000000001P-1022 | 4.9e-324 |


另外 `java.math` 包中还有 `BigInteger` 和 `BigDecimal` 类型，基本上是任意精度的，极限就是你机器的上限。


```java
// 0x7fffffff = 2147483647
System.out.println(Integer.MAX_VALUE);
// 0x80000000 = -2147483648
System.out.println(Integer.MIN_VALUE);

// 0x7fffffffffffffffL = 9223372036854775807
System.out.println(Long.MAX_VALUE);
// 0x8000000000000000L = -9223372036854775808
System.out.println(Long.MIN_VALUE);

// 0x1.fffffeP+127f = 3.4028235e+38f
System.out.println(Float.MAX_VALUE);
// 0x0.000002P-126f = 1.4e-45f
System.out.println(Float.MIN_VALUE);

// 0x1.fffffffffffffP+1023 = 1.7976931348623157e+308
System.out.println(Double.MAX_VALUE);
// 0x0.0000000000001P-1022 = 4.9e-324
System.out.println(Double.MIN_VALUE);
```