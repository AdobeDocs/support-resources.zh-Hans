---
title: 运行就绪
description: 运营就绪性建议，帮助Adobe Commerce商家为高流量事件（如假日季节）准备环境。
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
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bcd8874c-7b93-5596-bdaa-22660e84df14
    internal-label: Deploy
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 938d2364-5176-55ec-80f1-9415253e5e51
    internal-label: Site Management
  - id: b48dbafb-4193-5648-b9d9-bf96e9c9a411
    internal-label: Backend Development
  - id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
    internal-label: Admin tools and workspace
subfeature_v2:
  - id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
    internal-label: Admin workspace
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: c89c0345d0e483463ab44195c2d5c0cb18d1d4c5
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%
---

# 运行就绪

此部分提供有关准备Adobe Commerce环境（包括云基础架构上的Commerce和内部部署）的技术建议，以便开展假期之类的高流量活动。

## 应用所有安全和性能修补程序 {#apply-all-security-and-performance-patches}

在代码冻结前完成所有更新以防止部署中断。

## 运行假日前运行状况检查 {#run-pre-holiday-health-checks}

测试备份、 cron运行状况和缓存预热脚本，以确保在负载下顺利运行。

## 制定监控行动手册 {#establish-monitoring-playbooks}

记录警报阈值、上报步骤和联系点，以便在高峰期全天候响应。

## 记录回退计划 {#document-rollback-plans}

维护版本化的回滚策略，以便从部署异常中快速恢复。

