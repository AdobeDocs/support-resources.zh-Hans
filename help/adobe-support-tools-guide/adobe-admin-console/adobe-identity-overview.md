---
title: 身份概述
description: 了解并选择您组织的身份类型（Federated ID、Enterprise ID、Adobe ID和个人Adobe ID），并在Admin Console中管理用户访问权限。
Feature-set: Experience Cloud Services
Solution: Admin Console
Feature: Admin Console
source-git-commit: c066e95c05f8e8a0953daecda9a220268d325f98
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 5%

---


# 身份概述

适用于企业和团队。

Adobe identity management system可帮助管理员创建和管理用户对应用程序和服务的访问。 Adobe提供这些身份类型或帐户来验证和授权用户。

## Adobe Admin Console上的身份类型

身份类型允许组织对用户的帐户和数据进行不同级别的控制。 您选择的身份模型会对贵组织存储和共享资产的方式产生重大影响。 虽然Federated ID和Enterprise ID模型由组织创建和管理，但Adobe ID由个人创建和管理。

下表将指导您选择最适合贵组织的身份模型。

>[!NOTE]
>如果您的组织尚未更新到Adobe的企业存储模型，并且您仍在使用Adobe ID作为个人，请参阅下面[身份类型表](https://helpx.adobe.com/enterprise/using/identity.html#using-personal-adobe-id)中的描述。

<table>
<thead>
<tr>
<th scope="col">身份类型</th>

<th scope="col" style="text-align: center;">
  <img src="./assets/federated-id.png" alt="Federated ID图标"><br>
  Federated ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/enterprise-id.png" alt="Enterprise ID"><br>
  Enterprise ID
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/adobe-id.png" alt="Adobe ID"><br>
  Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>关键产品/服务</strong></th>
<td>由组织创建、拥有和管理。 该组织管理用户凭据并通过SAML2身份提供程序(IdP)使用单点登录(SSO)。</td>
<td>由组织创建、拥有和管理。 组织保留在已验证域上创建用户帐户的独占权限。</td>
<td>由最终用户创建、拥有和管理。 Adobe执行身份验证，由最终用户管理身份。 根据<a href="https://helpx.adobe.com/enterprise/using/storage-for-business.html">存储模型</a>，用户或企业保留对文件和数据的控制。 Adobe ID帐户在未验证、公共或受信任的域上创建。 请参阅下面注释一节中的第2点。</td>
</tr>
<tr>
<th scope="row"><strong>帐户和数据所有权</strong></th>
<td colspan="2">组织拥有和控制</td>
<td>企业存储由组织拥有，用户存储由用户拥有</td>
</tr>
<tr>
<th scope="row"><strong>安全和监控</strong></th>
<td colspan="2">
  <ul>
    <li>审核日志</li>
    <li>内容日志</li>
    <li>共享限制</li>
    <li>组织的身份验证设置</li>
  </ul>
</td>

<td>
  <ul>
    <li>内容日志</li>
    <li>共享限制</li>
    <li>密码策略</li>
  </ul>
</td>

</tr>
<tr>
<th scope="row"><strong>重置密码</strong></th>
<td colspan="2">不受支持</td>
<td><a href="https://helpx.adobe.com/cn/manage-account/using/change-or-reset-password.html">重置帐户密码</a></td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud企业版和Document Cloud企业版</strong></th>
<td colspan="3">受支持</td>
</tr>
<tr>
<th scope="row"><strong>适用于团队的Creative Cloud和适用于团队的Document Cloud</strong></th>
<td colspan="2">不受支持</td>
<td>受支持</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td colspan="3">受支持</td>
</tr>
<tr>
<th scope="row"><strong>推荐用于</strong></th>
<td>
  <ul>
    <li>已使用SSO或SAML的组织</li>
    <li>现有目录服务（例如Google和Azure AD）</li>
    <li>需要与非Adobe服务轻松集成</li>
    <li>可以演示域的所有权</li>
  </ul>
</td>
<td>
  <ul>
    <li>可以演示域的所有权</li>
    <li>不需要SSO</li>
  </ul>
</td>
<td>
  <ul>
    <li>Creative Cloud团队版</li>
    <li>组织希望使用他们不属于的域</li>
    <li>公共域（例如Hotmail、Gmail）</li>
    <li>访问Adobe Experience Manager Mobile等应用程序</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>快速入门</strong></th>
<td><a href="https://helpx.adobe.com/cn/enterprise/using/set-up-identity.html">设置身份</a></td>
<td><a href="https://helpx.adobe.com/enterprise/using/add-domains-directories.html#claim-domains">声明域</a></td>
<td><a href="https://helpx.adobe.com/enterprise/using/users.html#add-users">添加用户</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. Creative Cloud团队的密码策略与个人Creative Cloud的密码策略相同。
>1. Adobe ID用户使用其Adobe ID凭据或其所属组织的身份验证模型（SSO、2FA等）进行身份验证。 在这种情况下，用户将被重定向到所属组织的SSO页面。 验证后，用户可能需要[选择企业个人资料](https://helpx.adobe.com/enterprise/kb/enterprise-id-faq.html#choose-profile)。

## 使用个人Adobe ID

Adobe正在更新所有团队和企业客户，以使用Adobe的企业存储模型。 如果您的组织有用户使用个人Adobe ID访问其公司或学校Adobe应用程序和服务，请参阅下表。

### 个人Adobe ID

<table>
<thead>
<tr>
<th scope="col">身份标识类型</th>
</th>
<th scope="col" style="text-align: center;">
  <img src="./assets/personal-adobe-id.png" alt="Adobe ID"><br>
  个人Adobe ID
</th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>关键产品/服务</strong></th>
<td>由最终用户创建、拥有和管理。 Adobe执行身份验证，由最终用户管理身份。</td>
</tr>
<tr>
<th scope="row"><strong>帐户和数据所有权</strong></th>
<td>用户控制</td>
</tr>
<tr>
<th scope="row"><strong>安全和监控</strong></th>
<td>密码策略。 请参阅下面注释部分中的要点1。</td>
</tr>
<tr>
<th scope="row"><strong>重置密码</strong></th>
<td><a href="https://helpx.adobe.com/cn/manage-account/using/change-or-reset-password.html">重置帐户密码。</a>请参阅下面注释部分中的要点2。</td>
</tr>
<tr>
<th scope="row"><strong>Creative Cloud企业版和Document Cloud企业版</strong></th>
<td>受支持</td>
</tr>
<tr>
<th scope="row"><strong>Experience Cloud</strong></th>
<td>受支持</td>
</tr>
<tr>
<th scope="row"><strong>仅适用于/建议用于</strong></th>
<td>
  <ul>
    <li>迁移前加入的企业和团队客户</li>
    <li>Creative Cloud团队版</li>
    <li>希望获得用户手中的控制权</li>
    <li>访问Digital Publishing Suite等应用程序</li>
    <li>用户从组织分离后拥有资产</li>
  </ul>
</td>
</tr>
<tr>
<th scope="row"><strong>快速入门</strong></th>
<td><a href="https://helpx.adobe.com/enterprise/using/users.html#add-users">添加用户</a></td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>1. Creative Cloud团队的密码策略与个人Creative Cloud的密码策略相同。
>1. 对于使用[企业存储](https://helpx.adobe.com/enterprise/using/manage-adobe-storage.html)的企业版Creative Cloud客户，管理员可以将Adobe ID用户添加到Admin Console，但无法将其添加到产品配置文件。 管理员必须将Adobe ID用户迁移到另一种身份类型。
>1. 有一些产品和服务（如&#x200B;**Adobe授权网站）仅支持** Adobe ID。

## 更多此类内容

- [设置标识](https://helpx.adobe.com/cn/enterprise/using/set-up-identity.html)
- [切换用户标识](https://helpx.adobe.com/enterprise/using/switch-user-identity.html)
- [Admin Console概述](https://helpx.adobe.com/enterprise/using/admin-console-overview.html)
- [教育常见问题解答](https://helpx.adobe.com/enterprise/using/education-faq.html)
- [添加和管理用户](https://helpx.adobe.com/cn/enterprise/using/users.html)