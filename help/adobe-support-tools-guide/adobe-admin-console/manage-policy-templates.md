---
title: 在Global Admin Console中管理策略模板
description: 了解全局管理员如何将策略模板直接或间接地从存储在Global Admin Console中的组织应用到任何子组织。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: e4dc5c35-1323-4894-bd47-b31c61a864bc
source-git-commit: ad324036dbeb2a54855349321b2ba33405d2c075
workflow-type: tm+mt
source-wordcount: 705
ht-degree: 0%

---

# 在Global Admin Console中管理策略模板

**应用于：**&#x200B;企业

了解全局管理员如何将策略模板直接或间接地从存储在Global Admin Console中的组织应用到任何子组织。

>[!NOTE]
>
>在[Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html)中，选择要编辑的组织，并导航到&#x200B;**策略模板**&#x200B;选项卡，以简化设置并简化跨组织的一致策略管理。
>
> [登录到Global Admin Console](https://global-admin-console.adobe.com/)

## 策略模板的工作方式

策略模板与组织一起存储，并对该组织的所有全局管理员可见。 应用策略模板中的条目后，将在每个组织中单独设置。 将策略模板应用于组织时，策略模板中的每个条目都将应用于组织的策略，并替换现有策略值。

### 锁定的策略行为

仅当应用更新的用户是由正在更新的策略的&#x200B;**[!UICONTROL 锁定者]**&#x200B;图标所指示的组织的全局管理员时，才会执行对锁定策略的更新。

如果应用模板的用户有权解锁策略，则策略锁定会获取所应用模板（已锁定或已解锁）的值。 如果模板指示锁定应保持不变，则策略中锁的值将与之前相同。

### 有关保存的重要说明

>[!NOTE]
>
>与Global Admin Console中的其他更改不同，对策略模板的编辑将立即生效，而无需执行&#x200B;**[!UICONTROL 审核待处理更改 — 提交]**&#x200B;流程。 但是，要在应用策略模板的组织中实施挂起的更改，需要[提交](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

## 创建策略模板

1. 在[Global Admin Console](https://global-admin-console.adobe.com/)中，选择要编辑的组织，然后导航到&#x200B;**[!UICONTROL 策略模板]**&#x200B;选项卡。
1. 选择&#x200B;**[!UICONTROL 创建模板]**.<br>
   ![Pic1](./assets/DXSKB-3209-1-ga_14.png)
   <br>
1. 在&#x200B;**[!UICONTROL 创建策略模板]**&#x200B;对话框中，输入策略模板的&#x200B;**名称**&#x200B;和&#x200B;**描述**。<br>策略模板的名称最多可为100个字符。
1. 选择要包含在模板中的策略。
1. 为所选策略设置值（请参阅下面的[设置策略值](#setting-policy-values)）。
1. 选择&#x200B;**[!UICONTROL 保存]**。

### 设置策略值 {#setting-policy-values}

对于模板中包含的每个策略，请配置两个设置：

* **允许/不允许：**&#x200B;将滑块设置为所需的值。 了解[策略详细信息](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html#policy-details)。
* **锁定值：**&#x200B;使用以下选项之一修改策略的锁定状态：
   * **锁定** — 应用模板后将锁定策略。
   * **解锁** — 应用模板后将解锁策略。
   * **保持原样** — 策略的锁定状态将保持与应用模板之前相同。<br>
     ![Pic2](./assets/DXSKB-3209-2-policy-template.png)
<br>

## 将模板应用于组织

1. 在[Global Admin Console](https://global-admin-console.adobe.com/)中，选择要编辑的组织，然后导航到&#x200B;**[!UICONTROL 策略模板]**&#x200B;选项卡。
1. 为相关策略模板选择&#x200B;**[!UICONTROL 更多选项]** ![更多选项](./assets/manage-product-profiles_more-options.png)图标，然后选择&#x200B;**[!UICONTROL 将模板应用到组织]**。<br>
   ![Pic3](./assets/DXSKB-3209-3-ga_15.png)
   <br>
1. 选择要应用模板的组织。 您可以选择多个组织。<br>
   ![Pic4](./assets/DXSKB-3209-4-bulk-apply-template.png)
   <br>
1. 选择&#x200B;**[!UICONTROL 应用模板]**。
1. 要在应用策略模板的组织中实施挂起的更改，请选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

如果所选组织中的所有策略值已经与模板中的值匹配，则会显示一条消息，通知未进行任何更改。 此外，如果没有其他待处理编辑，则不会启用&#x200B;**[!UICONTROL 审阅待处理更改]**。

## 编辑模板

1. 在[Global Admin Console](https://global-admin-console.adobe.com/)中，选择要编辑的组织，然后导航到&#x200B;**[!UICONTROL 策略模板]**&#x200B;选项卡。
1. 为相关模板选择&#x200B;**[!UICONTROL 更多选项]**&#x200B;图标![更多选项](./assets/manage-product-profiles_more-options.png)，然后选择&#x200B;**[!UICONTROL 编辑模板]**。<br>
   ![Pic5](./assets/DXSKB-3209-5-ga_15-1.png)
   <br>
1. 更新策略模板并选择&#x200B;**[!UICONTROL 立即更新]**。
1. 要在应用策略模板的组织中实施挂起的更改，请选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

## 删除模板

1. 在[Global Admin Console](https://global-admin-console.adobe.com/)中，选择要编辑的组织，然后导航到&#x200B;**[!UICONTROL 策略模板]**&#x200B;选项卡。
1. 为相关模板选择&#x200B;**[!UICONTROL 更多选项]** ![更多选项](./assets/manage-product-profiles_more-options.png)图标，然后选择&#x200B;**[!UICONTROL 删除模板]**。<br>
   ![Pic6](./assets/DXSKB-3209-6-ga_15-2.png)
   <br>
1. 在出现的对话框中选择&#x200B;*是*。
