---
title: 系统分析
description: 系统分析可主动识别Adobe Commerce环境中的潜在问题。 在案例创建期间查看见解可减少解决时间，有助于防止中断，并支持稳定而安全的部署。
source-git-commit: 4172c364c9bfffaae13759da882d03daa15d0754
workflow-type: tm+mt
source-wordcount: '741'
ht-degree: 0%

---

# 系统分析

系统分析提供主动调查结果，帮助在Adobe产品设置中识别性能、安全性和功能方面的潜在问题。 这些洞察会根据从可观察性工具（包括API、New Relic和[!DNL Splunk]）收集的遥测数据来显示风险，例如性能下降、安全漏洞或配置不正确。

系统分析在案例创建过程中出现，有助于加快诊断和解决问题。

## 如何创建系统分析

Adobe团队持续分析常见的支持问题和新趋势。 Adobe会根据这些发现为系统添加自动检查功能。

这些检查可扫描产品设置，以检测配置错误、作业停滞或可能导致功能问题或系统停机的情况。

当检查标识的值或状态超出Adobe产品和支持团队定义的安全范围时，系统将其显示为System Insight。

## 为什么系统分析很重要

定期查看系统分析有助于在问题影响系统稳定性或客户体验之前及早发现问题。 这种积极主动的方法是：

- 提高平台可靠性
- 减少停机时间
- 帮助维护Adobe推荐的最佳实践

## 可用性和范围

系统分析当前仅适用于Adobe Commerce。 这些见解显示在Experience League支持的案例创建过程中，并可通过[站点范围分析工具(SWAT)](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/tools/site-wide-analysis-tool/intro)获得。

> [ !N注意]
>
>系统分析仅显示生产环境的数据。

## 访问系统分析

系统分析会在整个案例创建工作流中显示。 输入问题详细信息后，**[!UICONTROL 系统分析]**&#x200B;面板将显示在屏幕右侧，AI支持的推荐部分下方。 要了解有关AI支持的推荐的更多信息，请参阅Adobe客户支持体验一文中的[填写支持工单](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#fill-out-the-support-ticket)。

该面板显示一个可滚动的见解列表，这些见解限于特定项目实例。 范围设定基于&#x200B;**[!UICONTROL 项目URL]**&#x200B;字段中输入的信息。 准确地输入&#x200B;**[!UICONTROL 项目URL]**&#x200B;以确保分析反映正确的环境。

加载面板后，它会显示一个可滚动的列表，其中包含为您的环境标记的insight卡片。 每个insight卡包括：

- 摘要问题的标题
- insight的简短说明

![访问支持资源](/help/adobe-support-tools-guide/assets/access-support-resources.png)

要查看完整的insight详细信息，请从列表中选择一个insight卡。 详细视图提供以下信息：

- insight名称
- 标记insight的Adobe产品
- insight类型，分类为：
   - [!UICONTROL 功能]
   - [!UICONTROL 性能]
   - [!UICONTROL 安全性]
- [!UICONTROL 风险级别]表示严重程度
- [!UICONTROL 上次检查运行]指示何时检测到调查结果。
- [!UICONTROL Insight Source]，由站点范围分析工具(SWAT)提供
- 详细解释问题及其潜在影响，以及调查和解决问题的可操作步骤。 详细视图还说明了此类型问题的典型原因，并包含指向相关Adobe文档的链接以供进一步参考。

![点击案例卡](/help/adobe-support-tools-guide/assets/click-case-card.png)

在继续操作之前，请查看面板中的所有洞察，因为insight可以直接解决所遇到的问题。

## 对insight执行操作

复查insight后，选择以下操作之一。

### 继续创建案例

如果问题仍然存在，或需要其他帮助，请选择&#x200B;**[!UICONTROL 继续创建案例]**。 系统将保留所有以前输入的案例信息。

### 将问题标记为已解决

如果insight解决了问题并且不再需要某个支持案例，请选择&#x200B;**[!UICONTROL 已解决的问题]**。

选中此选项时：

- 将显示确认对话框。
- 该对话框指示将永久清除所有输入的案例数据。

在insight上执行![操作](/help/adobe-support-tools-guide/assets/issue-resolved.png)

选择&#x200B;**[!UICONTROL 完成]**&#x200B;以确认并返回&#x200B;**[!UICONTROL 我的案例]**&#x200B;页面。 选择&#x200B;**[!UICONTROL 取消]**&#x200B;以返回insight详细信息视图。

![清除案例表单](/help/adobe-support-tools-guide/assets/clear-case-form.png)

## 提供insight反馈

在每个insight详细信息视图的底部，可以提供insight是否有用的反馈。 此反馈有助于Adobe持续改进System Insights的相关性和准确性。

![提供反馈](/help/adobe-support-tools-guide/assets/submit-feedback.png)

要提供反馈，请执行以下操作：

1. 打开insight详细信息视图。
2. 滚动到面板底部。
3. 找到提示&#x200B;**[!UICONTROL 这是否有帮助？ 发送反馈。]**
4. 选择以下选项之一：
   - 如果insight有帮助，请&#x200B;**竖起缩略图**&#x200B;图标
   - 如果insight没有帮助，请&#x200B;**向下缩略图**&#x200B;图标
5. （可选）输入其他注释。
6. 选择&#x200B;**[!UICONTROL 提交]**&#x200B;以发送反馈，或选择&#x200B;**[!UICONTROL 解除]**&#x200B;以关闭反馈部分而不提交。
