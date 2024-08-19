---
title: 代码块中的斜杠UGP-11189
description: 代码块中的斜杠UGP-11189测试
hide: true
hidefromtoc: true
source-git-commit: 4fc9b739d18941d276b88f8799163523c8bd5f85
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 4%

---

# 代码块中的斜杠

1. 运行以下命令：

   ```bash
   vendor/bin/magento-patches -n status |grep "27015\|Status"
   ```

1. 下一步

不在代码块中

vendor/bin/magento-patches -n状态 |grep“27015\|Status”

转义的反斜线：

vendor/bin/magento-patches -n状态 |grep &quot;27015&amp;amp；bsol；|Status&quot;
