---
title: 如何在支持通知中包含团队成员
description: 本文解释了如何在支持通知中包含团队成员。
feature: Cloud, Support, Admin Workspace
role: Admin, Developer
solution: Commerce
feature-set: Commerce
exl-id: 392ef795-f710-401f-8b0e-3c8dfec7bb3a
TQID: 'https://experienceleague.adobe.com/fWRfvDT8NCwPfzmAx1Zowo4T8KvKLKWqhDkZDfX8stU'
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: e7dae43f-215c-4cdf-90d3-c5a461a6e669
subfeature_v2: id: bb2df8be-afdd-4818-b6b5-95ca1dd3bc3a
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9f1760d31cd80e0358aa341c3f6091b2a86b6d67
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 12%

---


# 如何在支持通知中包含团队成员

本文阐述如何包含团队成员以使其通过电子邮件通知自动接收支持更新。

## 受影响的产品和版本

* 云基础架构上的Adobe Commerce，所有[支持的版本](https://www.adobe.com/content/dam/cc/en/legal/terms/enterprise/pdfs/Adobe-Commerce-Software-Lifecycle-Policy.pdf)。

## 原因

* 尚未将该团队成员添加到具有必要权限的[!DNL cloud project]。
* 团队成员没有支持帐户。

## 解决方案

1. 转到&#x200B;**[!DNL Cloud Project URL]**（示例： `https://us-3.magento.cloud/projects/xxxxxx/edit`）。
1. 验证团队成员是否已添加到项目中，并且是[!DNL Project Admin]。

如果它们尚未添加到项目中，则需要将它们添加为[!DNL Project Admin]并授予[!DNL Shared Access]：

* 在我们的用户指南中[管理用户访问权限](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html)。
* [无法向Commerce知识库中的Adobe Commerce云项目](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/unable-add-user-adobe-commerce-cloud-project.html)添加用户。
* [Adobe Commerce帮助中心用户指南：在我们的Commerce知识库中共享访问权限](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#shared-access)。

如果他们已添加到[!DNL cloud project]，但没有该[!DNL Project Admin role]，请在[管理用户访问权限](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html)中相应地更新其[!DNL role]。

如果您希望使团队成员成为您组织的所有已打开案例的关注者，请提交[支持票证](https://experienceleague.adobe.com/home?lang=en&support-tab=home#support)。

## 相关阅读

[以前的团队成员会收到Adobe Commerce Cloud通知电子邮件](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)
