---
title: 可扩展性和容量规划
description: 可扩展性和容量规划建议，以帮助Adobe Commerce商家为假期之类的高流量事件准备环境。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
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
source-wordcount: '413'
ht-degree: 0%
---

# 可扩展性和容量规划

此部分提供有关缩放Adobe Commerce环境以准备假日季节等高流量事件的技术建议。

>[!NOTE]
>
>标记为&#x200B;**（仅限Cloud）**&#x200B;的步骤适用于云基础架构上的Commerce。 大多数其他建议也适用于内部部署。

## 提前规划群集扩展（仅限云） {#plan-cluster-upsize-early}

对于云基础架构客户上的Commerce而言，临时群集升级可分配更多计算资源来处理高峰季节的流量激增。 提前提交支持工单并提供日期范围和所需的群集大小，并就当前资源消耗和需求与您的专门客户经理进行协调。 请在需要容量之前至少提前48个工作小时提交请求，尤其是对于假日季节，请尽早提交，因为黑色星期五和网络星期一期间的容量有限。 请参阅[如何请求临时扩展](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/how-to-request-temporary-adobe-commerce-on-cloud-infrastructure-upsize)。

例如，如果支持体系结构的客户每日基线为24个内核（24个vCPU、96 GB RAM），将内核（96个vCPU、384 GB RAM）调整为96个，则每天将占用约4倍的资源（96个vCPU、384 GB RAM），即大约增加504个vCPU的消耗(96×7−24×7)。

## Fastly源屏蔽 {#fastly-origin-shielding}

Adobe Commerce [!DNL Fastly]的原始防护旨在减少直接发往Adobe Commerce原始服务器的流量。 收到请求后，[!DNL Fastly]边缘位置(Point of Presence)会检查缓存的内容并将其交付。 如果未缓存，则将继续向Shield POP缓存，以检查是否将其缓存在此处 — 如果先前甚至从其他全局POP请求过内容，则将会缓存该内容。 最后，如果未在Shield POP上缓存它，则它只会继续到源服务器。

可以在Adobe Commerce管理员的[!DNL Fastly]配置后端设置中启用[!DNL Fastly]源屏蔽。 选择最接近Adobe Commerce原始数据中心的屏蔽位置以获得最佳性能。 有关详细信息，请参阅[配置后端和源屏蔽](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/cdn/setup-fastly/fastly-custom-cache-configuration#configure-back-ends-and-origin-shielding)。 默认情况下，[!DNL Fastly]源屏蔽未启用。

## 执行加载和故障转移测试 {#conduct-load-and-failover-tests}

在主要活动之前执行加载和恢复测试，以验证扩展配置和回滚计划。