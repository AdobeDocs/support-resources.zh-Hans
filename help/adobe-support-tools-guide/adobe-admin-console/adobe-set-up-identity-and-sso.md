---
title: 设置身份和单点登录
description: 了解组织系统管理员如何使用Adobe ID、Enterprise ID或Federated ID在Adobe Admin Console中设置用户标识和单点登录(SSO)。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 0c2992946f1cdbbcfb44a2baf37888bd05b2253b
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 1%

---

# 设置身份和单点登录

**应用于：**&#x200B;企业

了解如何在Adobe Admin Console中设置身份。 比较Adobe ID、Enterprise ID和Federated ID，并配置单点登录(SSO)以安全访问Adobe应用程序。

配置身份并设置单点登录(SSO)，以便员工可以使用现有的组织凭据[登录](https://adminconsole.adobe.com/settings/)。

下面是有关如何[设置标识和SSO (YouTube)](https://youtu.be/V57lU4zaSBs)的视频教程。

## 关键术语和概念

### 目录

Admin Console中的目录是一个实体，其中包含用户和身份验证等策略等资源。 这些目录类似于LDAP或Active Directories。

### 标识提供者(IdP)

身份提供者(IdP)是您组织的身份提供者，例如：

- 活动目录
- Microsoft Azure
- Ping
- Okta
- 共同
- 希博莱特

### 涉及的角色

| 角色 | 责任 |
|------|----------------|
| 系统管理员 | 与IdP目录管理器和DNS管理器合作，在Admin Console中设置标识。 |
| DNS管理器 | 更新DNS令牌以验证域所有权。 |
| 标识提供程序(IdP)目录管理器 | 处理IdP门户和关联的连接器。 |

### Adobe ID

由最终用户创建、拥有和管理。 Adobe执行身份验证，由最终用户管理身份。 根据[存储模型](https://helpx.adobe.com/enterprise/using/storage-for-business.html)，用户或企业保留对文件和数据的控制。

对于已更新为企业存储模型的组织，资产和数据由组织控制。 对于尚未更新的组织，个人将拥有并控制Adobe ID资源。

### Enterprise ID

由组织创建、拥有和管理。 Adobe托管Enterprise ID并执行身份验证，但由组织维护Enterprise ID。 管理员创建一个Enterprise ID并将其颁发给用户。 管理员可以通过接管帐户或删除Enterprise ID永久阻止对关联数据的访问来撤销对产品和服务的访问权限。 要了解更多信息，请单击[此处](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html)。

### Federated ID

由组织创建和拥有，并通过联合链接到企业目录。 该组织通过SAML2身份提供程序(IdP)管理凭据并处理单点登录。

以下是推荐使用Federated ID的几种要求和方案：

- 如果您要根据组织的企业目录预配用户。
- 如果要管理用户的身份验证。
- 如果您需要严格控制用户可用的应用程序和服务，

## 在不使用单点登录的情况下设置身份

如果您的组织当前未在其他应用程序上使用SSO，则可以使用Adobe ID或Enterprise ID。

## 使用Adobe ID

Adobe正在将所有组织更新到[企业存储模型](https://helpx.adobe.com/enterprise/using/storage-for-business.html)。 这使您的组织能够更好地控制用户的资产和数据。

开始使用[将用户](https://helpx.adobe.com/cn/enterprise/using/users.html)添加到Admin Console。

## 使用Enterprise ID设置身份

如果您希望在不使用SSO的情况下更好地控制用户数据，则可以设置Enterprise ID目录。 只有管理员可创建Enterprise ID并将其颁发给用户。

有关创建Enterprise ID目录的要求和步骤，请参阅[使用Enterprise ID设置组织](https://helpx.adobe.com/enterprise/using/setup-enterprise-id.html)。

## 设置单点登录身份

您必须使用Federated ID帐户设置用户身份才能使用SSO。

在以下情况下，建议使用Federated ID：

- 您需要对可供用户使用的应用程序和服务保持严格控制。
- 您希望管理用户的身份验证。
- 要根据组织的企业目录配置用户。

## 设置新的SSO集成

您可以使用常用的身份提供程序（如Microsoft Azure AD、Google）或使用其他基于SAML的IdP在您的组织和Adobe产品之间设置SSO。

**Azure AD**（推荐） — [设置SSO并与Azure AD Connector进行用户同步](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html)

**其他SAML IdP** - [使用其他SAML提供程序设置SSO](https://helpx.adobe.com/enterprise/using/create-directory.html)

**Google**（推荐） — [使用Google Connector设置SSO和用户同步](https://helpx.adobe.com/enterprise/using/setup-sso-google.html)

## 管理现有SSO设置

在您的组织和Adobe之间设置SSO后，使用以下内容管理和更改您的设置。

了解如何管理域和目录：

- [管理用户](https://helpx.adobe.com/cn/enterprise/using/users.html)和[组](https://helpx.adobe.com/enterprise/using/user-groups..html)
- [将域链接到目录](https://helpx.adobe.com/enterprise/using/add-domains-directories.html#link-domains-to-directoies)以控制用户对应用、服务和设置的访问
- [管理目录信任](https://helpx.adobe.com/enterprise/using/directory-trust.html)以使用其他组织声明的域

了解如何更改您的身份提供程序：

- [在不中断用户工作的情况下更改IdP](https://helpx.adobe.com/enterprise/using/migrate-authentication-provider.html)
- [跨目录移动域](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#move-domains-across-directories)
- [删除旧版目录用户](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [删除旧/无人认领的域和空目录](https://helpx.adobe.com/enterprise/using/manage-domains-directories.html#delete)

## 错误和常见问题

设置和管理SSO时常见问题和错误的解决方案：

### Azure AD — 常见问题解答和疑难解答

#### 常见问题解答

- [Azure AD连接器常见问题解答](https://helpx.adobe.com/enterprise/using/azure-ad-connector-faq.html)
- [如何删除目录和域](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#Deletedirectoriesandremovedomains)

#### 疑难解答

- [用户拒绝访问](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)
- [同步问题](https://helpx.adobe.com/enterprise/using/sso-setup-azure.html#sync-issues)

### 其他SAML IdP — 常见问题解答和疑难解答

#### 常见问题解答

[SAML集成常见问题解答](https://helpx.adobe.com/enterprise/using/sso-faq.html)

#### 疑难解答

- [常规SSO故障排除](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [“访问被拒绝”错误](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#Error_Access_Denied_logging_in)
- [“另一用户当前已登录”错误](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html#ErrorAnotheruseriscurrentlyloggedin)
- [执行SAML跟踪](https://helpx.adobe.com/enterprise/kb/perform-a-saml-trace.html)

### Google — 常见问题解答

- [Google连接器常见问题解答](https://helpx.adobe.com/enterprise/using/google-federation-faq.html)
- [如何删除目录和域](https://helpx.adobe.com/enterprise/using/setup-sso-google.html#Deletedirectoriesandremovedomains)

## 加入对话

若要进行协作、提问并与其他管理员聊天，请使用[企业版和团队版](https://www.adobe.com/go/entcom)。

## 法律和隐私

- [法律声明](https://helpx.adobe.com/legal/legal-notices.html)
- [联机隐私策略](https://www.adobe.com/cn/privacy.html)
