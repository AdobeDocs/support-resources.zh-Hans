---
title: 如何获取和应用[!UICONTROL 安全修补程序]
description: 本文提供了有关如何获取和应用已发布的[!UICONTROL 安全修补程序]的说明，但相关说明不可用。
exl-id: 6764d60e-5088-4a85-90fa-4372570b065b
source-git-commit: 9a4d96e06b949e4c229fdf0f084810b27bf8b346
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 0%

---

# 如何获取和应用[!UICONTROL 安全修补程序]

>[!NOTE]
>如果您使用的是内部部署安装，并且没有使用[!DNL CVS]或GitHub等版本控制系统来管理代码，则Web主机可能能够协助应用修补程序。 欢迎您随时联系他们寻求支持。

本文提供了有关如何获取和应用已发布的[!UICONTROL 安全修补程序]的说明，但相关说明不可用。

## 受影响的产品和版本

Adobe Commerce内部部署和云基础架构 — 所有受支持的版本


## 原因

对于Adobe Commerce安全公告，仅当作为公告的一部分明确发布工件时，Adobe才提供单独的独立修补程序文件或修补程序。 如果公告资料中未发布或引用任何独立的修补程序或修补程序，则Adobe之后不会创建单独的独立修补程序。

这是因为安全修补程序是作为适用版本行的受支持安全版本的一部分进行工程、验证和发布在一起的。

因此，支持的修正路径是为受影响的版本行应用官方安全更新，或升级到已包含该修复的版本。

## 解决方案


### 案例一：

* 如果[发行说明](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite)中提到独立的修补程序文件/修补程序，请从[https://account.magento.com](https://account.magento.com/downloads/view/)的下载部分下载该文件。 共享访问用户必须首先由帐户所有者/许可证持有人授予下载权限。

**注意事项：**

* 在2027年8月30日之前，Adobe Commerce 2.4.6在扩展支持下仍受支持。

* Adobe Commerce 2.4.5在2026年8月11日之前仍受延长支持。 在此日期之后，Adobe仅提供到2027年5月31日的安全修复。

* Adobe Commerce 2.4.4不再受扩展支持。 Adobe仅提供了到2027年5月31日的安全修复。

* 对于Adobe Commerce 2.4.4和2.4.5，Adobe仅提供安全修补程序文件。 这些更新不包括：

   * Adobe Commerce支持或工程协助
   * 高品质的修补程序
   * 平台或操作系统依赖关系更新

不受支持的版本（2.3.x和2.4.0-2.4.3）没有资格获得支持。 您可以升级到支持的版本以接收最新的安全修复。

### 案例二：

隔离修补程序仅在异常情况下提供，不是实现安全修补程序的首选方法。

如果发行说明中未提及独立的修补程序文件或修补程序，请遵循以下准则：

>[!IMPORTANT]
>
>如果没有针对安全问题明确发布独立的修补程序文件或修补程序，请将完整的Adobe Commerce应用程序升级到受影响版本行的最新适用修补程序版本。

**云：**

1. 某些[!UICONTROL 安全修补程序]可能包含在最新版本的Cloud Tools Suite (ECE Tools)中，发布在Commerce的Cloud Patches下 — 请查看[发行说明](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)，如果发行版中提到安全修补程序，请将包升级到该版本。
1. 如果发行说明未提及安全修复，请继续阅读。

**云基础架构或内部部署：**

* 如果隔离的修补程序文件/修补程序不可用，请[将云基础架构上的Adobe Commerce版本](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X升级到最新的修补程序版本2.4.X-pY。
* 如果隔离的修补程序文件/修补程序不可用，请[将Adobe Commerce版本On-Premise](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X升级到最新的修补程序版本2.4.X-pY。

## 相关阅读

* 请参阅《Commerce Cloud基础架构上的Adobe Commerce指南》*中的[Cloud Tools Suite](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)发行说明*。
* 请参阅&#x200B;*Adobe Commerce Infrastructure指南*&#x200B;中的[升级Adobe Commerce版本](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version)。
