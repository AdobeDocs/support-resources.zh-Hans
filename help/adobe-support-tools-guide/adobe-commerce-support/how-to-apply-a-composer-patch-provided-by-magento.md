---
title: 如何应用Adobe提供的编辑器修补程序
description: 本文指示如何对Adobe Commerce内部部署、Adobe Commerce on cloud infrastructure和Magento Open Source应用编辑器修补程序。
feature: Best Practices, Compliance, Console
solution: Commerce
feature-set: Commerce
exl-id: 66d8df60-4c4a-49ef-8107-986e10d6e289
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
    internal-label: Compliance
  - id: 125c1f49-aefd-5f34-a252-288937f95f6b
    internal-label: Marketing Tools
subfeature_v2:
  - id: c4af0798-d497-5e6b-8380-19812c26d00a
    internal-label: Console
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%
---
# 如何应用Adobe提供的编辑器修补程序

本文指示如何对Adobe Commerce内部部署、Adobe Commerce on cloud infrastructure和Magento Open Source应用编辑器修补程序。

>[!WARNING]
>
>我们强烈建议先在暂存/集成环境中应用和测试修补程序，然后再将其应用于生产。 我们建议您在进行任何操作之前先进行备份。

## 如何在云基础架构上为Adobe Commerce应用编辑器修补程序 {#cloud}

1. 如果项目根目录中没有名为`m2-hotfixes`的目录，请创建一个。
1. 将`%patch_name%.composer.patch`文件复制到`m2-hotfixes`目录。
1. 添加、提交和推送代码更改：

   ```git
   git add -A
   ```

   ```git
   git commit -m "Apply %patch_name%.composer.patch patch"
   ```

   ```git
   git push origin
   ```

有关将修补程序应用到云项目的其他信息，请参阅我们的开发人员文档中的[应用修补程序](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/develop/upgrade/apply-patches)。

## 如何为Adobe Commerce内部部署和Magento Open Source应用编辑器修补程序 {#commerce}

1. 将修补程序上传到Adobe Commerce内部部署或Magento Open Source根目录。
1. 运行以下SSH命令：

   ```bash
   patch -p1 < %patch_name%.composer.patch
   ```

   （如果上述命令不起作用，请尝试使用`-p2`而不是`-p1` ）

1. 要使更改生效，请在&#x200B;**[!UICONTROL 系统]** > **[!UICONTROL 缓存管理]**&#x200B;下的管理员中刷新缓存。
