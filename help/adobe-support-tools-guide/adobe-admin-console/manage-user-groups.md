---
title: 在Global Admin Console中管理用户组
description: 了解如何在Global Admin Console中创建、共享、编辑和删除用户组以简化跨组织的用户管理。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 1e20362a-0974-4b83-a083-9edaab04c255
source-git-commit: 265c341935b3257e5731a129c42411151645ae89
workflow-type: tm+mt
source-wordcount: '1330'
ht-degree: 0%

---

# 在Global Admin Console中管理用户组

在Global Admin Console中创建、管理和共享用户组，通过对具有相同权限的用户进行分组、节省时间和确保一致性，从而简化用户管理。

在[Global Admin Console](https://helpx.adobe.com/cn/enterprise/global-admin-console/adopt-global-administration.html)中，选择一个组织，然后导航到&#x200B;**[!UICONTROL 用户组]**。 使用单个用户管理源跨多个组织共享组以同步用户和组。

[登录到Global Admin Console](https://global-admin-console.adobe.com)



## 创建用户组

您可以[批量单独创建用户组](https://helpx.adobe.com/cn/enterprise/using/user-groups.html)，或将[用户组从已建立的Azure AD](https://helpx.adobe.com/cn/enterprise/using/add-azure-sync.html)直接同步到Adobe Admin Console中的联合目录。 在Global Admin Console中，您可以定义分配了相关产品配置文件的用户组，用户组管理员稍后可以使用Admin Console将用户添加到这些用户组。

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)，选择要编辑的组织，然后导航到&#x200B;**[!UICONTROL 用户组]**&#x200B;选项卡。

2. 选择&#x200B;**[!UICONTROL 添加用户组]**。

   在Global Admin Console中选择了“用户组”选项卡的“![组织”选项卡。](assets/add-user-group.png "添加用户组")

   _将用户组添加到组织以简化用户管理。_

3. 在出现的&#x200B;**[!UICONTROL 添加用户组]**&#x200B;对话框中输入以下内容：
   - **[!UICONTROL 名称]**：指定用户组的名称。
   - **[!UICONTROL 产品配置文件]**：如果要向用户组中当前或将来的成员授予产品访问权限，请单击下拉箭头以从列表中选择产品配置文件，或输入产品配置文件名称并从显示的下拉列表中选择该名称。 如果要添加尚未创建的产品配置文件，必须首先使用[产品配置文件](https://helpx.adobe.com/cn/enterprise/using/global-admin-edit-organizations.html#profiles)选项卡执行此操作。
   - **[!UICONTROL 管理员]**：单击下拉箭头从列表中选择管理员，或输入管理员的电子邮件地址并从显示的下拉列表中选择该地址。 如果要添加尚未创建的新管理员，必须首先使用[管理员](#share-user-groups)选项卡创建该管理员。

   您指定的产品配置文件将分配给用户组，并且您指定的管理员将成为该组的用户组管理员。 用户组管理员可以使用相关组织的Adobe Admin Console来管理组。

4. 选择&#x200B;**[!UICONTROL 保存]**。

5. 选择&#x200B;**[!UICONTROL 审阅挂起的更改]**&#x200B;以审阅更新。 然后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/set-up-organizations.html#execute-jobs)。

   >[!NOTE]
   >
   >全局管理员可以使用Global Admin Console [将产品配置文件和用户组管理员](#review-user-groups)分配给用户组。 使用Adobe Admin Console，系统管理员和用户组管理员可以[添加用户，并将管理员和产品配置文件](https://helpx.adobe.com/cn/enterprise/using/user-groups.html)分配给用户组。



## 共享用户组

组投影允许您将用户组及其关联用户从单个管理源同步到多个Admin Console。 全局管理员可与源组织的层级子代共享用户组，向下工作，而不是向上或并排工作。

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)，选择一个组织，然后导航到&#x200B;**[!UICONTROL 用户组]**&#x200B;选项卡。

2. 选中要共享的用户组的复选框。

   在以下情况下，可能会禁用组共享：
   - 用户组是从其他组织共享的。 要共享或编辑组，请从组织层次结构中选择拥有该组的组织。
   - 组织未使用[用于企业的Adobe存储](https://helpx.adobe.com/in/enterprise/using/storage-for-business.html)，该存储正在分阶段在全球推出。
   - 已禁用组织策略。 转到&#x200B;**[!UICONTROL 策略]**&#x200B;选项卡以打开&#x200B;**[!UICONTROL 管理共享用户组]**&#x200B;策略。
   - 组织没有任何要与其共享用户组的子组织。

3. 选择&#x200B;**[!UICONTROL 共享用户组]**。

4. <a id="review-user-groups"></a>查看要与其他组织共享的用户组。 如果您还是所选组织的系统管理员，请选择&#x200B;**[!UICONTROL 在Admin Console中打开]** <img src="assets/icon-open-in-admin-console.png" alt="在Admin Console中打开图标" width="14" height="14">图标以查看Adobe Admin Console中的用户组成员列表。

   >[!NOTE]
   >
   >要防止冲突，请确保您计划与其共享用户组的组织不具有同名组。

5. 选择&#x200B;**[!UICONTROL 下一步]**。

6. 选择要与其共享用户组的组织，然后选择&#x200B;**[!UICONTROL 下一步]**。

7. 如果没有冲突，请选择&#x200B;**[!UICONTROL 共享用户组]**。

   如果存在冲突（目标组织中存在具有相同名称的用户组），请选择以下选项之一，然后选择&#x200B;**[!UICONTROL 共享用户组]**：
   - **[!UICONTROL 忽略（默认）]**：跳过目标组织中具有相同名称的组。
   - **[!UICONTROL 仅添加]**：通过将新用户添加到现有用户组而不删除任何用户来合并用户组。
   - **[!UICONTROL 镜像组]**：通过添加或删除用户，调整目标组织的组以匹配共享组。

8. 选择&#x200B;**[!UICONTROL 审阅挂起的更改]**&#x200B;以审阅更新。 然后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/set-up-organizations.html#execute-jobs)。

   将记录组预测事件以供您参考。 了解[查看和下载审核日志](https://helpx.adobe.com/cn/enterprise/global-admin-console/insights.html)。


共享用户组时，该组及其用户将添加到目标组织。 但是，*源用户组控制*&#x200B;共享用户组及其用户。 管理员和产品配置文件分配&#x200B;*未*&#x200B;在组织之间同步。

在目标组织中会自动更新预计用户组名称或源用户组中关联用户的更改。 虽然无法直接管理共享用户组，但目标组织内的管理员可以将产品配置文件分配给共享组，为该组的用户授予许可证访问权限。



## 撤销对共享组的访问权限

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)，选择一个组织，然后导航到&#x200B;**[!UICONTROL 用户组]**&#x200B;选项卡。

2. 为相关用户组选择&#x200B;**[!UICONTROL 管理共享访问权限]**。

3. 选择要撤销其访问权限的组织。

4. 选择&#x200B;**[!UICONTROL 撤销访问权限]**。

5. 撤销访问权限时，您可以选择删除用户组和用户，或者在目标组织中保留副本：
   - 删除时，将从目标组织中删除用户组。 不属于其他共享组的用户将从目标组织中删除，并失去对所有产品、服务和资产的访问权限。
   - 离开副本时，用户组和用户将保留在目标组织中，保持所有分配不变。 但是，该用户组将不再同步，并可由目标组织的管理员管理。

6. 选择&#x200B;**[!UICONTROL 撤销访问权限]**。

7. 选择&#x200B;**[!UICONTROL 审阅挂起的更改]**&#x200B;以审阅更新。 然后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/set-up-organizations.html#execute-jobs)。



## 编辑用户组

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)，选择一个组织，然后导航到&#x200B;**[!UICONTROL 用户组]**&#x200B;选项卡。

2. 选择&#x200B;**[!UICONTROL 更多选项]** 相关用户组的<img src="assets/icon-more-options.png" alt="“更多选项”图标" width="14" height="14" style="vertical-align:middle">图标，然后选择&#x200B;**[!UICONTROL 编辑用户组]**。

   >[!NOTE]
   >
   >您无法编辑所选组织未拥有的用户组。

   ![在“用户组”选项卡下使用“编辑用户组”选项选择的组织。](assets/edit-user-group.png "编辑用户组")

   _编辑用户组以更新用户组名称、产品配置文件或管理员。_

3. 更新用户组名称、产品配置文件或管理员。 然后选择&#x200B;**[!UICONTROL 保存]**。

   >[!NOTE]
   >
   >在&#x200B;**[!UICONTROL 编辑用户组]**&#x200B;向导中，您只能将管理员角色分配给已在此组织中分配了管理员角色的用户。 了解如何[添加新管理员](https://experienceleague.adobe.com/zh-hans/docs/support-resources/adobe-support-tools-guide/adobe-admin-console/manage-administrators)。

4. 选择&#x200B;**[!UICONTROL 审阅挂起的更改]**&#x200B;以审阅更新。 然后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/using/global-admin-set-up-organizations.html#execute-jobs)。

   >[!NOTE]
   >
   >如果更改共享用户组的名称，则会在目标组织中自动更新这些更改。



## 删除用户组

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)，选择一个组织，然后导航到&#x200B;**[!UICONTROL 用户组]**&#x200B;选项卡。

2. 选择&#x200B;**[!UICONTROL 更多选项]** 相关用户组的<img src="assets/icon-more-options.png" alt="“更多选项”图标" width="14" height="14" style="vertical-align:middle">图标，然后选择&#x200B;**[!UICONTROL 删除用户组]**。

   >[!NOTE]
   >
   >您无法删除所选组织未拥有的用户组。

3. 在出现的对话框中选择&#x200B;**[!UICONTROL 确定]**。

   >[!CAUTION]
   >
   >删除用户组可能会影响您的用户。 确保删除用户组时没有访问权限或信息将丢失。

4. 编辑组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**&#x200B;以审阅这些更改。 然后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/using/global-admin-set-up-organizations.html#execute-jobs)。
