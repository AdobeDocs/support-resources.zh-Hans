---
title: 管理组织层次结构
description: 了解全局管理员如何在Global Admin Console中管理组织的层次结构。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
exl-id: 6fcf16e3-0408-4961-9981-14d526e1ea28
source-git-commit: 976bfc44cdae61376e2da89019f7758518c6fadc
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 0%

---

# 管理组织层次结构

适用于企业。

了解全局管理员如何在Global Admin Console中管理组织的层次结构。

获得[对 [!DNL Global Admin Console]](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration#request-access-to-the-global-admin-console)的访问权限后，您可以创建新组织、将现有组织添加到层次结构、删除组织和更改父组织。 转到此处[登录到Global Admin Console](https://global-admin-console.adobe.com/)

组织是一种用于管理Adobe产品和用户的结构。 [[!DNL Adobe Admin Console]](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/admin-console-overview)允许管理员管理其组织中产品和用户的部署和配置。 [[!DNL Global Admin Console]](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/adopt-global-administration)允许全局管理员创建、管理和删除多个组织。

## 创建子组织

作为[全局管理员](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以在层次结构中创建任何组织的子组织，并设置名称、国家/地区、用户组、产品、产品配置文件、管理员和策略。

创建新子组织时，系统会自动从直接父项继承以下内容：

- 组织的[策略](https://helpx.adobe.com/cn/enterprise/global-admin-console/update-policies.html)设置（如果存在，则包括锁定）。
- 系统管理员列表（由创建&#x200B;**&#x200B;**&#x200B;策略[时继承系统管理员的](https://helpx.adobe.com/cn/enterprise/global-admin-console/update-policies.html)控制）。
以下内容可能会阻止系统管理员被继承：
   - 缺少[域信任](https://helpx.adobe.com/cn/enterprise/using/directory-trust.html)。
   - 用户类型限制（添加Adobe ID / Enterprise ID / Federated ID用户策略）。 了解[策略详细信息](https://helpx.adobe.com/cn/enterprise/global-admin-console/update-policies.html)。
- 从父组织有权访问的域访问[[!DNL Federated ID]]或[[!DNL Enterprise ID]]个用户。 这使父组织中的域用户可在子组织中使用。 用户访问权限的继承由&#x200B;**从父组织管理的目录继承用户** [策略](https://helpx.adobe.com/cn/enterprise/global-admin-console/update-policies.html)控制。
- 共享策略、密码策略和安全联系人（在创建子组织时由&#x200B;**继承资产共享设置** [策略](https://helpx.adobe.com/cn/enterprise/global-admin-console/update-policies.html)控制）。

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡中，选择要为其添加子组织的组织。
2. 选择&#x200B;**[!UICONTROL 添加+]**&#x200B;图标。
   ![添加组织](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. 指定组织的&#x200B;**名称**&#x200B;和&#x200B;**国家/地区**。\
   组织的简单名称必须介于4到100个字符之间；路径名的最大长度为255个字符。
   ![添加子组织](/help/adobe-support-tools-guide/assets/add-a-child-organization.png)
4. 选择&#x200B;**[!UICONTROL 保存]**。
5. 在编辑完组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/execute-jobs.html)。

## 删除子组织

作为[全局管理员](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以删除子组织。 无法撤消删除操作，并且无法删除根组织。 分配给已删除组织的资源将返回至其父组织。 在删除组织之前，其父项会自动成为其任何子组织的父项。

仅当满足以下条件时，才能删除组织：

- 组织中没有Sign帐户、Adobe Stock购买或存储库。
- 组织中没有声明的域。
- 组织中没有实例化的产品。
- 组织中没有任何可包含实例化的Experience Cloud产品。

>[!WARNING]
>
>删除组织会影响您的用户。 确保删除组织时没有访问权限或信息会丢失。

1. 登录到[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)。 转到&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡，然后选择要删除的组织。
1. 选择&#x200B;**[!UICONTROL 删除]**&#x200B;图标。
   ![删除组织](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. 在&#x200B;**[!UICONTROL 删除组织]**&#x200B;对话框中，选择&#x200B;**[!UICONTROL 确定]**。
1. 在编辑完组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/execute-jobs.html)。

## 重命名组织

组织名称是贵公司或机构的正式名称，在购买时设置。 用户在登录期间选择配置文件时看到此名称，尤其是如果他们有权访问多个组织的Adobe产品，或者需要从企业配置文件和个人配置文件之间进行选择。

作为[全局管理员](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以编辑任何父或子组织的名称，以帮助用户在登录到[[!DNL Creative Cloud]]产品和服务时识别正确的配置文件。

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡中，选择要重命名组织。
1. 选择&#x200B;**[!UICONTROL 编辑]**&#x200B;图标。
   ![重命名组织](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. 更新您的组织名称并选择&#x200B;**[!UICONTROL 保存]**。

>[!TIP]
>
>使用最多255个字符的清晰、可识别的组织名称来帮助用户选择正确的配置文件。 避免使用特殊字符，并考虑包括地区、部门或权利。 此外，请避免在组织层次结构中使用不常见的首字母缩略词以及模糊或类似的名称。

更改会记录到审核日志中，所有用户都会收到电子邮件通知，并且名称在24小时内无法再次更新。 [了解如何查看和下载审核日志](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/download-audit-logs-and-export-reports)。

## 更改组织的父级

作为[[!DNL Global Administrator]](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以使用&#x200B;**[!UICONTROL 更改层次结构]**&#x200B;按钮重新父级组织层次结构中的组织。

更改组织的父项会产生以下影响：

- 为组织重新设置父项会移动以重新设置父项的组织为根的整个子树。 已重设父级组织的路径名及其子级将更新以反映它们的新位置。
- 已更新已移动组织的组织[策略](https://helpx.adobe.com/cn/enterprise/global-admin-console/update-policies.html)，以便新层次结构中的组织保留对策略的任何锁定。
- 更改组织在层次结构中的职位可以更改该组织的全局管理员。 全局管理角色沿层级继承，因此新父组织的任何全局管理员都会自动成为所移动组织的全局管理员。 同样，如果全局管理员因是旧父项的全局管理员而拥有移动组织的角色，则他们可能会失去该角色。 继承的全局管理角色未列在组织的“管理员”窗格中。
- 重新设定父母身份也会影响已移动组织中的可用产品。 如有可能，将更新[产品分配](https://helpx.adobe.com/cn/enterprise/global-admin-console/allocate-products.html)，以便它们通过新的父位置来访问。
- 如果无法更新产品分配以使其来自新父项，则将删除产品以及这些产品的产品配置文件。 此操作可能导致用户失去访问权限。 要使产品在新位置可用，新旧位置之间最近的共同祖先必须拥有可用的产品。

>[!WARNING]
>
>如果因重新为人父母而删除了产品，则用户将无法访问这些产品。

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL 更改层次结构]**&#x200B;以启用组织重设父级。
2. 在显示的弹出屏幕中选择&#x200B;**[!UICONTROL 确定]**。
3. 要重新父项，请将子组织拖动到所需组织的顶部。
4. 完成组织重设父级后，选择&#x200B;**[!UICONTROL 保存]**。
5. 在编辑完组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/execute-jobs.html)。

作业完成后，您可以导航到“产品分配”，然后[更改授权值](https://helpx.adobe.com/cn/enterprise/global-admin-console/allocate-products.html)以反映产品资源分配中的更改。

## 使用组织映射器添加现有组织

作为[全局管理员](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)，您可以将当前不属于Global Admin Console层次结构的现有组织添加到组织层次结构。

您还可以将小组组织添加到组织层次结构。 团队组织不参与产品分配或产品使用汇总，并且Global Admin Console中的团队组织管理有限。 您可以将受众添加到组织层次结构中以跟踪受众，并可以查看他们购买的产品。 团队组织不能在其下具有子组织，并且不具有企业组织的许多功能。

了解有关产品分配[的](https://helpx.adobe.com/cn/enterprise/global-admin-console/allocate-products.html#limitations)限制的更多信息。

>[!WARNING]
>
> 您只能将子组织添加到基于同一存储模型的根组织。 因此，只能将基于用户存储模型的子组织添加到基于用户存储模型的根组织。 而且，只能将基于企业存储模型的子组织添加到基于企业存储模型的根组织。

**[!UICONTROL 组织映射器]**&#x200B;选项卡显示以下内容：

1. 一个下拉列表，其中包含可添加子组织的可能父组织的列表。 这些组织是您作为全局管理员的组织。
1. 可以在步骤1中选择的父项下添加的子组织列表。 这些组织是您是其系统管理员且已不是其他组织的子项的组织。

将组织添加到全局管理时，使用组织映射器添加的组织中的产品仍为购买；[产品分配](https://helpx.adobe.com/cn/enterprise/global-admin-console/allocate-products.html)数字在这些组织中停止汇总。

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)，然后导航到&#x200B;**[!UICONTROL 组织映射器]**。
2. 从下拉列表中选择一个父组织。\
   这些组织是您直接作为全局管理员添加的组织。 在下拉列表中，如果您没有看到要用作父项的组织，请选择层次结构中较高的一个。 组织映射器操作完成后，您可以使用[更改层次结构](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/set-up-organizations#change-the-parent-of-an-organization)在树中向下移动新组织，以便拥有要使用的父组织。
3. 选择要作为上一步中所选组织的子项添加的组织。
4. 选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 然后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/execute-jobs.html)。
5. 执行更改后，您可以重复上述步骤，向组织层次结构中添加其他子组织。

当组织进入层次结构后，您可以通过导航到&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡来调整组织策略、管理员或其他设置。
