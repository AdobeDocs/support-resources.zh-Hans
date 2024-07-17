---
title: 换表符
description: 测试不同的表分隔符
hide: true
hidefromtoc: true
exl-id: a769fcb7-f8d3-419b-bdd4-98b71bdf3b5d
source-git-commit: 972704990172c966a27744b49b9f7af5626e9f3e
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 25%

---

# 换表符

这里没什么可看的。

## 带有`<br>`的标准Markdown表

**已修复`Green<br>Red<br>Blue`**

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

## 带双精度型`<br>`的Markdown表

**已修复`Green<br><br>Red<br><br>Blue`**

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

## 带有`<p>`的Markdown表

**已修复`Green<p>Red<p>Blue`**

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
| Juanya | 17 | 这是颜色&#x200B;**绿色**，它用于作为事项换行，并且是测试上述段落分隔的手段。 <p>这是颜色&#x200B;**红色**，它用于作为事项换行，并且是测试上述段落分隔的手段。 <p>这是颜色&#x200B;**蓝色**，它用于作为事项换行，并且是测试上述段落分隔的手段。 |
| Maria | 23 | 黄色<p>棕色 |

{style="table-layout:fixed"}

|  | 数值 | 颜色 |
|---|---|---|
| Juanya | 17 | 这是颜色&#x200B;**绿色**，它用于作为事项换行，并且是测试上述段落分隔的手段。 <p>这是颜色&#x200B;**红色**，它用于作为事项换行，并且是测试上述段落分隔的手段。 <p>这是颜色&#x200B;**蓝色**，它用于作为事项换行，并且是测试上述段落分隔的手段。 |
| Maria | 23 | 黄色<p>棕色 |

{style="table-layout:auto"}
