---
title: Adobe DX解决方案统一假日准备指南
description: 为AEP、AJO、CJA、Commerce、AEM、Marketo、Workfront、Campaign、Analytics和Target做好Adobe DX假日准备工作，以帮助您规划、扩展、安全和优化。
solution: Experience Platform, Journey Optimizer, Customer Journey Analytics, Commerce, Experience Manager, Workfront, Campaign, Analytics, Target, Marketo Engage
role: Developer, Admin, Leader, User
index: true
source-git-commit: 3d8acc3aabdb7de154ecce45f28c493033193096
workflow-type: tm+mt
source-wordcount: '3827'
ht-degree: 1%

---

# Adobe DX解决方案统一假日准备指南


Adobe DX解决方案统一假日准备指南将重点放在主动规划而不是被动解决问题上，帮助您为假日季节做好准备。 它提供了切实可行的步骤来确保实例已准备就绪，从而最大限度地减少潜在问题。 Adobe团队带来了技术专业知识、多种功能和经验证的方法，可提供适当级别的支持和指导（包括技术和战略支持），让您的业务做好充分准备。

请遵循以下最佳实践，确保您的Adobe数字体验解决方案可复原、安全且为假期流量高峰做好准备：

* 计划增加流量。
* 避免在窗口高峰期发生重大更改；在假日季节之前或之后安排更新。
* 使用功能板和警报监控性能并及早发现瓶颈。
* 确保您的授权支持联系人为最新状态。
* [尽可能提前联系Adobe支持部门](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket)。

有关Adobe中特定于解决方案的假日准备建议，请参阅以下部分。

* [Adobe Experience Platform](#aep)
* [Adobe Journey Optimizer](#ajo)
* [Adobe Customer Journey Analytics](#cja)
* [Adobe Commerce](#commerce)
* [Adobe Experience Manager](#aem)
* [Adobe Marketo](#marketo)
* [Adobe Workfront](#workfront)
* [Adobe Campaign](#campaign)
* [Adobe Analytics](#analytics)
* [Adobe Target](#target)

>[!NOTE]
>
>单击每个部分以展开它。


## Adobe Experience Platform (AEP)假日准备指南 {#aep}

+++**单击以查看Adobe Experience Platform (AEP)假日准备建议。**

Adobe Experience Platform (AEP)在提供实时客户体验方面起着关键作用。 随着假日季节的临近，确保您的AEP实施针对增加流量、安全数据处理和可扩展引入进行优化至关重要。

### 预测季节性需求

为了准备应对季节性流量尖峰，Adobe建议规划容量并监控流式配置文件摄取。 这包括预测数据量，并确保您的系统能够处理增加的吞吐量。 请参阅[容量和季节性流量的计划](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile)以供参考。

### 准备扩展

Adobe提供了多种策略来确保您的环境为假期流量做好准备：

* 增加沙盒的分配容量。
* 识别[监视仪表板](https://experienceleague.adobe.com/en/docs/experience-platform/dataflows/ui/monitor-streaming-profile)中的高吞吐量数据流，并根据需要应用限制或过滤。
* 使用针对低延迟用例的批量摄取来优化性能，如[许可证使用和容量：流式传输最佳实践](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions)中所述。

这些实践有助于在峰值期间保持摄取可靠性并减少延迟。

### 最佳实践和防护

为了保持在操作限制范围内并避免服务中断，Adobe建议遵循以下引入和配置文件护栏：

* [流吞吐量最佳实践](https://experienceleague.adobe.com/en/docs/experience-platform/landing/license/capacity#suggestions)
* 用于数据引入的[护栏](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/ingestion/guardrails)
* [实时客户个人资料数据和细分的默认护栏](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/guardrails)
* [AEP Blueprint：护栏](https://experienceleague.adobe.com/en/docs/blueprints-learn/architecture/architecture-overview/guardrails)

### 安全和治理

Adobe强调强大的安全和治理实践，尤其是在高流量季节中，此时数据敏感性会提高。

有关如何在Adobe Experience Platform实施中保护客户数据、实施隐私控制以及维护合规性的建议，请参阅[AEP：安全性](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/overview#security)。

通过遵循这些准则并利用Adobe的公共文档，组织可以确保其Adobe Experience Platform可复原性、安全性并准备好在整个假日季节提供卓越的客户体验。

+++

## Adobe Journey Optimizer (AJO)假日准备指南 {#ajo}

+++**单击以查看Adobe Journey Optimizer (AJO)假日准备建议。**


为了准备Adobe Journey Optimizer以应对假日季节，组织应该预测事件峰值和跨渠道复杂性，配置历程和频度规则，并确保数据卫生和决策逻辑。 它们还必须验证大规模性能、强制实施安全和API护栏，并应用峰值后分析来优化未来的营销活动。

### 预测需求

* 根据假日季节压缩和更大的促销活动量，预计：
   * 实时事件激增并触发了历程（购物车放弃、最新优惠）
   * 报文饱和度风险（更高的选择退出率、疲劳）
   * 增加了跨渠道复杂性（电子邮件+推送+短信+应用程序内）
* 使用去年的指标（打开/点击/选择退出率、历程进入量）对预期负载进行建模，并设置消息传递系统的阈值。
* 确定可能的“安静时段”或性能不佳时段（例如：周末、假日），并相应地规划发送量。

### 准备扩展

* 确保AJO中的所有渠道配置均已正确设置：电子邮件、推送、短信、Web、应用程序内。 请参阅[设置渠道配置](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/channel-surfaces)。
* 配置频率上限和上限规则以控制消息量。 请参阅[频率封顶](https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer-learn/tutorials/configuration/business-rules/configure-frequency-capping-rules)文章。
* 配置渠道/历程规则集：请参阅[使用规则集](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/capping-rules/rule-sets)。
* 准备数据卫生/实时事件流和分段框架。
* 确保您为假日营销活动定义了目标受众，例如：
   * 高价值客户
   * 忠诚的区段
   * 购物车放弃者
   * 首次购买者
* 为假期历程预加载或准备模板，利用决策逻辑（优惠/约束），以便您可以根据库存、对时间敏感的优惠和渠道首选项动态调整。 请参阅[将约束添加到优惠](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/decisioning/offer-decisioning/managing-offers-in-the-offer-library/configure-offers/add-constraints)文章中的示例。
* 技术就绪性：确认API/端点加载能力、自定义操作的限制/上限规则以及外部集成。 请参阅[护栏和限制](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/guardrails)。

### 测试和验证

* 使用试验框架测试关键变量更改：
   * 发送时间
   * 优惠类型
   * 渠道组合
请参阅[AJO Experimentation Accelerator最佳实践](https://experienceleague.adobe.com/en/docs/experimentation-accelerator/using/get-started/experiment-accelerator-best-practices)。
* 进行端到端历程验证：
   * 事件触发器
   * 分段条目
   * 历程路径流
   * 个性化逻辑
   * 优惠约束
   * 退出条件
* 验证上限和冲突规则。 请参阅[历程上限和仲裁](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/conflict-prioritization/journey-capping)文章。
* 对峰值发送或峰值进行压力测试缩放的卷：模拟高触发卷，以验证系统在负载下的行为。
* 验证可投放性：预热电子邮件域/发件人，确认移动推送配置，并检查短信/应用程序内消息的备用渠道。

### 最佳实践

* 使用全渠道编排。 请参阅博客[参与度和增长的基本全渠道客户历程](https://business.adobe.com/blog/essential-customer-journeys-for-omnichannel-engagement)文章，该文章展示了AJO的假日季节示例。
* 在适当的时候优先考虑实时触发器。 例如：购物车放弃、浏览放弃和库存警报，因为节假日购物者更加被动反应。
* 利用分段和个性化：定位意图强烈的区段，根据过去的购买行为和偏好定制优惠。
* 对消息传送的疲劳程度最低：强制实施上限和静默时间，以避免过度招徕。 请参阅AJO中的[通过每日频率上限提升客户体验](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/elevate-customer-experience-with-daily-frequency-capping-in-ajo/ba-p/761510)博客帖子。
* 计时问题：计划提前在假日时段（给定压缩的季节）发送，并使渠道与时区和本地受众行为保持一致。
* 提供动态/限时优惠以创建紧迫感，并在各渠道之间协调以避免重复和冲突。
* 使用隐藏逻辑：隐藏刚刚购买的受众，或应用购买后历程以避免冗余消息传递。

### 安全和治理

* 确保配置了访问控制和权限，以便仅所需用户可以部署历程或修改业务规则。
* 监视并强制执行API调用/连接上限：例如，请参阅[上限API | Adobe Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/connect-systems/external-systems/capping)文章。
* 使用干净的第一方数据并确保正确进行身份拼接，以便以客户为中心的消息传送不会重复/错位。
* 确保可投放性域预热并部署反垃圾邮件措施，特别是对于高流量假日发送。
* 在旺季经常查看审核日志和历程更改，以尽早检测误运行或错误的历程。

### 峰后学习

* 在达到峰值负载后，对历程条目计数、抑制计数、选择退出率、可投放性指标和渠道性能进行审核。
* 清理抑制的区段，并暂停或停用为假日窗口构建的历程，以避免结转疲劳。
* 利用来自实时性能的见解完善下一年的计划（例如：发送时间调整、渠道组合和报文量）。

通过主动预测季节性需求、配置渠道和规则、验证历程性能以及强制实施安全和治理，组织可以确保Adobe Journey Optimizer在整个假日季节及之后提供无缝、个性化且可复原的客户体验。

+++

## Customer Journey Analytics (CJA)假日准备指南 {#cja}

+++**单击以查看Customer Journey Analytics (CJA)假日准备建议。**

Customer Journey Analytics使用5 P为假日/旺季做好准备。

### 准备扩展

* 查看CJA连接和数据视图；确定哪些连接和数据视图需要增强的监控和配置。
* 确认配置足以满足假日的扩展需要；根据需要扩展关键连接和数据视图。 有关详细信息，请参阅[管理连接](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/manage-connections)。

### 监控性能

* 利用RAM （[[!UICONTROL 报告活动管理器]概述](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)）实时监视活动和已排队的报告请求，识别容量不足的连接，并发现瓶颈。
* 使用[错误和疑难解答指南](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages)和[已知限制](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/aw-limitations)文章，查看在峰值负载期间延迟增加的情况。
* 使管理员能够通过RAM抢先挂起或取消长时间运行/受阻的请求。 请参阅CJA中的[取消报表请求](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-cancel-requests)一文。

### 最佳实践

* 安排在低流量期间导出/报告，以平滑加载并最大程度地减少延迟。 请参阅[计划报表](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/scheduled-projects-manager)文章。
* 分布请求：将报表安排在一天中的不同时间间隔。
* 减少面板、简化区段、缩短日期范围以及避免过多的并发作业。 有关详细信息，请参阅[优化CJA Workspace性能](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/optimizing-performance)一文。

### 故障排除

* 在排除工作区错误时，请参阅错误消息以了解原因和建议的操作；使用RAM （[!UICONTROL 报告活动管理器]）清除瓶颈并有效管理并发。 有关详细信息，请参阅[CJA Workspace错误处理](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/error-messages)。
* CJA使用RAM （[[!UICONTROL 中的]报告活动管理器](https://experienceleague.adobe.com/en/docs/analytics-platform/using/reporting-activity-manager/reporting-activity-overview)）来查明有问题的用户、查询或项目；根据需要排列优先顺序并终止/取消。

### 峰后学习

* 在假日/高峰期之后，审查性能和事件日志，以评估提供的最佳实践的影响。
* 查看慢查询和用户任务，以确定可以为下一季优化的模式/趋势。
* 从用户和利益相关者收集反馈 — 使用新获得的见解更新您自己的运行手册和准备计划。
* 通过您的客户团队向Adobe团队提供反馈。

+++

## Adobe Commerce假日准备指南 {#commerce}

+++**单击查看Adobe Commerce假日准备情况建议。**

为了确保您的组织能够度过一个成功的旺季，请务必为您的Adobe Commerce数字店面做好应对高流量的准备。

### 预测需求

* 在假日销售高峰期（11月中旬至1月中旬），Adobe建议所有托管在云基础架构中的Adobe Commerce商家通过提交假日激增容量请求来主动规划访客增长。 有关详细信息，请参阅云基础架构上的[Adobe Commerce的假期激增容量请求](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/announcements/commerce-announcements/holiday-surge-capacity-requests-for-magento-commerce-cloud)。

### 准备扩展

遵循[计划和透视：2025年高峰季战略方针](https://experienceleague.adobe.com/en/perspectives/planning-and-pivoting-a-strategic-approach-to-peak-season-2025)指南中的建议，该指南使用Adobe Commerce(和可选的Adobe Experience Cloud工具)提供切实可行的战略，帮助您在一年中最繁忙的时间规划、透视和提供卓越的客户体验。

### 最佳实践

* 遵循Adobe的指南[如何为高流量准备基础架构 — 旺季性能的5 Ps](https://business.adobe.com/blog/how-to/the-5-ps-of-peak-season-performance-a-guide-to-preparing-your-infrastructure-for-high-traffic)。
* 查看[Commerce假日准备工作技术提示](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/how-to/tech-tips-for-commerce-holiday-readiness)，了解如何在假日期间为基础设施做好高流量准备、防止停机并优化性能的提示。

+++

## Adobe Experience Manager (AEM)假日准备指南 {#aem}

+++**单击以查看Adobe Experience Manager (AEM)假日准备建议。**

假日季节正迅速临近，对许多Adobe客户而言，这意味着销售高峰期的开始。 我们致力于帮助您取得成功，我们希望确保您为即将到来的流量激增做好充分准备。

### Adobe Experience Manager (AEM)云服务

如果您的组织在假日季节遇到最繁忙的时刻，您可能正在考虑如何优化您的Adobe Experience Manager网站以适应峰值流量。 幸运的是，通过Adobe Experience Manager云服务，您的站点已具备自动扩展的功能，无论流量是否突然变化，都可以确保为访客提供无缝体验。

#### 准备扩展

* 有关使用Adobe Experience Manager云服务为高流量做好准备的详细见解和指南，请参阅以下链接：

   * AEM as a Cloud Service中的[CDN](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/cdn)
   * [AEM as a Cloud Service缓存](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/caching/overview)

* 如果您是Ultimate Success客户，并且最近与您的Adobe客户团队共享了流量预测信息，则无需再次将信息发送给我们，因为我们已经有了一个视图。

我们将在您历程的每个步骤中为您提供支持。 如果您有任何问题或顾虑，请随时[提交支持票证](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/how-to-submit-support-ticket)。

要准备假日季节的营销活动，请查看[AEMaaCS用户指南：简介 — 营销活动参数](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/content-delivery/caching#marketing-parameters)文档。

#### 安全和治理

有关AEM网站流量安全/保护的信息，请参阅AEM as a Cloud Service教程中的[概述 — 保护AEM网站](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/cloud-service/security/traffic-filter-and-waf-rules/overview)一文。

#### 假日维护计划

Adobe设有预定的维护排除期，以确保在关键假日时段内服务不会中断：

* **在下列时间之间不会发生自动更新**：
   * 2025年11月24日至2025年12月2日
   * 2025年12月15日至2026年1月2日

这可以确保高流量期间的稳定性。 有关完整的发行计划和维护时段，请参阅[AEM发行路线图](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/update-releases-roadmap)。


### Adobe Experience Manager (AEM)与Adobe Managed Services (AMS)

利用Adobe Managed Services的AEM客户可以主动与其CSE合作，规划假日的复盖需求。

++++

## Adobe Marketo假日准备指南 {#marketo}

+++**单击查看Adobe Marketo假日准备情况建议。**

为确保利用Adobe Marketo成功开展假日营销活动，各团队应验证电子邮件身份验证设置，清理并保护其数据库，优化营销活动逻辑和时间安排，彻底测试电子邮件渲染和可投放性，并简化为达到最高绩效和参与度而进行的支持准备工作。

### 准备扩展

* 检查您的SPF/DKIM设置，确保一切仍处于设置状态并正常工作。 有关详细信息，请参阅[为您的电子邮件可投放性设置SPF和DKIM](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/deliverability/set-up-spf-and-dkim-for-your-email-deliverability)。
* 通过清除不活动/无效记录来审核并清理Marketo数据库。 这将增加将土地送入您最畅销的潜在客户的收件箱中的机会。 有关详细信息，请参阅[Marketo数据库运行状况检查以及如何保持其干净](https://nation.marketo.com/t5/champion-program-blogs/marketo-database-health-check-up-amp-how-to-keep-it-clean/ba-p/323563)文章。
* 确认您的团队成员具有执行任务的正确权限，并防止对电子邮件的意外访问或更改。 无论您是通过&#x200B;**[!UICONTROL 管理员]**&#x200B;还是通过&#x200B;**[!UICONTROL Admin Console]**&#x200B;进行更改，我们都能为您提供相应的服务。 请参阅[管理用户角色和权限](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/users-and-roles/managing-user-roles-and-permissions)文章。
* 请检查您的Launchpad集成，以确保正确的身份验证，并在使用之前解决任何潜在错误。 请参阅[Marketo Developer Guide： Authentication](https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/rest/authentication)文章。

### 最佳实践

提高效率首先要了解Marketo如何确定促销活动的优先级和处理促销活动。 通过这些优化提示，为您的营销活动提供超快的速度。

* 了解Marketo如何划分促销活动流程步骤处理的优先级，对于避免无意中延迟任何紧急或高优先级电子邮件至关重要。 请参阅[Campaign处理的工作方式](https://nation.marketo.com/t5/knowledgebase/how-campaign-processing-works/ta-p/248264)文章。
* 留意智能列表逻辑有助于确保您的营销活动快速以最佳性能执行。 请参阅[智能列表的最佳实践](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/creating-a-smart-list/best-practices-for-smart-lists)文章。
* **[!UICONTROL 开始时间]**&#x200B;或&#x200B;**[!UICONTROL 收件人时区]**&#x200B;可以在发送之前开始构建电子邮件，从而减少延迟，并为具有高资源逻辑的潜在客户提供更多的准备时间。 有关详细信息，请参阅[电子邮件计划快速入门](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/head-start-for-email-programs)和[使用收件人时区计划电子邮件计划](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-programs/email-program-actions/scheduling-with-recipient-time-zone/schedule-email-programs-with-recipient-time-zone)文章。
* 您的营销活动处于活动状态，潜在客户正在流动，然后您注意到流程步骤存在错误。 我们很容易通过快速调整来进行修复，但如果您意识到在更改实时等待步骤或重新排序流量时会发生什么情况，则可以帮助您避免许多头疼并在以后进行清理。 请参阅[在等待步骤](https://nation.marketo.com/t5/knowledgebase/editing-campaign-flow-with-members-in-wait-steps/ta-p/254294)中与成员一起编辑营销活动流程一文。

### 测试和验证

在点击&#x200B;**[!UICONTROL 发送]**&#x200B;之前，请确保您的电子邮件的外观和性能与预期完全一致。

* Marketo提供了多种方法来测试电子邮件的外观，以确保其外观与您的预期完全相同。
   * 使用&#x200B;**[!UICONTROL 预览]**&#x200B;函数通过按区段或单个潜在客户进行预览来确保您的动态内容和令牌正确呈现。 请参阅[预览包含动态内容的电子邮件](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/general/functions-in-the-editor/preview-an-email-with-dynamic-content)文章。
   * 快速轻松地向测试记录发送直接电子邮件，以了解您的电子邮件在不同客户端/设备上的显示方式。 请参阅[从智能列表中运行单流程步骤](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/using-smart-lists/run-a-single-flow-step-from-a-smart-list)一文。
   * 对于[!DNL Litmus]用户，现在可以比以往更轻松地集成您的帐户并直接从电子邮件编辑器启动渲染测试。 查看包含[&#x200B; [!DNL Litmus]的](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/test-email-rendering)测试电子邮件渲染文章。
* 查看电子邮件垃圾邮件报告功能，该功能与[!DNL SpamAssassin]集成以审查您的电子邮件的内容，并为其分配一个分数，以表示其到达收件箱或标记为&#x200B;*垃圾邮件的可能性*。 请参阅[电子邮件垃圾邮件报告](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/spam-report)文章。
* 请密切关注[!UICONTROL 营销活动队列]，以验证您的营销活动是否正在处理并正确优先处理紧急项目。 查看[我的营销活动是否正在运行？](https://nation.marketo.com/t5/knowledgebase/is-my-campaign-running/ta-p/248662)篇文章。

### 简化您的支持体验

如果出现错误，速度至关重要，Marketo支持将为您提供帮助！ 请在您的支持案例中加入这些详细信息，以避免来回切换，并帮助我们的团队努力更快地解决问题。 请参阅[使用Marketo支持的最佳实践](https://nation.marketo.com/t5/knowledgebase/best-practices-for-working-with-marketo-support/ta-p/253491)文章。

有了本指南，您可以更轻松地了解自己是从一个强有力的位置开始在这个关键窗口推动参与和转化。 风险很高，但你的压力并不一定非得如此。 今天就开始准备工作，让这个假日季节成为您迄今最成功的季节。

+++

## Adobe Workfront假日准备指南 {#workfront}

+++**单击查看Adobe Workfront假日准备情况建议。**

为了准备Adobe Workfront应对假日季，团队应更新支持联系人，将内部计划与Adobe保持一致，避免在峰值时段发生重大更改，并主动监控自动化和集成以确保顺利运行。

### 准备扩展

为帮助确保在假日期间获得流畅的支持体验：

* 提前查看并更新您的授权支持联系人。
* 验证在出现关键问题时，关键利益相关者是否可与支持团队协作。
* 如果计划产品或工作流在假日窗口期间发生更改，请考虑在11月中旬或1月初之前安排时间，以获得最佳的周转时间。
* 将内部假日计划传达给您的Adobe联系人，以确保一致性。

### 测试和验证

随时了解Workfront版本并在沙盒环境中测试新功能：

* [准备Adobe Workfront版本](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-readiness)
* [Workfront发行说明存档](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/product-announcements/product-releases/product-releases)
* [2025年第1季度发行版概述](https://experienceleague.adobe.com/en/docs/workfront/using/product-announcements/product-releases/release-25-q1/25-q1-release-overview)
* [Workfront发布网络研讨会录像](https://experienceleague.adobe.com/en/docs/events/workfront-recordings/releases/25-1-release-webinar)

### 最佳实践

* 前瞻性规划：识别任何可能受内部休息时间计划影响的系统依赖项或计划的自动化。
* 持续沟通：让您的内部团队和Adobe支持人员了解计划内维护或关键事件。
* 使用功能板：监控关键集成和自动化，以发现性能问题的早期迹象。
* 提前上报：如果您预计或发现服务降级，请立即打开支持工单 — 不要等待它变得严重。

通过提前规划、保持清晰的沟通并及早上报问题，企业可以最大限度地减少中断，并确保Workfront在整个假日期间继续支持关键工作流程。

+++

## Adobe Campaign假日准备指南 {#campaign}

+++**单击查看Adobe Campaign假日准备情况建议。**


为了准备Adobe Campaign以进行假日准备，团队应主动验证可投放性设置、优化受众分段和消息频率、确保基础架构可扩展性并测试跨渠道活动编排以有效处理季节性流量和参与度峰值。

### 专家提示让您的假日营销活动引人注目

就像假日购物越早开始越好一样，计划火爆的假日营销活动也是越早开始越好。借助Adobe Campaign，您可以设计、规划和执行营销活动，使贵组织的所有假日愿望都成真。 但是您知道让举行的营销活动圆满结束的小贴士吗？ 观看此视频，[专家提示让您的假日营销活动脱颖而出](https://experienceleague.adobe.com/en/docs/events/experience-league-live-recordings/episodes/exl-live-episode-03)，其中讨论了可投放性和执行最佳实践，并将向您展示如何在Adobe Campaign中完成所有这些工作。

### 假期时的注意事项和准备工作

此视频[Adobe Campaign：假日准备工作 — 假日期间的注意事项和准备工作](https://helpx.adobe.com/customer-care-office-hours/campaign/campaign-holiday-readiness.html)涵盖：

* 参与Campaign社区
* 可交付性 — 节假日及以后的注意事项！
* Adobe Campaign Classic (ACC)和Adobe Campaign Standard (ACS)的技术建议

要让Adobe Campaign为假期旺季做好准备，组织应该完成可投放性检查、验证活动配置，并确保可扩展的基础架构和跨渠道编排到位，从而在整个假期中放心地执行大容量、时效性强的活动。

+++

## Adobe Analytics假日准备指南 {#analytics}

+++**单击查看Adobe Analytics假日准备情况建议。**

随着假日季节的临近，使用Adobe Analytics的组织应当采取主动步骤，确保在流量高峰期间的数据准确性、平台性能和报表可靠性。 Adobe提供了多种资源和最佳实践，以帮助团队有效准备。

### 预测流量

为确保足够的硬件分配和系统响应能力，Adobe建议提前&#x200B;**提交每小时峰值和每日服务器点击/调用量**。

* 检查[流量尖峰计划和硬件分配提前期](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/traffic-management/t-traffic-schedule-spike#hardware-allocation-lead-times)，因为了解数据可用速度对于大流量期间的实时决策至关重要。

* 在[Adobe Analytics数据延迟概述](https://experienceleague.adobe.com/en/docs/analytics/technotes/latency)中了解Adobe Analytics中的数据可用性和延迟有何影响，包括意外的流量尖峰和硬件问题，并探索减少数据延迟的建议策略。

### 最佳实践

对于使用数据馈送导出原始Analytics数据的团队，Adobe提供了有关优化馈送配置和避免常见隐患的指导。

* [Adobe Analytics数据馈送的最佳实践](https://experienceleague.adobe.com/en/docs/analytics/export/analytics-data-feed/data-feeds-best-practices)

为了在节假日保持快速可靠的报表，Adobe建议：

* [优化Analysis Workspace性能](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/workspace-faq/optimizing-performance)
* [Report Builder疑难解答和最佳实践：优化请求的建议](https://experienceleague.adobe.com/en/docs/analytics/analyze/legacy-report-builder/troubleshoot#section_33EF919255BF46CD97105D8ACB43573F)
* [Analytics组件指南：计划报表队列](https://experienceleague.adobe.com/en/docs/analytics/components/scheduled-reports-admin)

### 假日维护计划

Adobe通常在假日高峰期执行&#x200B;**排除维护时段**&#x200B;以确保服务不中断。 客户应通过Experience League监控Adobe的发布和维护计划，并与其Adobe客户团队协调支持计划。

通过遵循这些准则并利用Adobe的公共文档，组织可以确保其Adobe Analytics实施稳健、响应迅速并满足假日季节的需求。

+++

## Adobe Target假日准备指南 {#target}

+++**单击查看Adobe Target假日准备情况建议。**

假日季节提供了令人振奋的参与机会，但也带来了流量激增和个性化系统需求增加等挑战。 为了帮助您在这个关键时期提供无缝体验，我们编译了关键建议，以确保您的Adobe Target实施准备就绪。

### 预测需求

首先，预计流量会达到20-50%或更高，并验证您的基础架构能否处理负载。 预测Adobe Target、Analytics和AEP中的活动和数据量，以避免出现意外情况。

确定任务关键型历程（如结账、产品推荐和促销优惠）也很重要，因此个性化工作将重点放在最重要的地方。

请参阅[使用Adobe Target进行优化的最佳实践](https://experienceleague.adobe.com/en/docs/target-learn/tutorials/administration/strategy/target-best-practices-for-optimization)。

### 准备扩展

* 规划增加网站和移动设备上的流量，并通知Target支持团队增加服务器容量以避免任何被阻止的调用。
* 对于任何加载/笔测试，应提前通知Target支持团队。
* 升级到最新的`at.js`/交付API版本。
* 冻结非关键性更改；准备后备体验。
* 协调支持和上报流程，并启用主动警报。

### 测试和验证

使用[QA链接](https://experienceleague.adobe.com/en/docs/target/using/activities/activity-qa/activity-qa)验证内容投放，以确认一切都按预期运行。 使用&#x200B;**[!UICONTROL 匹配受众规则查看体验]**&#x200B;切换以确保正确的受众符合您正在测试的活动。 仔细检查您的&#x200B;**[!UICONTROL 目标量度]**&#x200B;配置是否与活动的&#x200B;**[!UICONTROL 目标]**&#x200B;一致。 而且随时准备备份计划 — 以防万一。

### 最佳实践

将您的实施保留在[Adobe Target限制](https://experienceleague.adobe.com/en/docs/target/using/troubleshoot/target-limits)之内，并在启动之前预先验证[GDPR和CCPA合规性](https://experienceleague.adobe.com/en/docs/target-dev/developer/implementation/privacy/cmp-privacy-and-general-data-protection-regulation)。 维护少于100个的活动并存档旧的活动以保持简化。 利用&#x200B;**[!UICONTROL 自动分配]**/**[!UICONTROL 自动定位]**&#x200B;进行AI驱动的优化。 建立回滚计划和实时监控仪表板。

### 安全和治理

在个性化体验之前，请确认GDPR和CCPA下的同意合规性。 避免在配置文件参数中存储个人身份信息(PII)，并验证API安全性以保护客户数据。

+++
