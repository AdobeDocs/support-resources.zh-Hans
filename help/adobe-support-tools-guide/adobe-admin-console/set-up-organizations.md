---
title: 管理组织层次结构
description: Learn how global administrators can manage the organization’s hierarchy in the Global Admin Console.
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: 3b3b2711887f0db086e4eb8281344cc7356accf7
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---

# 管理组织层次结构

适用于企业。

了解全局管理员如何在Global Admin Console中管理组织的层次结构。

在获得[对 [!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html#request-access)的访问权限后，您可以创建新组织、将现有组织添加到层次结构、删除组织以及更改父组织。
[登录Global Admin Console](https://global-admin-console.adobe.com/)

组织是一种用于管理Adobe产品和用户的结构。 [[!DNL Adobe Admin Console]](https://helpx.adobe.com/enterprise/using/admin-console.html)允许管理员管理其组织中产品和用户的部署和配置。 [[!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/overview.html)允许全局管理员创建、管理和删除多个组织。

## 创建子组织

作为[全局管理员](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)，您可以在层次结构中创建任何组织的子组织，并设置名称、国家/地区、用户组、产品、产品配置文件、管理员和策略。

创建新子组织时，系统会自动从直接父项继承以下内容：

- 组织的[策略](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)设置（如果存在，则包括锁定）。
- 系统管理员列表（受&#x200B;**[!UICONTROL 创建时继承系统管理员]** [策略](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)控制）。
以下情况可能会阻止继承系统管理员：
   - 缺少[域信任](https://helpx.adobe.com/enterprise/using/directory-trust.html)。
   - 用户类型限制（添加Adobe ID/Enterprise ID/Federated ID用户策略）。 了解[策略详细信息](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)。
- Access to [[!DNL Federated ID]] or [[!DNL Enterprise ID]] users from domains to which the parent org has access. This makes the domain users in the parent available in the child org. 用户访问权限的继承受&#x200B;**从父组织管理的目录继承用户** [策略](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)控制。
- Sharing policy, password policy, and security contacts (controlled by **Inherit asset sharing settings when child organization is created** [policy](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)).

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)。 In the **[!UICONTROL Organizations]** tab, select the organization you want to add a child organization to.
2. 选择&#x200B;**[!UICONTROL 添加+]**&#x200B;图标。
   ![添加组织](/help/adobe-support-tools-guide/assets/add-an-organization-1.png)
3. 指定组织的&#x200B;**名称**&#x200B;和&#x200B;**国家/地区**。\
   组织的简单名称必须介于4到100个字符之间；路径名的最大长度为255个字符。
   ![添加子组织](/help/adobe-support-tools-guide/assets/add-an-child-organization.png)
4. 选择&#x200B;**[!UICONTROL 保存]**。
5. 在编辑完组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

## 删除子组织

作为[全局管理员](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)，您可以删除子组织。 无法撤消删除操作，并且无法删除根组织。 分配给被删除的组织的资源将归还给其父组织。 在删除组织之前，其父级自动成为其任何子组织的父级。

只有在满足以下条件时才能删除组织：

- There are no Sign accounts, Adobe Stock purchases, or storage repositories in the organization.
- 该组织中没有已申请的域。
- 该组织中没有实例化产品。
- Experience Cloud中没有可包括实例化的组织产品。

>[!WARNING]
>
>删除组织影响您的用户。 确保在删除组织时不会丢失任何访问权限或信息。

1. 登录到[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)。 转到&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡，然后选择要删除的组织。
1. Select the **[!UICONTROL Delete]** icon.
   ![Delete organization](/help/adobe-support-tools-guide/assets/delete-organization.png)
1. In the **[!UICONTROL Delete Organization]** dialog box, select **[!UICONTROL OK]**.
1. 编辑完组织后，选择&#x200B;**[!UICONTROL 查看挂起的更改]**。 审核后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;到[执行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)个更改。

## Rename an organization

组织名称是贵公司或机构的正式名称，在购买时设置。 用户在登录期间选择配置文件时看到此名称，尤其是如果他们有权访问多个组织的Adobe产品，或者需要从企业配置文件和个人配置文件之间进行选择。

作为[全局管理员](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)，您可以编辑任何父或子组织的名称，以帮助用户在登录到[[!DNL Creative Cloud]]产品和服务时识别正确的配置文件。

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡中，选择要重命名组织。
1. Select the **[!UICONTROL Edit]** icon.
   ![重命名组织](/help/adobe-support-tools-guide/assets/rename-organization.png)
1. 更新您的组织名称并选择&#x200B;**[!UICONTROL 保存]**。

>[!TIP]
>
>使用最多255个字符的清晰、可识别的组织名称来帮助用户选择正确的配置文件。 避免使用特殊字符，并考虑包括地区、部门或权利。 此外，请避免在组织层次结构中使用不常见的首字母缩略词以及模糊或类似的名称。
>使用最多255个字符的清晰、可识别的组织名称来帮助用户选择正确的配置文件。 避免使用特殊字符，并考虑包括地区、部门或权利。 此外，请避免在组织层次结构中使用不常见的首字母缩略词以及模糊或类似的名称。

更改会记录到审核日志中，所有用户都会收到电子邮件通知，并且名称在24小时内无法再次更新。 [了解如何查看和下载审核日志](https://helpx.adobe.com/enterprise/global-admin-console/insights.html)。

## 更改组织的父级

作为[[!DNL Global Administrator]](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html)，您可以使用&#x200B;**[!UICONTROL 更改层次结构]**&#x200B;按钮重新父级组织层次结构中的组织。

更改组织的父项会产生以下影响：

- 为组织重新设置父项会移动以重新设置父项的组织为根的整个子树。 已重设父级组织的路径名及其子级将更新以反映它们的新位置。
- 已更新已移动组织的组织[策略](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)，以便新层次结构中的组织保留对策略的任何锁定。
- 更改组织在该层次结构中的位置可能会更改该组织的全局管理员。 全局管理角色继承在层级结构下，因此新父组织的任何全局管理员都会自动成为被移动组织的全局管理员。 同样，如果全局管理员由于是旧父代的全局管理员而具有被移动组织中的全局管理员角色，则全局管理员可能也会失去该角色。 继承的全局管理角色未在组织的“管理员”窗格中列出。
- 重新养育子女还会影响被移动组织中的可用产品。 如有可能，将更新[产品分配](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)，以便它们通过新的父位置获得。
- 如果无法更新产品分配以使其来自新父项，则将删除产品以及这些产品的产品配置文件。 此操作可能导致用户失去访问权限。 要使产品在新位置可用，新旧位置之间最近的共同祖先必须拥有可用的产品。

>[!WARNING]
>
>如果因重新为人父母而删除了产品，则用户将无法访问这些产品。

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL 更改层次结构]**&#x200B;以启用组织重设父级。
2. 在显示的弹出屏幕中选择&#x200B;**[!UICONTROL OK]**。
3. 要重新父项，请将子组织拖动到所需组织的顶部。
4. 完成组织重设父级后，选择&#x200B;**[!UICONTROL 保存]**。
5. 在编辑完组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

作业完成后，您可以导航到“产品分配”，然后[更改授权值](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)以反映产品资源分配中的更改。

## 使用组织映射器添加现有组织

As a [Global Administrator](https://helpx.adobe.com/enterprise/global-admin-console/manage-administrators.html), you can add existing organizations that are not currently part of your Global Admin Console hierarchy to the organization hierarchy.

You can also add team organizations to the org hierarchy. Team orgs don&#39;t participate in product allocation or product usage rollup, and management of team organizations in the Global Admin Console is limited. 您可以将它们添加到组织层次结构以跟踪它们并可查看它们购买的产品。 团队组织不能具有子组织，并且不具备企业组织的许多功能。

了解有关产品分配[的](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html#limitations)限制的更多信息。

>[!WARNING]
>
> 您只能将子组织添加到基于同一存储模型的根组织中。 因此，基于用户存储模型的子组织只能添加到基于用户存储模型的根组织中。 而且，只能将基于企业存储模型的子组织添加到基于企业存储模型的根组织。
>您只能将子组织添加到基于同一存储模型的根组织。 因此，只能将基于用户存储模型的子组织添加到基于用户存储模型的根组织。 而且，只能将基于企业存储模型的子组织添加到基于企业存储模型的根组织。

**[!UICONTROL 组织映射器]**&#x200B;选项卡显示以下内容：

1. 一个下拉列表，其中包含可添加子组织的可能父组织的列表。 这些组织是您作为全局管理员的组织。
1. 可以在步骤1中选择的父项下添加的子组织列表。 您是这些组织的系统管理员，并且这些组织还不是其他组织的子级。

将组织添加到全局管理后，组织中使用组织映射器添加的产品仍为已购买；在这些组织上停止汇总[产品分配](https://helpx.adobe.com/enterprise/global-admin-console/allocate-products.html)数字。

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)，然后导航到&#x200B;**[!UICONTROL 组织映射器]**。
2. 从下拉列表中选择父组织。\
   这些组织是您直接作为全局管理员添加的组织。 In the drop-down list, if you don&#39;t see an organization you want to use as the parent, select one higher up in the hierarchy. Once the Organization mapper operation is complete, you can use [Change hierarchy](https://helpx.adobe.com/enterprise/global-admin-console/set-up-organizations.html#change-the-parent-of-an-organization) to move the new organization down in the tree to have the parent you want to use.
3. 选择要作为在上一步中选择的组织的子级而添加的组织。
4. 选择&#x200B;**[!UICONTROL 查看待处理的更改]**。 然后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)更改。
5. 执行这些更改后，可重复上述步骤以将其他子组织添加到您的组织层次结构。

当某个组织进入层次结构后，您可通过导航到&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡而调整该组织的策略、管理员或其他设置。
