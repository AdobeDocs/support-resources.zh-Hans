---
title: 新体验联盟案件表格发布说明
description: EXL案件表格的最新发布信息。
feature: Release Notes
source-git-commit: 7bca9c4ae25c77092de6957193ceecd146d19a1a
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 6%

---


# 新体验联盟案件表格发布说明

新的案例创建体验引入了更新的表单，旨在简化问题的解决，其中包括：

![新](../adobe-support-tools-guide/assets/new.svg) - 新功能
![修复](../adobe-support-tools-guide/assets/fix.svg) - 修复和改进
![错误](../adobe-support-tools-guide/assets/bug.svg) - 已知问题

## 1.0版本——增强型案件创建表格

*2026年1月15日*

![新件](../adobe-support-tools-guide/assets/new.svg) 案例表单组织成引导流程，帮助用户了解每个阶段所需的信息：

- [!UICONTROL 产品选择]
- [!UICONTROL 问题详情]
- [!UICONTROL 系统信息]
- [!UICONTROL 影响]
- [!UICONTROL 联系方式]
- [!UICONTROL 审阅并提交]

![新](../adobe-support-tools-guide/assets/new.svg)添加了&#x200B;**要重新生成[!UICONTROL 字段的新]步骤**&#x200B;以捕获可操作详细信息并加快故障排除。

![新](../adobe-support-tools-guide/assets/new.svg)已添加授权产品的&#x200B;**其他[!UICONTROL 环境上下文]字段**&#x200B;以捕获关键详细信息：

- **马凯托**
   - Munchkin ID
- **Adobe Target**
   - 活动名称
   - 网站URL（标签、属性名称）/ HAR或保证日志
- **Adobe Analytics**
   - RSID
   - 站点URL（标签、属性名称）/ HAR或保证日志 / cURL / 调试日志
   - Workspace短链接
- **Adobe Journey Optimizer (AJO)**
   - 历程ID或历程URL
   - 示例配置文件
- **实时客户数据平台（RTCDP）**
   - 受影响的组件ID（目标ID、配置文件ID、受众ID、数据集ID或数据流ID）
   - HAR文件 / 保证日志
- **客户旅程分析（CJA）**
   - 工作空间项目
   - 标签 物业名称


![New](../adobe-support-tools-guide/assets/new.svg)添加了&#x200B;**AI驱动的[!UICONTROL 推荐面板]**，以便在不中断案例创建流程的情况下显示有用的指导。

![新](../adobe-support-tools-guide/assets/new.svg)添加了[!UICONTROL 审核摘要]步骤，以提供所有输入信息的合并视图，并允许用户：

- 在一个位置查看案例详细信息
- 导航回之前的步骤以进行编辑
- 返回摘要而不丢失进度

![修正](../adobe-support-tools-guide/assets/fix.svg) 更名的案件描述字段为 *[!UICONTROL “请描述问题”]* 以提升清晰度。

![修正](../adobe-support-tools-guide/assets/fix.svg) ：新增星号（*）作为强制字段指示，以确保完整性并减少提交错误。
