---
title: 无法将用户添加到Adobe Commerce云项目
description: 本文提供一种解决方案，用于解决您无法将用户添加到Adobe Commerce云项目的问题。
feature: Cloud, Paas
solution: Commerce
feature-set: Commerce
role: Developer
exl-id: 2dc52d5e-0930-48c4-986e-ce3f9f6f8221
source-git-commit: 755c6dc9cff041b9ca9183fbecde21f90fbaee1a
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---

# 无法将用户添加到Adobe Commerce云项目

当您尝试将用户添加到云项目时，本文会为您提供解决方案，但失败并出现错误： *用户XXX不存在*。

## 受影响的产品和版本

* 云基础架构上的Adobe Commerce，[所有支持的版本](https://magento.com/sites/default/files/magento-software-lifecycle-policy.pdf)

## 问题

本文提供一种解决方案，用于解决您无法将用户添加到Adobe Commerce云项目的问题。

## 原因

必须先在[https://accounts.magento.cloud](https://accounts.magento.cloud)创建用户帐户并将其链接到其Adobe SSO，然后才能将其添加为项目的用户。 如果用户具有Adobe帐户但不具有Commerce (magento.com)帐户，则必须首先创建一个。

## 解决方案

1. 要求用户在[https://accounts.magento.cloud](https://accounts.magento.cloud)登录。 用户必须已使用相同的电子邮件地址在Adobe中注册。
   >[!NOTE]
   >在[https://account.adobe.com](https://account.adobe.com)处创建或拥有帐户并不自动意味着用户在[https://accounts.magento.cloud](https://accounts.magento.cloud)处拥有帐户。 用户必须先[创建其Commerce帐户](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)。

1. 如果用户已有Adobe帐户但无法登录，请要求他们提交[支持请求](https://experienceleague.adobe.com/home#support)，并将[!UICONTROL 问题原因]设置为&#x200B;*用户管理*。

1. 用户成功登录[https://accounts.magento.cloud](https://accounts.magento.cloud)后，您可以将该用户添加到项目中。 有关详细步骤，请参阅Commerce on Cloud Infrastructure指南中的[添加用户和管理访问权限](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access#add-users-and-manage-access)。

## 相关阅读：

* 我们的Commerce on Cloud Infrastructure指南中的[管理用户访问权限](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html)。
* [无法登录Adobe Commerce支持或云帐户](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-to-log-in-to-support-or-cloud-project.html)
