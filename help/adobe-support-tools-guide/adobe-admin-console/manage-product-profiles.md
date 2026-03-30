---
title: 在Global Admin Console中管理产品配置文件
description: 了解全局管理员如何在Global Admin Console中添加、编辑和删除产品配置文件。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2:
  - id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 011223f71c06bcc17f669751ee8b12c81c52436f
workflow-type: tm+mt
source-wordcount: 580
ht-degree: 1%

---

# 在Global Admin Console中管理产品配置文件

> **应用于：**&#x200B;企业


## 概述

全局管理员可以在[Global Admin Console](https://global-admin-console.adobe.com/)中添加、编辑和删除产品配置文件。

>[!NOTE]
>
>在[Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html#request-access)中，选择一个组织并导航到&#x200B;**[!UICONTROL 产品]**。 您可以使用产品配置文件为产品激活所有或选定的服务。

与标准Admin Console中一样，产品配置文件允许您微调组织内产品的使用情况。 您还可以将管理员（称为&#x200B;**[!UICONTROL 产品配置文件管理员]**）分配给产品配置文件。 这些管理员可以将最终用户添加到他们管理的产品配置文件。

要管理产品配置文件，请选择一个产品。 将显示用于添加、编辑和删除产品配置文件的控件。

>[!NOTE]
>
>对于某些产品，您不能在Global Admin Console中创建或编辑产品配置文件。 在这种情况下，请改用[Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html)。

## 添加产品配置文件

1. 在[Global Admin Console](https://global-admin-console.adobe.com/)中，选择要编辑的组织，然后导航到&#x200B;**[!UICONTROL 产品]**&#x200B;选项卡。
1. 选择要将产品配置文件添加到的产品。
1. 选择&#x200B;**[!UICONTROL 添加配置文件]**。
1. 在&#x200B;**[!UICONTROL 添加配置文件]**&#x200B;对话框中，输入以下详细信息：

   | 字段 | 描述 |
   |---|---|
   | **[!UICONTROL 名称]** | 组织中产品配置文件的唯一名称，与其他产品配置文件和用户组不同。 |
   | **[!UICONTROL 配额]** | 为此配置文件分配的目标许可证数量。 |
   | **[!UICONTROL 用户组]** | 从下拉菜单中选择或键入用户组名称。 如果该用户组尚不存在，请首先通过[**[!UICONTROL 用户组&#x200B;]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html)选项卡创建它。 |
   | **[!UICONTROL 管理员]** | 从下拉列表中选择，或输入管理员的电子邮件地址。 如果管理员尚不存在，请首先通过[**[!UICONTROL 管理员&#x200B;]**](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)选项卡创建管理员。 |

   为指定的[!UICONTROL 用户组]分配了产品配置文件。 指定的管理员成为&#x200B;**[!UICONTROL 产品配置文件管理员]**，他们可以通过Adobe Admin Console管理相关组织的配置文件。

   ![添加配置文件](./assets/manage-product-profiles_add-profile.png)

1. 使用&#x200B;**[!UICONTROL 通知]**&#x200B;切换开关启用或禁用电子邮件通知。 启用后，当用户添加到用户档案或从用户档案中删除时，将会收到电子邮件通知。
1. 使用单个&#x200B;**[!UICONTROL 服务]**&#x200B;切换为产品配置文件启用或禁用特定服务。 有关详细信息，请参阅[为产品配置文件启用/禁用服务](https://helpx.adobe.com/enterprise/using/enable-disable-services.html)。
1. 选择&#x200B;**[!UICONTROL 保存]**。
1. 编辑完组织后，选择&#x200B;**[!UICONTROL 查看挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

## 编辑产品配置文件

1. 选择要编辑的组织，导航到&#x200B;**[!UICONTROL 产品]**&#x200B;选项卡，然后选择产品。
1. 为相关的产品配置文件选择&#x200B;**[!UICONTROL 更多选项]** ![更多选项](./assets/manage-product-profiles_more-options.png)图标，然后选择&#x200B;**[!UICONTROL 编辑配置文件]**。
1. 根据需要更新产品配置文件详细信息，然后选择&#x200B;**[!UICONTROL 保存]**。
1. 编辑完组织后，选择&#x200B;**[!UICONTROL 查看挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

## 删除产品配置文件

>[!WARNING]
>
> 删除产品配置文件会删除是该配置文件的成员，或属于附加到该配置文件的用户组的所有用户的产品访问权限。

1. 选择要编辑的组织，导航到&#x200B;**[!UICONTROL 产品]**&#x200B;选项卡，然后选择产品。
1. 为相关产品配置文件选择&#x200B;**[!UICONTROL 更多选项]** ![更多选项](./assets/manage-product-profiles_more-options.png)图标，然后选择&#x200B;**[!UICONTROL 删除配置文件]**。
1. 在确认对话框中选择&#x200B;**[!UICONTROL 确定]**。
1. 编辑完组织后，选择&#x200B;**[!UICONTROL 查看挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。


## 相关阅读

- [采用全局管理](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html)
- [管理管理员](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)
- [管理用户组](https://helpx.adobe.com/enterprise/global-admin-console/manage-user-groups.html)
- [将产品分配给子组织](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)
- [执行挂起的作业](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)
- [启用/禁用服务](https://helpx.adobe.com/enterprise/using/enable-disable-services.html)
- [Admin Console概述](https://helpx.adobe.com/enterprise/using/admin-console.html)
