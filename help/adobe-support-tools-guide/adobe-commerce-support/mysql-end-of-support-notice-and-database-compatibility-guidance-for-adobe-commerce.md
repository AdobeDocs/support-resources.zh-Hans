---
title: Adobe Commerce的MySQL支持终止通知和数据库兼容性指南
description: 本文提供了有关支持的Adobe Commerce版本的MySQL支持终止时间表和数据库兼容性指导的信息。
solution: Commerce
exl-id: f4ef2b3b-316c-421e-a645-9445cdd13448
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
source-git-commit: a4ba265c36bd4ba6c7c563879834f2c59fdc58a4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%
---
# Adobe Commerce的MySQL支持终止通知和数据库兼容性指南

本文提供了有关支持的Adobe Commerce版本的MySQL终止支持(EOS)和数据库兼容性的重要信息。
Adobe强烈建议商家查看此公告并采取措施来维护平台稳定性并保持遵守支持要求。
在[MariaDB升级先决条件](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/implementation-playbook/best-practices/maintenance/mariadb-upgrade)和[系统要求](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/installation-guide/system-requirements)中了解更多信息。

## MySQL 8.0终止支持(EOS)

MySQL 8.0于2026年4月30日到达支持终止点(EOS)。
在此日期之后，以下Adobe Commerce版本将不支持或保持与MySQL 8.0之后发布的MySQL版本的兼容性：

* Adobe Commerce 2.4.7
* Adobe Commerce 2.4.6
* Adobe Commerce 2.4.5

Adobe将不会验证或支持这些Adobe Commerce发行版上的较新MySQL主要版本。

## 内部部署客户的必需操作

强烈建议运行以下版本的Adobe Commerce本地安装将其数据库服务器迁移到兼容的MariaDB版本：

* 2.4.5
* 2.4.6
* 2.4.7

这些版本完全支持MariaDB，并且是推荐的数据库平台。

* 2.4.5
* 2.4.6
* 2.4.7

强烈建议将其数据库服务器迁移到兼容的MariaDB版本。
这些Adobe Commerce版本完全支持MariaDB，它是推荐的数据库平台。

## Adobe Commerce 2.4.8和2.4.9中的MySQL支持

Adobe Commerce 2.4.8和2.4.9是支持MySQL的最新Adobe Commerce版本。

对于这些版本：
* MySQL 8.4是Adobe Commerce支持的最终MySQL版本。
* Adobe Commerce中不会认证或支持任何在8.4之后发布的MySQL版本。

## 未来方向：将MariaDB作为默认数据库平台

今后，Adobe Commerce继续支持将MariaDB作为默认和推荐的数据库平台。

Adobe强烈建议以下客户开始规划其向MariaDB的迁移，以保持长期的兼容性并支持协调一致：
* 所有Adobe Commerce 2.4.8和2.4.9内部部署客户
* 运行早期支持的Adobe Commerce版本的客户
