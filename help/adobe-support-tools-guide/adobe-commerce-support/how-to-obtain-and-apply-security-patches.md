---
title: 如何获取和应用[!UICONTROL 安全修补程序]
description: 本文提供了有关如何获取和应用已发布的[!UICONTROL 安全修补程序]的说明，但相关说明不可用。
source-git-commit: 93ee9bd110930e244befca682fadd3edc24d138a
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# 如何获取和应用[!UICONTROL 安全修补程序]

>[!NOTE]
>如果您使用的是内部部署安装，并且没有使用[!DNL CVS]或GitHub等版本控制系统来管理代码，则Web主机可能能够协助应用修补程序。 欢迎您随时联系他们寻求支持。

本文提供了有关如何获取和应用已发布的[!UICONTROL 安全修补程序]的说明，但相关说明不可用。

## 受影响的产品和版本

Adobe Commerce内部部署和云基础架构 — 所有受支持的版本


## 原因

发布的大多数[!UICONTROL 安全修补程序]没有应用任何隔离的修补程序或修补程序，因此需要升级到[!UICONTROL 安全修补程序]版本。

## 解决方案


### 案例一：

* 如果[发行说明](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/release-notes/cloud-tools-suite)中提到独立的修补程序文件/修补程序，请从[https://account.magento.com](https://account.magento.com/downloads/view/)的下载部分下载该文件。 共享访问用户必须首先由帐户所有者/许可证持有人授予下载权限。

**注意事项：**

如果您使用的是较低版本的Adobe Commerce (2.4.4)，则您将自动获得扩展支持。 您的版本必须是下列不支持的版本之一，才能应用最新的可用安全修补程序：

2.4.4 - 2.4.4-p11

不受支持的版本(2.3.x、2.4.0 - 2.4.3)没有资格获得支持，您必须首先升级到受支持的版本才能利用最新的安全修复。

如果您没有扩展支持，可以请求支持人员与您共享修补程序，但是他们将无法解决您在应用修补程序时可能遇到的任何问题/错误。

### 案例二：

仅在特殊情况下才提供隔离的修补程序，它不是实施安全修补程序的首选形式。

如果发行说明中未提及独立的修补程序文件/修补程序，请执行以下操作：

* **云：**

1. 某些[!UICONTROL 安全修补程序]可能包含在最新版本的Cloud Tools Suite (ECE Tools)中，发布在Commerce的Cloud Patches下 — 请查看[发行说明](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)，如果发行版中提到安全修补程序，请将包升级到该版本。
1. 如果发行说明未提及安全修复，请继续阅读。

* **云基础架构或内部部署：**

* 如果隔离的修补程序文件/修补程序不可用，请[将云基础架构上的Adobe Commerce版本](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version) 2.4.X升级到最新的修补程序版本2.4.X-pY。
* 如果隔离的修补程序文件/修补程序不可用，请[将Adobe Commerce版本On-Premise](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade) 2.4.X升级到最新的修补程序版本2.4.X-pY。

## 相关阅读

* 请参阅《Commerce Cloud基础架构上的Adobe Commerce指南》[中的](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/release-notes/cloud-tools-suite)Cloud Tools Suite *发行说明*。
* 请参阅[Adobe Commerce Infrastructure指南](https://experienceleague.adobe.com/zh-hans/docs/commerce-cloud-service/user-guide/develop/upgrade/commerce-version)中的&#x200B;*升级Adobe Commerce版本*。
