---
title: 管理管理员
description: Adobe客户如何在Global Admin Console中设置和管理管理员，以控制用户访问权限、产品许可证和组织资源。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 7e5c601a5edd2558d16bfb7b2d508bcf8f976f51
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 2%

---


# 管理管理员

*适用于企业。*

探索全局管理员功能，了解如何将用户、产品许可证和组的管理委派给每个组织的管理员，并将这些委派给管理员。

在Global Admin Console中，您可以选择组织并导航到&#x200B;**[!UICONTROL 管理员]**&#x200B;选项卡以添加、编辑或删除管理员权限。 若要了解详细信息，请参阅[采用全局管理](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html)。 前往[Global Admin Console](https://global-admin-console.adobe.com/)登录。


Global Admin Console引入了一个称为全局管理员的角色。 此角色不同于系统管理员，允许您执行以下操作：

- 查看您在所有添加到Adobe层级的Admin Console中的Global Admin Console投资总额的全球情况。
- 在多个Admin Console中监控Adobe许可证和资源分配及使用情况。
- 创建管理控制台或组织。
- 将产品许可证从根或父Admin Console分配到位于层次结构下方的子Admin Console。
- 维护日常操作，同时系统管理员继续管理他们自己的Admin Console。 例如，全局管理员可以将产品分配给子Admin Console，但不能将其分配给用户。 系统管理员将获得其Admin Console中的名额，并将产品分配给其用户。
- （可选）将组织策略应用到层次结构中的任何Admin Console。

## 基本管理任务

Global Admin Console设计用于多个组织和Admin Console。 下表概述了各种功能以及完成这些功能的位置 — Admin Console或Global Admin Console。

<table>
  <tr>
    <th colspan="2">任务</th>
    <th>Global Admin Console</th>
    <th>Admin Console</th>
  </tr>

<tr>
    <td colspan="2">创建、重新父代和删除子组织</td>
    <td align="center">是</td>
    <td align="center">否</td>
  </tr>

<tr>
    <td colspan="2">使用多个组织</td>
    <td align="center">是</td>
    <td align="center">否</td>
  </tr>

<tr>
    <td rowspan="2" valign="middle">管理管理员</td>
    <td>对于一个或多个组织</td>
    <td align="center">是</td>
    <td align="center">否</td>
  </tr>

<tr>
    <td>对于一个组织</td>
    <td align="center">是</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">管理产品配置文件和用户组</td>
    <td align="center">是</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">定义和管理策略</td>
    <td align="center">是</td>
    <td align="center">否</td>
  </tr>

<tr>
    <td colspan="2">跨组织分配产品</td>
    <td align="center">是</td>
    <td align="center">否</td>
  </tr>

<tr>
    <td colspan="2">将产品分配给用户</td>
    <td align="center">否</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">管理用户</td>
    <td align="center">否</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">管理包</td>
    <td align="center">否</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">设置域和目录</td>
    <td align="center">否</td>
    <td align="center">是</td>
  </tr>

<tr>
    <td colspan="2">管理企业存储和加密</td>
    <td align="center">否</td>
    <td align="center">是</td>
  </tr>
</table>

## 管理管理员

您可以创建一个灵活的管理层次结构，以实现对Adobe产品访问和使用的精细管理。 与Adobe Admin Console类似，Global Admin Console允许您添加系统管理员、产品管理员、产品配置文件管理员、用户组管理员、部署管理员、支持管理员和存储管理员。 这些管理员可以在他们作为管理员的组织中执行各自的管理任务。 除了这些角色之外，全局管理还新增了两个角色：全局管理员和全局查看器。

全局管理员是一个可传递的角色。 将用户设为组织的全局管理员会自动将该用户直接或间接设为该组织所有子项的全局管理员。 此外，如果在组织层次结构中创建新组织，则该组织任何父级的所有全局管理员都将立即成为新创建组织的全局管理员。

以下是全局管理员角色的功能：

- 创建和删除子组织
- 设置和编辑策略
- 设置和修改管理角色
- 在子组织中添加和删除产品
- 设置或更改子组织的资源分配
- 管理产品配置文件和用户组

以下是“全局查看器”角色的功能：

- 查看组织和子组织中的用户组、产品、产品配置文件、管理员、策略集和资源列表。

## 分布式管理

通过管理管理员，全局管理员可以将用户、产品许可证和组的管理委派给每个组织的管理员，并将这些委派给管理员。 由全局管理员添加到组织的管理员可以灵活地管理组织，而无需了解其他组织的管理。 因此，全局管理员可以委托管理资源和用户，并将这些资源和用户上的数据隔离。

全局管理员可以创建组织，将产品和存储等资源分发给这些组织，管理身份设置，以及创建和应用组织策略模板。 由全局管理员添加到组织的系统管理员可以将产品分配给用户、载入用户、创建和管理产品配置文件，以及在该组织内执行其他管理任务。

## 添加管理员

1. 在[Global Admin Console](https://global-admin-console.adobe.com/)中，选择要编辑的组织，然后导航到&#x200B;**[!UICONTROL 管理员]**&#x200B;选项卡。

1. 选择&#x200B;**[!UICONTROL 添加管理员]**。

   ![全局管理控制台添加管理员](../assets/global-admin-console-add-admin.png)

1. 在&#x200B;**[!UICONTROL 添加管理员]**&#x200B;对话框中，输入&#x200B;**[!UICONTROL 用户详细信息]**：电子邮件、名字、姓氏、帐户类型和国家/地区代码。

   如果您尝试将现有用户添加为管理员，请选择与现有用户相同的帐户类型，否则添加操作将失败。

   > [!N注意]
   > 
   > 对于可以添加的帐户类型，组织可以有限制。 这些参数可以基于[策略](https://helpx.adobe.com/enterprise/global-admin-console/update-policies.html)或组织的其他配置参数。 组织不允许同时添加AdobeID用户和业务ID用户。 通常，组织中不应同时存在这两种类型的用户，但根据设置规则的顺序，可能会存在某些特定帐户类型的用户，这些用户会提前应用策略或规则。

1. 从&#x200B;**[!UICONTROL 管理员权限]**&#x200B;部分中选择一个或多个管理员角色。

   对于产品管理员、产品配置文件管理员和用户组管理员等角色，请分别选择特定的产品、配置文件和组。

   ![全局管理控制台添加管理员](../assets/global-admin-console-add-admin-detail.png)

1. 选择&#x200B;**[!UICONTROL 保存]**。

1. 编辑组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**，然后选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

添加管理员角色后，用户会收到电子邮件通知，告知其角色发生了更改。

添加管理员后，这些用户会收到一封电子邮件，邀请他们接受自己的角色并为其提供指向Admin Console的链接。 如果他们同时被添加为全局管理员和某些其他角色，他们将收到两个邀请，一个邀请到全局管理控制台，一个邀请到Admin Console。

## 编辑管理员

1. 选择要编辑的组织，并导航到&#x200B;**[!UICONTROL 管理员]**&#x200B;选项卡。

1. 选择相关管理员的&#x200B;**[!UICONTROL 更多选项]** (⋮)图标，然后选择&#x200B;**[!UICONTROL 编辑管理员]**。

   ![全局管理控制台编辑管理权限](../assets/global-admin-console-edit-admin-right.png)

1. 更新管理员详细信息，然后选择&#x200B;**[!UICONTROL 保存]**。

1. 在编辑完组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。

每个添加或删除的管理员角色的挂起更改列表中都会显示一个单独的命令。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

## 删除管理员权限

1. 选择要编辑的组织，并导航到&#x200B;**[!UICONTROL 管理员]**&#x200B;选项卡。

1. 选择相关管理员的&#x200B;**[!UICONTROL 更多选项]** (⋮)图标，然后选择&#x200B;**[!UICONTROL 删除管理员权限]**。

   ![全局管理控制台删除管理员权限](../assets/global-admin-console-remove-admin-right.png)

1. 在确认对话框中选择&#x200B;**[!UICONTROL 确定]**。

1. 在编辑完组织后，选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 审阅后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/enterprise/global-admin-console/execute-jobs.html)。

删除管理员后，用户会收到电子邮件通知，告知他们该组织无法访问管理控制台。

