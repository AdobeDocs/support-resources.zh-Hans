---
title: 代码块中的斜杠UGP-11189
description: 代码块中的斜杠UGP-11189测试
hide: true
hidefromtoc: true
source-git-commit: 2255dad674f1b4d456ffb50ebec9313bc4b3d7f5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 0%

---

# 代码块中的斜杠

1. 运行以下命令：

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. 运行命令（转义）：

   ```bash
   vendor/bin/magento-patches -n status |grep "27015&bsol;|Status"
   ```

不在代码块中

vendor/bin/magento-patches -n状态 |grep“27015\|Status”

转义：

vendor/bin/magento-patches -n状态 |grep &quot;27015&amp;amp；bsol；|Status&quot;

