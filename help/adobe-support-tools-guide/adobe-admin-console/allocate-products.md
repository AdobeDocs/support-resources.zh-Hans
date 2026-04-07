---
title: 使用Global Admin Console将产品分配给子组织
description: 了解全局管理员如何向子组织分配资源，从而实现每个组织内有效的资源管理和用户分配。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: de6e785d-8965-40d5-ac78-7fbb2cd7afc7
source-git-commit: d5f0473b100cda574b4980e6c871a9c275f9f95a
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# 使用Global Admin Console将产品分配给子组织

适用于企业。

了解全局管理员如何向子组织分配资源，从而实现每个组织内有效的资源管理和用户分配。

在[Global Admin Console](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)中，转到&#x200B;**[!UICONTROL 产品分配]**&#x200B;选项卡，然后选择要分配给子组织的产品。

登录到[Global Admin Console](https://global-admin-console.adobe.com)。

>[!NOTE]
>
>**[!UICONTROL 产品分配]**&#x200B;仅适用于企业定期许可协议(ETLA)合同。

在组织间分发和管理Adobe产品的一部分就是将购买的资源分区为要管理的组织间的资源分配。 通过提供全部或部分资源，您可以将产品资源的管理分发给其他组织。 并非所有产品的所有资源都可以分配；某些产品不可分配给其他组织。 此类产品显示在&#x200B;**[!UICONTROL 产品分配]**&#x200B;选项卡中，但没有控件可将其添加到其他组织。

>[!WARNING]
>
>您无法从具有&#x200B;**已过期**&#x200B;的合同或组织处于&#x200B;**不活动**&#x200B;状态的合同将产品分配给子组织。 了解有关[合同到期](https://helpx.adobe.com/cn/enterprise/using/contract-expiry.html)的详细信息，或联系您公司的管理员以获取帮助，以防止子组织中的用户无法访问其Adobe应用程序和服务。

## 池化存储

这适用于在其Admin Console中具有“存储”选项卡的客户。 如果您看不到“存储”选项卡，则表示Admin Console尚未更新到企业存储模型。 在迁移组织后，您将看到以下更改：

- 全局管理员可以跨层次结构获得对存储配额和使用情况的访问权限，并且可以使用&#x200B;**[!UICONTROL Global Admin Console]**&#x200B;中的[产品分配](https://adminconsole.adobe.com/)选项卡将存储分配给组织。
- 系统管理员和存储管理员可以完全控制和查看整个组织的存储。 他们可以使用&#x200B;**[!UICONTROL Adobe Admin Console]**&#x200B;中的[存储](https://adminconsole.adobe.com/)选项卡跟踪和管理存储。

随着对Adobe Creative Cloud存储的更新，存储配额对最终用户而言是灵活的，其数量取决于企业购买的存储容量。 [了解详情](https://helpx.adobe.com/cn/enterprise/using/manage-adobe-storage.html)。

## 分配产品

Global Admin Console中的&#x200B;**[!UICONTROL 产品分配]**&#x200B;选项卡显示跨组织层次结构购买的产品分配单位。 作为[全局管理员](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)，您可以将这些产品资源分配给组织树中的另一个组织，并指定分配数量。 作为[全局查看器](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)，您可以查看和导出数据，但无法进行任何更新。

要将产品分配给组织，请执行以下步骤：

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com)，然后转到&#x200B;**[!UICONTROL 产品分配]**。
1. 从下拉列表中选择产品，以查看如何将其分配给不同的组织。\
   如果组织当前没有该产品，则会显示&#x200B;**[!UICONTROL 添加+]**&#x200B;图标。

   >[ !N注意]
   >
   >如果子组织已有采购合同，则父组织向该子组织的产品分配可能会受到限制。 [了解详情](https://helpx.adobe.com/cn/enterprise/global-admin-console/allocate-products.html#limited-product-allocation)。

1. 要分配产品，请选择相关组织的&#x200B;**[!UICONTROL 添加+]**&#x200B;图标。\
   某些产品包含多个可分配的资源；在这种情况下，对话框中列出了多个资源，您必须为每个资源提供值。 例如，Adobe Stock可以包含Adobe Stock图像积分和高级积分。
   ![Adobe Stock图像](/help/adobe-support-tools-guide/assets/adobe-stock-images.png)
1. 在出现的对话框中，指定产品数量。
1. 选择&#x200B;**[!UICONTROL 保存]**。
1. 要允许或不允许过度分配资源，请选择相关的切换开关。
   ![过度分配](/help/adobe-support-tools-guide/assets/overallocation.png)
1. 在分配完资源后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/execute-jobs.html)。

## 分配并分发Adobe Acrobat Sign用户许可证或交易

通过Global Admin Console，您可以在组织层次结构中分配和分发Acrobat Sign用户许可证或交易。 层次结构中分配了Acrobat Sign许可证或交易的每个组织均会创建自己的单独Acrobat Sign帐户。

- 创建的每个Acrobat Sign帐户都是独立的，在管理和内容方面处于孤立状态。
- 每个Acrobat Sign帐户均不知道其他Acrobat Sign帐户（例如，在父组织或姐妹组织中）。

了解有关[在Admin Console中管理Adobe Acrobat Sign](https://helpx.adobe.com/cn/enterprise/using/adobe-sign-for-enterprise.html)的更多信息。

要管理身份验证插件，例如基于知识的身份验证(KBA)和电话身份验证(PA)，请联系您的Adobe代表或客户成功经理。


## 产品分配的限制

在以下情况下，从父组织到子组织的分配受到限制：

- 如果两个组织具有不同的合同，并且您尝试分配的产品同时存在于两个组织中，则不允许在合同之间混合使用同一选件。
- 如果两个组织具有相同的合同，您可以通过联系您的Adobe代表或[提交支持](https://helpx.adobe.com/cn/enterprise/using/support-for-enterprise.html)案例，指定Global Admin Console中的&#x200B;**[!UICONTROL 产品分配]**&#x200B;被阻止，来请求分配产品的权限。

## 过度分配

作为[全局管理员](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators#admins)，您可以允许过度分配资源。

与产品和组织关联的分配[策略](https://helpx.adobe.com/cn/enterprise/global-admin-console/update-policies.html#update-policies)指示是否允许过度分配。

过度分配允许授予子组织的产品资源多于父组织中的可用资源。 当分配已近似并且管理员不想负担使资源分配相加的负担时，此变量非常有用。
如果对组织中的产品资源禁用过度分配，则子授权的总和不能超过父授权。 对于标记为已禁用过度分配的资源，将不会执行过度分配请求。
当过度分配切换从启用切换到禁用时，如果资源的授权数量中存在过度分配情况，则必须调整授权值以消除过度分配，然后才能执行授权更新。

![过度分配](/help/adobe-support-tools-guide/assets/overallocation.png)

## 层次结构中过期的合同

您不能将已过期的ETLA合同中的产品分配给子组织。 **[!UICONTROL 概述]**&#x200B;和&#x200B;**[!UICONTROL 产品分配]**&#x200B;页面上的应用程序内横幅和通知（如以下内容）明确指示一个或多个子组织的合同何时到期、过期或不活动。

![产品分配](/help/adobe-support-tools-guide/assets/product-allocation.png)

>[ !I重要信息]
>
>属于层次结构的ETLA合同一旦停用，产品就会从&#x200B;**[!UICONTROL 概述]**&#x200B;和&#x200B;**[!UICONTROL 产品分配]**&#x200B;页面中删除。

[了解有关合同到期的详细信息](https://helpx.adobe.com/cn/enterprise/using/contract-expiry.html)，或联系贵公司的管理员以获取帮助，以防止子组织中的用户无法访问其Adobe应用程序和服务。
