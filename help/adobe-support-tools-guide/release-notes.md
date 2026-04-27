---
title: Experience League支持发行说明
description: 有关Experience League支持的最新发行信息。
feature: Release Notes
exl-id: 875ad82e-56b5-4d58-9237-bb7aa0d9ffaf
source-git-commit: 26a20998811059cf66d8609c0ae7ac2816df3337
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 1%

---

# Experience League支持发行说明

这些发行说明包含对Experience League支持的更新，其中包括：

![新](../adobe-support-tools-guide/assets/new.svg)新功能
![修复](../adobe-support-tools-guide/assets/fix.svg)修复和改进
![错误](../adobe-support-tools-guide/assets/bug.svg)已知问题


## 2026年4月27日 — Adobe Commerce的升级管理和系统分析增强功能

### 上报管理

1. Experience League支持上报管理提供了一系列新的自助服务功能，让您能够基于自己的需求构建一个简化的系统驱动工作流，从而更加深入地了解您的支持案例。

1. 获取支持AI的即时支持案例快照，包括当前状态、后续步骤、关键更新和完整案例摘要，而无需阅读整个案例历史记录。

1. 新的&#x200B;**[!UICONTROL 获取帮助]**&#x200B;选项为客户提供了与支持团队无缝协作的集中化体验 — 涵盖故障排除、回调请求、自助问题紧急更新以及管理关注请求。

1. **[!UICONTROL 请求立即致电]** — 对于P1关键案例，请直接从您的案例列表请求技术支持工程师立即回电。 只需提供您的电话号码和问题的简要说明，支持工程师将在提供时立即联系。

1. **[!UICONTROL 请求已安排的通话]** — 对于P2紧急和P3重要情况，请安排与技术支持工程师在适合您的日期和时间举行Web会议。 Microsoft Teams屏幕共享会话将在预订时进行确认，并包含所有会议详细信息。

1. **[!UICONTROL 问题紧迫性更改]** — 对于P3-Important和P4-Minor案例，自助服务会提供简短理由，将您的案例优先级从P4-Minor提升到P2-Important。 在没有票证导致重新分配的情况下，优先级请求可能会发生更改。

1. **[!UICONTROL 我有一个问题未列出]** — 对于所有优先级，针对上述选项未涵盖的任何情形上报问题，例如&#x200B;**[!UICONTROL 解决时间]**、**[!UICONTROL 解决方法未达到预期]**、**[!UICONTROL 代理沟通技能]**&#x200B;或&#x200B;**[!UICONTROL 代理技术知识]**。

### Adobe Commerce案例创建表单中的系统分析

1. System Insights会自动显示环境中检测到的问题。 它包含使用API、New Relic和[!DNL Splunk]中的遥测数据的性能下降、安全风险和配置错误。 这有助于您更快地识别和解决问题。

1. 在案例创建过程中，系统分析当前仅可用于Experience League支持的Adobe Commerce。

1. 分析仅限于您的特定项目实例，确保呈现的信息与您的环境相关。

1. 分析内容包括详细说明、解决步骤、根本原因分析以及相关Adobe文档的链接。

1. 用户可以提交关于个人见解的反馈，以帮助Adobe持续改进System Insights的准确性和相关性。

## 2026年4月23日 — 扩展“请求回调”功能

Analytics、Admin Console、Audience Manager和Target产品用户现在可以使用“请求回调”功能。

## 2026年4月8日 — 扩展“请求回调”功能

Marketo产品用户现在可以使用“请求回调”功能。

## 2026年3月30日 — 增强型案例表单

![新](../adobe-support-tools-guide/assets/new.svg)案例表单组织为引导式流程，可帮助用户了解每个阶段需要哪些信息：

- [!UICONTROL 产品选择]
- [!UICONTROL 问题描述]
- [!UICONTROL 系统信息]
- [!UICONTROL 优先级和业务影响]
- [!UICONTROL 联系信息和观察者列表]
- [!UICONTROL 审阅并提交]

![新](../adobe-support-tools-guide/assets/new.svg)已添加基于&#x200B;**[!UICONTROL 问题描述]**&#x200B;的自动标题生成，允许自动生成标题，同时仍允许用户在提交案例前编辑标题。

![新](../adobe-support-tools-guide/assets/new.svg)添加了&#x200B;**[!UICONTROL “问题是否可以复制？”]** 选项，以帮助改进故障排除。 如果用户选择&#x200B;**[!UICONTROL 是]**，系统将提示他们提供重现问题的步骤。 如果选择&#x200B;*否*，则用户可以继续提交案例。

![新](../adobe-support-tools-guide/assets/new.svg)添加了一个选项，用于指示最近是否对环境或实例进行了任何更改。 如果选择&#x200B;**[!UICONTROL 是]**，将提示用户提供有关更改的其他详细信息。

![新](../adobe-support-tools-guide/assets/new.svg)已添加授权产品的&#x200B;**其他[!UICONTROL 环境上下文]字段**&#x200B;以捕获关键详细信息：

- **Marketo**
   - Munchkin ID
- **Adobe Target**
   - 活动名称
   - 站点URL（标记属性名称）
- **Adobe Analytics**
   - RSID
   - 站点URL（标记属性名称） / cURL
   - Workspace短链接
- **Adobe Journey Optimizer (AJO)**
   - 历程ID或URL/促销活动ID或URL/渠道ID或URL/Offer Decisioning ID或URL
   - 示例配置文件
   - 沙盒名称
- **Real-Time Customer Data Platform (RTCDP)**
   - 受影响的组件ID（目标ID/受众ID/数据集ID/数据流ID/合并策略ID/架构ID/Source ID/批处理ID）
   - 示例配置文件
   - 沙盒名称
- **Adobe Experience Platform (AEP)**
   - 受影响的组件ID（目标ID/受众ID/数据集ID/数据流ID/合并策略ID/架构ID/Source ID/批处理ID）
   - 示例配置文件
   - 沙盒名称
- **Customer Journey Analytics (CJA)**
   - Workspace项目URL
   - 连接ID /错误消息/代码
   - 数据视图ID

![New](../adobe-support-tools-guide/assets/new.svg)添加了&#x200B;**AI驱动的[!UICONTROL 推荐面板]**，以便在不中断案例创建流程的情况下显示有用的指导。

![新](../adobe-support-tools-guide/assets/new.svg)添加了&#x200B;**[!UICONTROL 审核摘要]**&#x200B;步骤，以提供所有输入信息的合并视图，并允许用户：

- 在一个位置查看案例详细信息
- 导航回之前的步骤以进行编辑
- 返回到摘要而不会失去进度

![修复](../adobe-support-tools-guide/assets/fix.svg)将案例描述字段重命名为&#x200B;*[!UICONTROL “请描述问题”]*&#x200B;以提高清晰度。

![Fix](../adobe-support-tools-guide/assets/fix.svg)添加了星号(*)作为必填字段指示符，以确保完整性和减少提交错误。

## 2026年3月18日 — 扩展“请求回调”功能

Experience League现在提供了一个“请求回调”选项，通过屏幕共享功能启用自助服务Web会议时间安排，以便更快地解决问题。

- 此功能适用于Adobe Experience Manager、Campaign和Workfront。
- 客户可以在方便的时候安排会议，并接收即时邀请。
- 对于Adobe Experience Manager P1案例，即时回调确保在关键问题期间更快地参与，从而帮助将停机时间和对业务的影响降至最低。
