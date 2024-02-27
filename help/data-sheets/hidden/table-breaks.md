---
title: 换表符
description: 测试不同的表分隔符
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 28%

---

# 换表符

## 带有以下内容的标准Markdown表 `<br>`

**固定`Green<br>Red<br>Blue`**

|  | 数值 | 颜色 |
|---|---|---|
| Juanya | 17 | 绿<br>红<br>蓝 |
| Maria | 23 | 黄<br>棕 |

{style="table-layout:fixed"}

**自动`Green<br>Red<br>Blue`**

|  | 数值 | 颜色 |
|---|---|---|
| Juanya | 17 | 绿<br>红<br>蓝 |
| Maria | 23 | 黄<br>棕 |

{style="table-layout:auto"}

## 带双精度的Markdown表 `<br>`s

**固定`Green<br><br>Red<br><br>Blue`**

|  | 数值 | 颜色 |
|---|---|---|
| Juanya | 17 | 绿<br><br>红<br><br>蓝 |
| Maria | 23 | 黄<br><br>棕 |

{style="table-layout:fixed"}

**自动`Green<br><br>Red<br><br>Blue`**

|  | 数值 | 颜色 |
|---|---|---|
| Juanya | 17 | 绿<br><br>红<br><br>蓝 |
| Maria | 23 | 黄<br><br>棕 |

{style="table-layout:auto"}

## Markdown表格与 `<p>`

**固定`Green<p>Red<p>Blue`**

|  | 数值 | 颜色 |
|---|---|---|
| Juanya | 17 | 绿色<p>红色<p>蓝色 |
| Maria | 23 | 黄色<p>棕色 |

{style="table-layout:fixed"}

**自动`Green<p>Red<p>Blue`**

|  | 数值 | 颜色 |
|---|---|---|
| Juanya | 17 | 绿色<p>红色<p>蓝色 |
| Maria | 23 | 黄色<p>棕色 |

{style="table-layout:auto"}

|  | 数值 | 颜色 |
|---|---|---|
| Juanya | 17 | 这是颜色 **绿色** 并且它旨在作为事件和测试上述段落分隔符的方法换行。 <p>这是颜色 **红色** 并且它旨在作为事件和测试上述段落分隔符的方法换行。 <p>这是颜色 **蓝色** 并且它旨在作为事件和测试上述段落分隔符的方法换行。 |
| Maria | 23 | 黄色<p>棕色 |

{style="table-layout:fixed"}

|  | 数值 | 颜色 |
|---|---|---|
| Juanya | 17 | 这是颜色 **绿色** 并且它旨在作为事件和测试上述段落分隔符的方法换行。 <p>这是颜色 **红色** 并且它旨在作为事件和测试上述段落分隔符的方法换行。 <p>这是颜色 **蓝色** 并且它旨在作为事件和测试上述段落分隔符的方法换行。 |
| Maria | 23 | 黄色<p>棕色 |

{style="table-layout:auto"}
