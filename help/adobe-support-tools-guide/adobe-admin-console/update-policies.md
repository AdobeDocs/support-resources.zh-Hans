---
title: 在Global Admin Console中更新组织策略
description: 了解全局管理员如何在Global Admin Console中为组织及其子级设置和修改策略。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
product_v2: id: f7bdf6be-dd3b-4d2d-ac52-0e62ed0d3102
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
exl-id: bf8d4e71-30a6-4d6c-8749-47070e5b1906
TQID: https://experienceleague.adobe.com/X-f8Rr9evlFaLc3dBbXwbRvCZDrAHTTuqv-Mpxp-oc4
source-git-commit: d1c3158bb425e7966ccc5e5d79457c6b33e00063
workflow-type: tm+mt
source-wordcount: 1045
ht-degree: 1%

---

# 在Global Admin Console中更新组织策略

**应用于：**&#x200B;企业

了解全局管理员如何在Global Admin Console中为组织及其子级设置和修改策略。

>[!NOTE]
>
>在[Global Admin Console](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html)中，从层次结构中选择一个组织，然后导航到&#x200B;**策略**&#x200B;选项卡以允许或禁止或锁定策略。
>
> [登录到Global Admin Console](https://global-admin-console.adobe.com/)

策略与组织相关联，并限制可以对该组织执行的操作。 设置策略值后，它会限制或启用从该点以后的操作。
例如，如果**声明域**&#x200B;策略设置为&#x200B;*不允许*，则无法声明其他域，但在设置策略值之前声明的任何域都不会受到影响。

## 配置策略

要修改组织的策略，请执行以下操作：

1. 在Global Admin Console中，[选择要编辑的组织](https://helpx.adobe.com/enterprise/global-admin-console/overview.html)，然后导航到&#x200B;**[!UICONTROL 策略]**&#x200B;选项卡。
1. 选择相关策略的切换开关以允许或不允许使用该策略。 您还可以锁定策略，这样[选定组织](https://helpx.adobe.com/enterprise/global-admin-console/overview.html)或其父组织的全局管理员以外的人便无法更改或解锁该策略。
1. 要锁定策略，请选择&#x200B;**[!UICONTROL 锁定]** ![锁定](./assets/lock.png)图标。 将鼠标悬停在锁定上会显示所选组织的名称。 了解有关[策略锁定](#policy-locks)的详细信息。
1. 在编辑完组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

## 策略锁定 {#policy-locks}

锁定策略后，在解锁该策略之前，无法更改其值。 Global Admin Console将组织选取器中的[选定组织](https://helpx.adobe.com/enterprise/global-admin-console/overview.html)记住为锁定策略的组织。 所选组织或树中更高层组织的任何全局管理员都有权解锁策略。 范围小于该组织的全局管理员无权解锁和更改策略值。

要创建锁定的环境，请在子组织上设置所需的策略值，然后锁定它们。 这些子组织的全局管理员将无法编辑策略值。

### 示例：锁定的环境

如果&#x200B;*Acme部门*&#x200B;的全局管理员Elissa创建子组织&#x200B;*Marketing*&#x200B;和&#x200B;*Engineering*，则将Robert添加为&#x200B;*Marketing*&#x200B;的全局管理员，并将Sarah添加为&#x200B;*Engineering*&#x200B;的全局管理员。 接下来，她将多个策略设置为&#x200B;*不允许*&#x200B;和&#x200B;*锁定*。 Elissa以后选择&#x200B;*Acme部门*&#x200B;作为选定的组织时，可以解锁并更改策略值，但Robert和Sarah无法解锁他们作为全局管理员的组织上的策略，因为这些策略已被组织&#x200B;*Acme部门*&#x200B;锁定。

## 策略详细信息

### 组织管理

| 策略名称 | 描述 |
| --- | --- |
| **创建子组织** | 允许全局管理员创建子组织。 如果&#x200B;*off*，则无法创建任何子组织。 |
| **重命名组织** | 如果允许，全局或系统管理员可以重命名组织。 它还控制更改组织的国家/地区。 如果重命名父组织，或者重新命名组织或组织的祖先，也可以独立于此策略设置更改组织的路径名。 |
| **删除组织** | 允许全局管理员删除子组织。 由于存在删除用户资产的风险，因此启用了企业存储的企业将变得更加重要。 |

### 管理员管理

| 策略名称 | 描述 |
| --- | --- |
| **添加或删除管理员** | 允许全局管理员向组织添加新管理员。 如果&#x200B;*off*，则无法添加新管理员。 |
| 创建子组织时&#x200B;**从父组织继承系统管理员** | 当全局管理员创建新子组织时，父项的系统管理员会自动成为新组织的系统管理员。 默认情况下，此策略为&#x200B;*off*。 |
| **管理管理员** | 允许全局管理员更改或删除/编辑管理员权限。 |

### 用户管理

| 策略名称 | 描述 |
| --- | --- |
| **从父组织管理的目录中继承用户** | 此策略必须在创建新子组织之前，在&#x200B;*上切换*&#x200B;并处于活动状态。 创建子组织后，父组织中的用户将作为子组织中的用户使用。 换句话说，在GAC内创建新子项时，此策略会自动在父项和子项之间建立信任关系。 对于现有组织，在加入广汽之前，任何信任关系在加入广汽之后将保持不变。 如果没有建立信任关系，则必须遵循常规信任请求流程。 要成功实施此策略，创建新组织的全局管理员还必须是具有声明域的父组织的系统管理员。 否则，域信任关系将不会继承到新创建的组织中。 |
| **添加Adobe ID用户** | 如果设置，则组织无法通过Admin Console、用户管理API (UMAPI)或同步机制添加Adobe ID类型用户。 |
| **管理用户组** | 如果允许，全局、系统和用户组管理员可以创建、编辑和删除用户组。 |

### 目录和域实施

| 策略名称 | 描述 |
| --- | --- |
| **声明域** | 如果设置，系统管理员可以在Admin Console上声明域。 |
| **更改身份配置** | 如果设置，系统管理员可以在Admin Console上更改用户身份配置的设置。 |

### 产品分配

| 策略名称 | 描述 |
| --- | --- |
| **管理产品** | 允许全局管理员添加或删除产品并更改产品资源授权。 |

### 资源共享

| 策略名称 | 描述 |
| --- | --- |
| **系统或存储管理员可以更改资源共享设置** | 如果允许，存储管理员和系统管理员可以更改资产共享设置，包括安全联系人、密码策略和存储策略。 |
| 创建组织时&#x200B;**从父级继承共享策略** | 如果允许，则在创建子组织时从父项继承资产共享设置。 资产共享设置包括安全联系人、密码策略和存储策略。 这仅适用于创建时新创建的组织。 它在父项上设置，并影响该父项下子组织的创建。 |
