---
title: 监控和可观察性
description: 监控和可观察性建议，帮助Adobe Commerce商家准备环境以进行高流量事件，例如假日季节。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: 4239b8a6-e74f-567d-a7a5-b98b9ead0ea4
    internal-label: Observability
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 2%
---

# 监控和可观察性

此部分提供有关监控Adobe Commerce环境的技术建议，以便对高流量事件（如假日季节）做好准备。

>[!NOTE]
>
>标记为&#x200B;**（仅限Cloud）**&#x200B;的步骤适用于云基础架构上的Commerce。 大多数其他建议也适用于内部部署。

## 使用New Relic监控流量（仅限Cloud） {#monitor-traffic-with-new-relic}

云基础架构上的Adobe Commerce包括[!DNL New Relic]可观察平台订阅，该订阅无缝地合并以近乎实时的方式流式传输到[!DNL New Relic]中的[!DNL Fastly]日志。 通过此集成，您可以实时监控流量模式和趋势，以便采取纠正措施。

使用这些日志可以：

* 确定您的Web请求来自的国家/地区。
* 查找抓取您网站的滥用IP地址或用户代理。
* 识别针对特定端点的恶意流量，例如付款。
* 根据客户使用的设备和浏览器类型生成报表。

例如，监控流量的来源国家/地区，以确认它反映了促销活动和客户的地理位置：

```sql
SELECT count(*) FROM Log
WHERE cache_status IS NOT NULL
AND project_id = '<YOUR_PROJECT_ID>'
AND (content_type LIKE 'text/html;%' or url LIKE '%graphql%' or url like '%rest%')
FACET geo_country_code
SINCE 7 days ago until today
```

修改此查询以满足您的需求，进一步细分它，或将其转换为仪表板以便进行集中跟踪。 有关详细信息，请参阅[New Relic日志管理](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management)。

## 自定义New Relic警报（仅限Cloud） {#customize-new-relic-alerts}

除了Adobe Commerce在云基础架构上设置的“托管警报”之外，您还可以在销售旺季为平台设置各种警报和通知，例如，通知您机器人流量或在GraphQL查询中缩短响应时间。 有关内置警报的完整列表，请参阅[Adobe Commerce托管警报](https://experienceleague.adobe.com/en/docs/commerce-operations/tools/managed-alerts-for-adobe-commerce/managed-alerts-for-magento-commerce)。

[!DNL New Relic]警报和AI支持基于NRQL的查询结构。 从&#x200B;**[!UICONTROL 警报和AI]**&#x200B;下的[!DNL New Relic]仪表板设置自定义警报。

## 查看Apdex分数（仅限Cloud） {#review-apdex-score}

Apdex得分用于衡量用户对Web应用程序和服务的响应时间的满意度。 您可以使用[!DNL New Relic]查看Adobe Commerce在云基础架构上的Apdex分数。

Apdex得分从0到1不等。 0分是最差的分数，表示100%的响应时间是&#x200B;**受挫感**。 1分是最佳分数，表示100%的响应时间是&#x200B;**满意**。 [!DNL New Relic]报告反映后端性能的应用程序服务器得分和反映客户端性能的最终用户得分。

Apdex得分为0.5或更低的认股权证调查。 低于0.4的分数会被视为中断。

[!DNL New Relic]与Apdex一起提供了一系列统计数据，用于分析Adobe Commerce在云基础架构上的性能问题。 有关步骤，请参阅[在Adobe Commerce上使用New Relic进行性能故障诊断](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/troubleshoot-performance-using-new-relic-on-magento-commerce)。

## 查看支持见解（SWAT报表） {#review-support-insights-swat-report}

要获取有关您环境的更详细报告，请生成全站点分析工具(SWAT)报告。 有关SWAT工具的更多信息，请参阅[站点范围分析工具](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/tools/site-wide-analysis-tool/intro)。