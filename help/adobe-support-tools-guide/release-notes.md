---
title: 新的EXL案例表单发行说明
description: EXL案例表单的最新发行信息。
feature: Release Notes
source-git-commit: 421ef19ed939cd757e3182c8fa5bbda13fd7561e
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 6%

---


# 新的EXL案例表单发行说明

新的案例创建体验引入了更新的表单，旨在简化问题的解决，其中包括：

![新](../adobe-support-tools-guide/assets/new.svg) - 新功能
![修复](../adobe-support-tools-guide/assets/fix.svg) - 修复和改进
![错误](../adobe-support-tools-guide/assets/bug.svg) - 已知问题

## 1.0版 — 增强型案例创建表单

*2026年1月15日*

![新](../adobe-support-tools-guide/assets/new.svg)案例表单已组织为引导式流程，可帮助用户了解每个阶段需要哪些信息：

- [!UICONTROL 产品选择]
- [!UICONTROL 问题详细信息]
- [!UICONTROL 系统信息]
- [!UICONTROL 影响]
- [!UICONTROL 联系人信息]
- [!UICONTROL 审阅并提交]

![新](../adobe-support-tools-guide/assets/new.svg)添加了&#x200B;**要重新生成[!UICONTROL 字段的新]步骤**&#x200B;以捕获可操作详细信息并加快故障排除。

![新](../adobe-support-tools-guide/assets/new.svg)已添加授权产品的&#x200B;**其他[!UICONTROL 环境上下文]字段**&#x200B;以捕获关键详细信息：

- **Marketo**
   - Munchkin ID
- **Adobe Target**
   - 活动名称
   - 站点URL（标记属性名称）/HAR或Assurance日志
- **Adobe Analytics**
   - RSID
   - 站点URL（标记属性名称）/HAR或Assurance日志/cURL/调试日志
   - Workspace短链接
- **Adobe Journey Optimizer (AJO)**
   - 历程ID或历程URL
   - 示例配置文件
- **Real-Time Customer Data Platform (RTCDP)**
   - 受影响的组件ID（目标ID、配置文件ID、受众ID、数据集ID或数据流ID）
   - HAR文件/Assurance日志
- **Customer Journey Analytics (CJA)**
   - Workspace项目
   - 标记属性名称


![New](../adobe-support-tools-guide/assets/new.svg)添加了&#x200B;**AI驱动的[!UICONTROL 推荐面板]**，以便在不中断案例创建流程的情况下显示有用的指导。

![新](../adobe-support-tools-guide/assets/new.svg)添加了[!UICONTROL 审核摘要]步骤，以提供所有输入信息的合并视图，并允许用户：

- 在一个位置查看案例详细信息
- 导航回之前的步骤以进行编辑
- 返回到摘要而不会失去进度

![修复](../adobe-support-tools-guide/assets/fix.svg)将案例描述字段重命名为&#x200B;*[!UICONTROL “请描述问题”]*&#x200B;以提高清晰度。

![Fix](../adobe-support-tools-guide/assets/fix.svg)添加了星号(*)作为必填字段指示符，以确保完整性和减少提交错误。
