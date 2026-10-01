---
title: 性能优化
description: 性能优化建议，帮助Adobe Commerce商家准备环境以进行高流量活动，例如假日季节。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
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
source-git-commit: b2220ea4cb5a301cbee6cea5fb90d6dc8a05eeff
workflow-type: tm+mt
source-wordcount: '1698'
ht-degree: 0%
---

# 性能优化

此部分提供有关准备Adobe Commerce环境（包括云基础架构上的Commerce和内部部署）的技术建议，以便开展假期之类的高流量活动。

>[!NOTE]
>
>标记为&#x200B;**（仅限Cloud）**&#x200B;的步骤适用于云基础架构上的Commerce。 大多数其他建议也适用于内部部署。

## 优化Fastly请求缓存（仅限云） {#optimize-fastly-request-caching}

[!DNL Fastly]在边缘处缓存响应以减少原始服务器上的负载。 在旺季，一些配置检查可帮助您充分利用该缓存，尤其是在使用跟踪参数或Headless店面运行促销活动时。 有关完整配置引用，请参阅[自定义缓存配置](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration)。

* 标准化跟踪参数：在假日季节期间，您可能会运行社交和付费营销活动（例如Google Ads、Facebook和X），这些营销活动会为每个URL附加唯一的跟踪字符串。 每个唯一字符串会为原本属于同一页面的内容创建一个单独的缓存条目，从而降低缓存命中率。 将这些参数添加到Adobe Commerce管理员的[!DNL Fastly]配置中的&#x200B;**[!UICONTROL 忽略的URL参数]**&#x200B;列表中，以便[!DNL Fastly]将它们视为等效参数。
* 确认您的登陆页面可缓存：检查每个促销登陆页面上的`x-cache`响应标头。 可缓存的页面在后续加载时返回`HIT`或`HIT`/`MISS`对。 如果标头返回`MISS, MISS`，则表示该页面未缓存，需要调查。
* 对GraphQL查询使用GET请求：如果您运行PWA或headless店面，请将GraphQL查询作为`GET`请求发送，查询包含在URL中，而不是作为`POST`请求发送。 [!DNL Fastly]只缓存`GET`个请求，查询是URL的一部分。 在正文中发送查询的`GET`请求未缓存。

>[!NOTE]
>
>[!DNL Fastly]源屏蔽也会影响缓存性能。 有关配置详细信息，请参阅[快速原点屏蔽](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding)。

## 启用Fastly IO（仅限云） {#enable-fastly-io}

[!DNL Fastly] IO将图像大小调整和格式转换卸载到[!DNL Fastly]边缘网络，而不是Adobe Commerce源网络。 这减少了服务器负载并提高了图像密集型店面的页面渲染速度，这是高流量销售期间常见的瓶颈。 有关配置选项，请参阅[快速图像优化](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/cdn/fastly-image-optimization)。

在开始之前，请确认已配置原点屏蔽。[!DNL Fastly] IO要求源屏蔽作为先决条件。 有关配置详细信息，请参阅[快速原点屏蔽](/help/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-holiday-readiness-overview/scalability-capacity-planning.md#fastly-origin-shielding)。

要启用[!DNL Fastly] IO，请执行以下操作：

1. 在Admin中，转到&#x200B;**[!UICONTROL Fastly配置]**&#x200B;页面并选择&#x200B;**[!UICONTROL 默认IO配置选项]**&#x200B;旁边的&#x200B;**[!UICONTROL 配置]**。
1. 确认已启用[!DNL Fastly] IO代码片段。
1. 在&#x200B;**[!UICONTROL 图像优化]**&#x200B;配置中，将&#x200B;**[!UICONTROL 启用深层图像优化]**&#x200B;设置为&#x200B;*[!UICONTROL 是]*。 此设置禁用Adobe Commerce的内置图像大小调整功能，并将任务转移到[!DNL Fastly]。
1. 确认防护板位置设置正确。 有关配置详细信息，请参阅[快速原点屏蔽](#fastly-origin-shielding)。

>[!NOTE]
>
>深度图像优化仅调整产品图像的大小。 CMS图像（如横幅和内容块）不会受到影响，并继续使用Adobe Commerce的内置调整大小。

要验证[!DNL Fastly] IO是否正常工作，请检查产品图像请求上的响应标头：

* `x-cache`标头返回`HIT`。
* 已填充`fastly-io-info`和`fastly-stats`标头。
* 图像URL在路径中不包含`/cache/`目录。

## 实施Redis二级缓存 {#implement-redis-l2-cache}

实施有效的缓存做法，以便在流量高峰期可靠地执行存储。[!DNL Redis] L2缓存通过将缓存数据存储在每个Web节点的本地来将网络带宽减少到[!DNL Redis]。 有关二级缓存工作方式的背景，请参阅[二级缓存](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/configuration-guide/cache/level-two-cache)。

在云基础架构上的Commerce上，通过设置`REDIS_BACKEND`部署变量来启用此功能。 有关配置步骤，请参阅Commerce on Cloud Infrastructure指南中的[REDIS_BACKEND](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_backend)。 内部部署，直接在`app/etc/env.php`中进行配置。

>[!NOTE]
>
>不支持将[!DNL Redis]作为Adobe Commerce 2.4.9或更高版本上的二级缓存后端，也不支持将其用于高于2.4.5-p16、2.4.6-p14、2.4.7-p9或2.4.8-p4的修补程序版本。 在这些版本上，请改用`VALKEY_BACKEND`。

## 启用MySQL和Redis从属连接（仅限云） {#enable-mysql-and-redis-slave-connections}

[!DNL Redis]和[!DNL MySQL]从属连接将读取流量卸载到副本节点，从而减少高流量期间主连接上的负载。 有关配置步骤，请参阅[MYSQL_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#mysql_use_slave_connection)和[REDIS_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#redis_use_slave_connection)或[VALKEY_USE_SLAVE_CONNECTION](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/configure/env/stage/variables-deploy#valkey_use_slave_connection)，具体取决于您的Adobe Commerce版本。

### Redis从属连接

[!DNL Redis]从属连接是到[!DNL Redis]实例的只读连接，允许从非主节点提供读取流量。 如果未启用，则[!DNL MySQL]可能会遇到高负载瓶颈。 查看[!DNL New Relic]的APM概述图表以了解上升的响应时间作为早期符号，然后通过按最耗时的事务排序在&#x200B;**[!UICONTROL 数据库]**&#x200B;选项卡中确认，以识别缓慢的[!DNL MySQL] `SELECT`查询。 通过将部署变量`REDIS_USE_SLAVE_CONNECTION`设置为`true`来启用此功能。

>[!NOTE]
>
>`REDIS_USE_SLAVE_CONNECTION`仅在Staging和Production Pro群集环境中受支持。 入门级或缩放（拆分）架构项目不支持此功能。 在Scaled架构上启用它会导致[!DNL Redis]连接错误 — 请在该架构上使用[!DNL Redis] L2缓存。 请参阅上面的[实施Redis L2缓存](#implement-redis-l2-cache-implement-redis-l2-cache)。

### MySQL从属连接

在Pro群集环境中启用`MYSQL_USE_SLAVE_CONNECTION`标志以将特定的只读数据库查询定向到从属连接，从主连接卸载查询执行。

>[!CAUTION]
>
>在生产环境中启用任一设置之前进行负载测试。 在负载正常的环境中，从连接可能会使性能降低10%到15%。 在负载较重、持续较重的环境中，它们可以显着提高性能。 在启用之前评估预期的高峰季节流量。

## 启用异步订单和电子邮件处理 {#enable-asynchronous-order-and-email-processing}

使用异步处理在后台对大量订单相关操作进行排队和执行，从而减少流量高峰期间的前端延迟。 这涵盖了三个相关但不同的设置 — 请参阅[配置最佳实践](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/performance-best-practices/configuration)以查看概述。

* 异步订单下达： “异步订单”模块将订单标记为已接收，并将其放入队列中，然后处理先入先出的订单。 默认情况下处于禁用状态。 从命令行启用它：

  ```
  bin/magento setup:config:set --checkout-async 1
  ```

  启用后，无法立即获得订单详细信息 — 订单将保持排队状态，直到`placeOrderProcess`消费者根据库存验证订单（默认启用）并进行更新。 在禁用此模块之前，请验证所有正在进行的异步订单都已完成处理。 有关详细信息，请参阅[签出性能最佳实践](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/performance-best-practices/high-throughput-order-processing)。

* 异步订单数据处理：密集的店面销售和密集的订单处理可能在数据库级别发生冲突。 启用此设置将区分这两种流量模式，因此订单会被放在临时存储中，并在没有冲突的情况下批量移动到Order Management网格。 此计划通过cron更新“订单”、“发票”、“发运”和“贷项通知单”网格，从而避免锁定并减少处理时间。 为了获得最佳结果，请将cron配置为每分钟运行一次。

  >[!NOTE]
  > 
  >启用方式取决于您的部署模式。 默认情况下，云基础架构上的Adobe Commerce暂存和生产环境以生产模式运行，此设置不可通过管理员使用。 在生产模式下，请改为运行`bin/magento config:set dev/grid/async_indexing 1`。 在默认模式下，转到&#x200B;**[!UICONTROL 存储]** > **[!UICONTROL 配置]** > **[!UICONTROL 高级]** > **[!UICONTROL 开发人员]** > **[!UICONTROL 网格设置]**，并将&#x200B;**[!UICONTROL 异步索引]**&#x200B;设置为&#x200B;*[!UICONTROL 启用]*。

  有关详细信息，请参阅[计划订单工序](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/stores-sales/order-management/orders/order-scheduled-operations)。

* 异步电子邮件通知：此设置将结账和订单处理电子邮件通知移至后台。 在&#x200B;**[!UICONTROL 商店]** > **[!UICONTROL 配置]** > **[!UICONTROL 销售]** > **[!UICONTROL 销售电子邮件]** > **[!UICONTROL 常规设置]** > **[!UICONTROL 异步发送]**&#x200B;处启用它。

## 配置索引器以按计划更新 {#configure-indexers-for-update-on-schedule}

将索引器设置为在计划模式下运行，以避免数据库锁定并提高频繁更新目录时的响应性。 有关详细信息，请参阅[索引器配置的最佳实践](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/implementation-playbook/best-practices/maintenance/indexer-configuration)。

索引器可以在&#x200B;**[!UICONTROL Update on Save]**&#x200B;或&#x200B;**[!UICONTROL Update on Schedule]**&#x200B;模式下运行。

* 每当目录或其他数据发生更改时，**[!UICONTROL 保存时立即更新]**&#x200B;索引。 它假定更新和浏览强度较低，并在高负载下可能会导致严重延迟和数据不可用。
* 建议对生产执行计划&#x200B;**[!UICONTROL 更新]**。 它通过专用的cron作业在后台存储有关数据更新和重新索引的信息。

在&#x200B;**[!UICONTROL 系统]** > **[!UICONTROL 工具]** > **[!UICONTROL 索引管理]**&#x200B;处单独设置每个索引器的更新模式。

>[!IMPORTANT]
>
>`customer_grid`索引器支持的模式取决于您的Adobe Commerce版本。 在低于2.4.8的版本上，客户网格仅支持&#x200B;**[!UICONTROL 保存时更新]**，不要将其设置为&#x200B;**[!UICONTROL 计划更新]**。 在Adobe Commerce 2.4.8及更高版本上，客户网格支持这两种模式，现在默认为&#x200B;**[!UICONTROL 按计划更新]**。

## 禁用并评估目录平面表 {#disable-and-evaluate-catalog-flat-table}

不建议将平面表用于产品和类别。 此已弃用的功能可能会导致性能下降和索引问题。 有关详细信息，请参阅[平面目录](https://experienceleague.adobe.com/zh-hans/docs/commerce-admin/catalog/catalog/catalog-flat)。

要禁用平面目录，请转到&#x200B;**[!UICONTROL 商店]** > **[!UICONTROL 配置]** > **[!UICONTROL 目录]** > **[!UICONTROL 目录]** > **[!UICONTROL 店面]**，将&#x200B;**[!UICONTROL 使用平面目录类别]**&#x200B;设置为&#x200B;*[!UICONTROL 否]*，将&#x200B;**[!UICONTROL 使用平面目录产品]**&#x200B;设置为&#x200B;*[!UICONTROL 否]*，然后单击&#x200B;**[!UICONTROL 保存配置]**。

某些第三方模块和自定义项确实需要平面表才能正常工作。 在禁用平面表之前，评估继续使用这些扩展的影响和风险。

## 考虑扩展（拆分）架构（仅限云） {#consider-scaled-split-architecture}

如果在应用上述配置和代码级优化后，负载测试或实时基础架构性能仍显示CPU和其他资源已达到极限，请考虑迁移到扩展（拆分）架构。 有关详细信息，请参阅[缩放的体系结构](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/architecture/scaled-architecture)。

>[!NOTE]
>
>扩展体系结构仅适用于具有Pro 48或更高群集的客户。

拆分层架构使用最少六个节点：三个运行[!DNL OpenSearch]或[!DNL Elasticsearch]、[!DNL MariaDB]和[!DNL Redis]或[!DNL Valkey]的服务节点以及三个运行`php-fpm`和`NGINX`的Web节点。

* 通过增加服务器大小（CPU和内存），服务节点只能垂直扩展。 由于数据库群集是为高可用性而构建的，因此服务节点无法以可靠的方式水平扩展。
* Web节点可以纵向和横向扩展，添加Web服务器来处理增加的请求量。

这使您能够在高负载期间按需扩展基础架构，并独立扩展每个层。 要在预期的高负载期间之前切换到分层架构，请联系您的Adobe客户团队。
