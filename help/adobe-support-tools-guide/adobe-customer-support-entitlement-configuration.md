---
title: Adobe客户支持权利配置
description: Adobe客户如何配置支持权利以启用案例提交。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 009be3353a4bd690a7cf395e7e95540808058b39
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# Adobe客户支持权利

要为贵组织配置支持权利，请首先通过Admin Console添加或邀请用户。

## 将支持权利角色添加到组织

支持管理员角色是一个非管理角色，有权访问与支持相关的信息。 支持管理员可以查看、创建和管理问题报告。

添加或邀请管理员：

1. 在Admin Console中，选择&#x200B;**[!UICONTROL 用户]** > **[!UICONTROL 管理员]**。
1. 单击&#x200B;**[!UICONTROL 添加管理员]**。
1. 输入姓名或电子邮件地址。

   您可以搜索现有用户，或通过指定有效的电子邮件地址并在屏幕上填写信息来添加新用户。

   ![添加管理员](assets/admin-console-add-admin.png)

1. 单击&#x200B;**[!UICONTROL 下一步]**。 此时将显示管理员角色列表。

要为用户分配支持管理员角色（使用户能够联系支持人员），请执行以下操作：

1. 选择&#x200B;**[!UICONTROL 支持管理员]**&#x200B;选项。

   ![编辑管理员权限](assets/edit-admin-rights.png)

1. 选择以下两个选项之一：

   * 选项1：**[!UICONTROL 基本支持管理员]**。 如果要授予用户对所有解决方案(Marketo Engage除外)的支持访问权限，请选择此选项。
   * 选项2：**[!UICONTROL 产品支持管理员]**：为Marketo Engage支持选择此选项。 选择要授予用户支持访问权限的Marketo Engage实例。

   ![编辑管理员权限Marketo](assets/edit-admin-rights-advanced.png)

1. 作出选择后，单击&#x200B;**[!UICONTROL 保存]**。

用户将收到来自`message@adobe.com`的有关新管理权限的电子邮件邀请。

用户必须单击电子邮件中的&#x200B;**[!UICONTROL 开始]**&#x200B;才能加入组织。 如果新管理员未使用电子邮件邀请中的&#x200B;**[!UICONTROL 入门]**&#x200B;链接，他们将无法登录Admin Console。

作为登录过程的一部分，如果用户还没有Adobe配置文件，则可能会要求用户设置配置文件。 如果用户有多个与其电子邮件地址关联的配置文件，则用户必须选择&#x200B;**[!UICONTROL 加入团队]**（如果出现提示），然后选择与新组织关联的配置文件。

![管理员权限确认](assets/admin-rights-confirmation.png)

有关更多详细信息，请参阅管理角色文档中的[编辑企业管理员角色](admin-roles.md#add-enterprise-role)说明。 请注意，只有组织的系统管理员才能分配此角色。 有关管理层次结构的详细信息，请访问[管理角色](admin-roles.md)文档。
