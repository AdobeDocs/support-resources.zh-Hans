---
title: 下载审核日志和导出报告
description: 了解全局管理员如何在Global Admin Console中查看、筛选和导出审核日志和报告。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 4b562a4d-14e5-4687-a1ae-6a435f087627
source-git-commit: 5573d0f0e58b7ba799726740ae0d29b1053122aa
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 3%

---

# 下载审核日志和导出报告

适用于企业。

了解全局管理员如何使用Global Admin Console查看、筛选和导出审核日志和报告。

若要开始，请登录到[Global Admin Console](https://global-admin-console.adobe.com/)。 然后转到&#x200B;**[!UICONTROL 分析]**&#x200B;选项卡并选择&#x200B;**[!UICONTROL 审核日志]**&#x200B;以跟踪跨组织所做的所有更改。

## 查看和下载审核日志

作为全局管理员，您可以完全了解在Global Admin Console中所做的更改。 您可以搜索所有组织中的审核日志，以查看过去90天内采取的操作，包括操作发生的时间以及操作的执行者。
- 审核日志通过防止不适当的系统访问以及审核组织内的可疑行为，帮助确保持续合规。
- Global Admin Console中可用的日志仅包括全局管理员有权访问的事件。 它们不包括用户分配或用户事件。 [了解更多](https://helpx.adobe.com/cn/enterprise/using/admin-console.html)有关每个控制台提供的不同功能。
- 日志涵盖层次结构中所有组织的事件，允许您一次搜索所有组织的审核日志。

>[!NOTE]
>
> 作为[Adobe Admin Console](https://adminconsole.adobe.com)组织中的系统管理员，您可以使用[审核日志](https://helpx.adobe.com/cn/enterprise/using/audit-logs.html)来查看用户分配和用户事件。 审计日志中还包括所选组织的子组织中系统管理员执行的操作。 详细了解系统管理员如何[跟踪在Admin Console中所做的更改](https://helpx.adobe.com/cn/enterprise/using/audit-logs.html)。

要查看或下载组织的审核日志，请执行以下操作：

1. 以全局管理员身份登录到[Global Admin Console](https://global-admin-console.adobe.com/insights)。
1. 选择&#x200B;**[!UICONTROL 分析]** > **[!UICONTROL 审核日志]**。

审核日志会显示已过滤事件的以下信息：

| 字段 | 描述 |
|------ |-------------|
| 日期 | 事件的日期和时间，以本地时区显示。 |
| 活动名称 | 所执行操作的描述。 |
| 事件详细信息 | 其他事件详细信息（如果可用）。 |
| 对象名称 | 事件中涉及的产品、产品配置文件或用户组的名称（如果适用）。 |
| 受影响的用户 | 受影响用户的电子邮件地址（如果适用）。 |
| 管理员 | 执行操作的管理员的电子邮件地址。 如果操作是由Adobe后端系统执行的，则显示&#x200B;*系统*。 |
| IP地址 | 执行操作的计算机的IP地址。 这通常反映了物理位置，但可以是代理服务器或VPN地址。 |
| 组织 | 受事件影响的组织的名称。 |

1. 您可以使用以下选项筛选审核日志：

   - 按受影响的用户或管理员进行搜索。
   - 选择一个或多个组织。
   - 定义日期范围。
   - 按事件名称筛选。
   - 合并过滤器以缩小结果范围，例如查看特定组织过去七天的事件。

   ![审核日志](assets/audit-logs.png)

   *根据事件名称、受影响的组织或日期范围筛选审核日志。*

   ![选择组织](assets/select-organizations.png)

   *选择要筛选审核日志的组织。*

1. 要导出审核日志，请选择&#x200B;**[!UICONTROL 导出CSV]**&#x200B;以导出筛选的结果。 结果将以CSV格式下载。

有关导出中包含的字段的详细信息，请参阅[日志架构](#log-schema)。

>[!NOTE]
>
>导出的审核日志报告在生成后将保留90天。


## 了解您的审核日志报告 {#log-schema}

导出的审核日志报告包含每个组织的以下字段：

| 字段 | 描述 |
|------|------------|
| ID | 事件 ID |
| eventTime | 事件的日期和时间（本地时区） |
| 事件类型 | 事件的名称 |
| eventSubtype | 其他事件详细信息（如果可用） |
| actorEmail | 执行事件的管理员的电子邮件地址。 如果事件是由Adobe后端系统执行的，则显示&#x200B;*系统*。 |
| targetUserEmail | 受影响用户的电子邮件（如果适用） |
| targetGroupName | 受影响的用户组（如果适用） |
| targetProductName | 受影响的产品（如果适用） |
| targetProfileName | 受影响的产品配置文件（如果适用） |
| ipAddress | 执行操作的计算机的IP地址。 通常反映物理位置，但可以是代理服务器或VPN地址。 |
| organizationName | 受影响组织的名称 |

## 下载导出报告

当任何全局管理员从[Global Admin Console](https://global-admin-console.adobe.com/insights)导出组织数据时，将在&#x200B;**[!UICONTROL 导出报告]**&#x200B;的&#x200B;**[!UICONTROL 分析]**&#x200B;选项卡下处理该报告并提供该报告。

任何全局管理员生成的所有报告都在一个位置提供。 导出报表功能在以下情况下很有帮助：

- 如果您有一个包含许多组织的大型层次结构，则无需再等待导出文件进行处理。 您可以使用其他管理员生成的报告。
- 您不再需要保留或保存这些报告以便将来进行比较。 报告会保留90天，您可以随时下载它们以比较报告。


要下载导出报告，请执行以下操作：

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/insights)，然后导航到&#x200B;**[!UICONTROL 分析]** > **[!UICONTROL 导出报表]**。

   此时会显示过去90天内生成的报告。 90天完成后，您可以再次生成报表。 了解如何生成[组织结构](https://helpx.adobe.com/cn/enterprise/global-admin-console/export-and-import-data.html#export-and-import-organization-structure)的报告。


   | 字段 | 描述 |
   |------|------------|
   | 报表 | 生成报告的日期和时间（当地时区） |
   | 格式 | 文件格式(CSV、JSON、XLSX) |
   | 大小 | 文件大小 |
   | 创建者 | 生成报告的管理员的电子邮件地址 |
   | 操作 | 用于下载报告的链接 |

1. 要下载报表，请选择&#x200B;**[!UICONTROL 下载]**。

   如果刚刚生成的报告未出现在列表中，请选择&#x200B;**[!UICONTROL 刷新]**。

   ![export-reports](assets/export-reports.png)

*下载过去90天内生成的任何报告。*
