---
title: Adobe Commerce假日准备概述
description: 在云基础架构环境中为假期之类的高流量事件准备Adobe Commerce的执行级别指南。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/63svzoaJbKTgiO3iJR3iCyr4-slOLmt4QaVT2Y--NYI'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 7ffe3c23f94b67342f02ed655d0a1700dd8f5a02
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%
---

# Adobe Commerce假日准备概述

本行动手册提供了有关准备Adobe Commerce环境以进行高流量活动（如假日季节）的指南。 该战略将技术建议整合为五个战略重点领域：

- 性能优化
- 最佳实践和稳定性
- 监控和可观察性
- 可扩展性和容量规划
- 运行就绪

这些重点领域有助于确保您的平台在峰值负载下保持稳定、安全和性能。

## 性能优化

以下是确保优化性能的建议步骤概述。 有关详细信息，请参阅[Adobe Commerce假日准备工作>性能优化](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/performance-optimization.md)。

* 优化Fastly请求缓存：标准化您的促销跟踪参数，确认您的登陆页面可缓存，并使用适用于PWA或Headless店面的GraphQL GET提高您的Fastly缓存命中率。
* 启用Fastly IO：打开Fastly图像优化和深度IO，以便图像转换在CDN边缘而不是源位置运行，从而缩短图像密集型商店的页面渲染时间。
* 启用二级缓存：将缓存数据存储在每个Web节点的本地，以缩短延迟并减少对Redis/Valkey的网络调用，具体取决于您的Adobe Commerce版本。 Adobe Commerce 2.4.9或更高版本的2.4.5-p16、2.4.6-p14、2.4.7-p9和2.4.8-p4修补程序不支持Redis缓存。
* 启用从属连接：将重读查询路由到具有`MYSQL_USE_SLAVE_CONNECTION`和`REDIS_USE_SLAVE_CONNECTION`或`VALKEY_USE_SLAVE_CONNECTION`的副本节点，使主数据库不是负载下的瓶颈。
* 启用异步订单和电子邮件处理：队列订单下达、订单数据网格更新和结账电子邮件可在后台跨三个单独的设置运行，因此结账速度在高订单量下保持快速。
* 将索引器切换到“按计划更新”模式：将索引器从“保存时更新”移动到cron驱动的“按计划更新”模式，以避免在频繁更新目录期间锁定 — customer_grid索引器除外。
* 考虑扩展（拆分）体系结构：如果调整和代码级修复仍使CPU在负载下达到极限，请迁移到可独立扩展Web和数据库节点的六节点拆分层设置。

## 最佳实践和稳定性

以下是确保实例稳定性的最佳实践概述。 有关每个选项的详细步骤，请参阅[Adobe Commerce假日准备情况>最佳实践和稳定性](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/best-practices-stability.md)。

* 升级到最新的Adobe Commerce版本：保持在受支持的版本以保留Adobe在每个版本中提供的安全修复和性能改进。
* 安装最新的ECE-Tools和Quality Patch Tool (QPT)：更新ece-tools及其依赖项，并确认对云和本地安装都应用了适用的质量修补程序工具修复。
* 查看和清理日志文件：删除调试日志并监控重复错误，以防止磁盘过度使用并改善日志可见性。
* 监控磁盘大小增长：将共享文件和数据库卷的使用率保持在70%以下，以便存储增长不会触发中断。
* 查看慢速数据库查询：使用APM工具和MySQL慢速查询日志查找和修复代价高昂的查询，然后将其复合到高峰流量下。
* 正确配置cron作业：确认cron在正确的用户下每分钟运行一次，因为Commerce中的每个异步操作都依赖于它。
* 优化客户端设置：打开CSS、JavaScript和HTML缩小和捆绑功能，以加快店面加载速度。

## 监控和可观察性

以下是旺季期间监控Adobe Commerce实例的推荐方法。 有关每个监控和观察性建议的详细步骤，请参阅[Adobe Commerce假日准备情况>监控和观察性](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/monitoring-observability.md)。

* 使用New Relic监控流量：使用流式传输到New Relic的Fastly日志发现流量异常、滥用IP、针对支付等端点的恶意请求以及设备/浏览器趋势。
* 自定义New Relic警报：在Adobe托管警报的基础上，针对异常流量、GraphQL查询速度缓慢或错误率不断上升的情况，自行设置基于NRQL的警报。
* 跟踪Apdex得分：观看Apdex得分（目标≥0.85），以将后端和前端响应时间保持在用户认为满意的范围内。
* 查看支持见解（SWAT报告）：在峰值事件之前和之后运行SWAT报告，以确定系统级风险和改进领域。

## 可扩展性和容量规划

有关每个可扩展性和容量规划建议的详细步骤，请参阅[Adobe Commerce假日准备情况>可扩展性和容量规划](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md)。

* 提前规划集群升级：在重大升级之前至少10个工作日，向Adobe支持部门请求临时计算升级。
* 启用Fastly源屏蔽：通过位于您源附近的Shield POP路由未缓存的请求，以减少直接命中源服务器的请求。
* 执行加载和故障转移测试：在主要活动之前测试加载和恢复方案，以确认您的扩展和回滚计划实际有效。

## 运行就绪

* 应用所有安全和性能修补程序：在代码冻结之前完成所有修补程序，以便以后不会中断部署。
* 运行假日前运行状况检查：测试备份、cron运行状况和缓存热备份脚本，以使操作在负载下平稳运行。
* 建立监控行动手册：记录警报阈值、上报路径和全天候联系，以便团队能够在高峰期快速响应。
* 记录回滚计划：使版本化的回滚策略准备就绪，以便您可以从错误的部署中快速恢复。