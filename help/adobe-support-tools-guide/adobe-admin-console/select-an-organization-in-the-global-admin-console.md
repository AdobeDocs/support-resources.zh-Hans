---
title: 在Global Admin Console中选择组织
description: 了解如何选择要在Global Admin Console中编辑的组织。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 0bc0dbd8c7040e0be7e7bd45945edb0fb24cb7cc
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 1%

---


# 在Global Admin Console中选择组织

了解如何选择要在Global Admin Console中编辑的组织。

>[!NOTE]
>
>在访问[Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html#request-access)后，您可以首先选择一个组织来查看和管理组织的名称、用户组、产品配置文件、管理员和组织策略。 要登录到Global Admin Console，[单击此处](https://global-admin-console.adobe.com/)。

Global Admin Console是组织中管理Adobe资源的中心枢纽。 全局管理员可以：

- 在其组织下创建子组织
- 分配系统管理员来管理他们
- 将资源分配给子组织，以便对这些组织中的用户进行管理和分配

>[!NOTE]
>
> 组织中的用户和管理员无法查看其组织外的用户、存储或其他资源。

## 选择您的组织

**[!UICONTROL 组织选择器]**&#x200B;下拉列表中列出的组织是您明确为其全局管理员的组织，即您已被添加到具有全局管理员或全局查看器角色的组织的管理员列表中。 您隐含是层次结构中该点以下所有组织的全局管理员（或全局查看器），但这些组织未列在[!UICONTROL 组织选取器]中。

![组织选取器](/help/adobe-support-tools-guide/assets/org-picker.png)

如果您希望将他们列出，请将自己作为全局管理员添加到要列出的组织。 当您在[!UICONTROL 组织选择器]中选择组织时，您的管理权限基于您是所选组织的全局管理员。 此外，您还可能在树中作为父组织的全局管理员列出，这样可为您提供更多权限。 您必须选择该更高级别的组织才能获得其他权限。

在Global Admin Console中，从[!UICONTROL 层次结构树]中选择组织后，即可开始编辑特定组织的信息。

**编辑可能影响：**

- 组织名称
- 用户组
- 产品配置文件
- 管理员
- 组织策略

**编辑无法影响：**

- 用户（删除组或产品配置文件除外）
- 添加用户（管理员除外）

从层次结构树中选择组织时，将显示以下信息：

- 组织名称
- 区域
- 用户数量
- 产品列表
- 产品配置文件
- 用户组
- 管理员
- 声明的域
- 组织的策略值

要查看或编辑产品、用户组、管理员、域、策略或策略模板，请选择相应的选项卡。 在大多数情况下，您可以使用[!UICONTROL 搜索]字段在选项卡中查找特定项目。

![编辑组织](/help/adobe-support-tools-guide/assets/edit-an-organization.png)

添加到组织或从组织中删除的任何管理员都将收到电子邮件通知。 对组织所做的某些策略更改会在该组织的[!DNL Admin Console]中生成通知。

## 了解限制和必要条件

- 嵌套组织的最大深度为5。 因此，允许a/b/c/d/e ，但a/b/c/d/e/f为错误。 例如，允许Acme Corp/国际区域/ Acme Europe/ Acme UK/ Acme London ，但Acme Corp/国际区域/ Acme Europe/ Acme UK/ Acme London/ Acme Mayfair是一个错误。

- 路径名的最大长度（包括所有组织）为255个字符（包括“/”）。 单个组织名称的最大长度为4至100个字符。

- 组织路径名是唯一的，但简单名称在其同级中是唯一的。 在组织层次结构中的其他位置，可能会有具有相同简单名称的组织。

- 您只能使用Global Admin Console查看链接到所选组织的域列表。 如果您是所选组织的系统管理员，请选择&#x200B;**[!UICONTROL 在Admin Console中打开]**&#x200B;以[管理域](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html)。 若要了解“域”选项卡中显示的信息，请参阅[导出和导入架构](https://helpx.adobe.com/enterprise/global-admin-console/export-and-import-data.html#export-and-import-schemas)。

- 全局管理访问不支持IE 11。 使用其他浏览器或更新版本的IE浏览器。
