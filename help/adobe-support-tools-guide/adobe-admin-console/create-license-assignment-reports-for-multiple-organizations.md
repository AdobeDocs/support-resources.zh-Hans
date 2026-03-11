---
title: 为多个组织和产品创建许可证分配报告
description: 从Global Admin Console生成、查看和下载跨多个组织和产品的许可证分配报告。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 1ab0cf0f1e813e3d7cd594c60cd2d58e4f09c072
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 1%

---

# 为多个组织和产品创建许可证分配报告

了解全局管理员如何针对特定日期范围生成和下载多个组织和产品的详细许可证报告，以促进对许可证配置的精确跟踪。

&#x200B;> [!NOTE]
>
> 要创建、查看和导出许可证分配报告，请登录到[Global Admin Console](https://global-admin-console.adobe.com/)，然后转到&#x200B;**[!UICONTROL 分析]** > **[!UICONTROL 报告]** > **[!UICONTROL 许可证分配]**。

## 创建报告

许可证分配报告可帮助您主动监控许可证配置并减少手动跟踪。 全局管理员可以为任意数量的子组织创建选定产品的许可证分配报告，以监控所有部门的软件许可证设置数据。

1. 转到Global Admin Console中的&#x200B;**[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)**&#x200B;选项卡。
2. 在&#x200B;**[!UICONTROL 许可证分配]**&#x200B;页面上，选择&#x200B;**[!UICONTROL 创建报告]**。
3. 选择组织，然后选择&#x200B;**[!UICONTROL 下一步]**。 您可以使用&#x200B;**[!UICONTROL 全选]**&#x200B;按钮分别选择每个组织或选择父组织内的所有子组织。
   &#x200B;> [!NOTE]
   >
   >**了解为什么不能选择某些组织**：
   >如果子组织没有合同，或者与父组织的产品具有单独的企业合同，则子组织将无法创建许可证分配报表。 例如，如果父组织的合同具有Adobe Acrobat，而子组织与其他合同的一部分具有相同，则产品分配受到限制。 因此，在Global Admin Console中创建报表时也会受到限制。 [了解如何使用此类组织各自的Admin Console](https://helpx.adobe.com/enterprise/using/assignment-reports.html)跟踪配置。
   >
   > [!NOTE]
   >
   > 您只能为具有有效合同的组织创建分配报表。
4. 选择要包含在报告中的产品，然后选择&#x200B;**[!UICONTROL 下一步]**。
   &#x200B;> [!NOTE]
   >
   >**了解为什么不能选择某些产品**：
   >在Global Admin Console中无法分配的产品不包括在报表创建中。 这目前包括一些数字体验产品，如[!DNL Workfront]、[!DNL Adobe Experience Manager]和[!DNL Adobe Experience Platform]，以及产品，如[!DNL Adobe Firefly Services]、[!DNL Acrobat Sign]和[!DNL Adobe Stock]。 [您使用Adobe Admin Console查找这些产品的许可证配置数据](https://helpx.adobe.com/enterprise/using/assignment-reports.html)。
5. 选择是按月还是按年汇总报表。
6. 选择自定义日期范围或从预设选项中进行选择。 您可以选取从2020年6月18日开始一直到前一天的任何开始日期，只要该日期不早于合同开始日期。
7. 选择&#x200B;**[!UICONTROL 下载]**&#x200B;以将报告导出为CSV文件。

报告开始处理，并出现在&#x200B;**[!UICONTROL 许可证分配]**&#x200B;页面上，其中包含名称、创建者、创建时间、日期范围和状态等详细信息。 准备就绪后，您将收到电子邮件通知，并且报告会自动下载。

任何全局管理员都可以在报告准备就绪后随时使用报告名称旁边的&#x200B;**[!UICONTROL 下载]**&#x200B;图标下载报告。

>[!NOTE]
>
>- 要确保反映最新数据，请在分配后48小时内生成报表。
>- 报告在生成后会保留90天。

## 查看和下载以前生成的报告

全局管理员可以查看和下载由贵组织中的任何其他全局管理员生成的许可证分配报告。 但是，全局查看者只能查看许可证分配报告的列表。

1. 转到Global Admin Console中的&#x200B;**[[!UICONTROL Insights]](https://global-admin-console.adobe.com/insights)**&#x200B;选项卡。
1. 在&#x200B;**[!UICONTROL 许可证分配]**&#x200B;页面上，列出了所有报告以及以下详细信息：

   | 字段 | 描述 |
   | ------------- | ------------------------------------------------------------------------------------------------- |
   | 名称 | 自动生成且无法编辑。 |
   | 创建者 | 生成报告的全局管理员。 |
   | 创建时间 | 创建报告时的系统时间。 |
   | Date range | 为报表选择的日期范围。 |
   | 状态 | 如果报告已可供下载，则返回&#x200B;**成功**；如果仍在生成报告，则返回&#x200B;**正在处理**。 |

1. 要将报表导出为CSV文件，请选择报表旁边的&#x200B;**[!UICONTROL 下载]**&#x200B;图标。

## 了解您的许可证分配报告

您下载的报表包含每个事件的以下信息：

| 字段 | 描述 |
| -------------------------------- | -------------------------------------------------------- |
| 组织 ID | 与父组织关联的唯一ID |
| 组织名称 | 父组织的名称 |
| 子组织Id | 所选子组织的唯一标识符 |
| 子组织名称 | 子组织的名称 |
| 许可证ID | 产品许可证的唯一ID |
| 产品名称 | 所选产品的名称 |
| 日期 | 日期选择 |
| 许可证数量总计 | 父组织级别的许可证总数 |
| 子许可证 | 分配给子组织的许可证计数 |
| 每月/每年峰值分配数量 | 许可证配置的合计值（每月/每年） |
