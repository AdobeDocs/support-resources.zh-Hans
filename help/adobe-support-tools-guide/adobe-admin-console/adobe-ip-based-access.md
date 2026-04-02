---
title: 按IP地址限制产品访问
description: 使用基于IP的访问权限来控制用户对Adobe产品的访问权限，并将使用限制为批准的公共IP范围。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 879a936ea110084c03df6003494f88831561d3c2
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 0%

---


# 按IP地址限制产品访问

适用于企业。

使用基于IP的访问权限来控制用户对Adobe产品的访问，并防止从未列出的公共IP地址进行未授权使用。

转到[Admin Console](https://adminconsole.adobe.com/settings/identity)将受信任的公共IP地址添加到基于&#x200B;**IP的访问**&#x200B;允许列表，以安全地使用Adobe应用程序和服务。

## 基于IP的访问的优点

基于IP的访问控制使用IP地址允许列表来限制从随机公共IP地址使用Adobe产品。 基于IP的访问适用于您的Adobe Admin Console中的所有目录和相关产品。

您可以将受信任的公共IP添加到&#x200B;**允许的IP地址**&#x200B;列表，以阻止用户：

- 从位于允许的IP范围之外的公共IP访问产品
- 从允许IP范围外的公共IP登录到Adobe [用户配置文件](https://helpx.adobe.com/enterprise/using/manage-adobe-profiles.html)
- 在允许的IP范围之外切换Web应用程序上的用户配置文件

  ![导出组织结构](./assets/ip-based-access.avif)

## 启用基于IP的访问

### 重要注意事项

>[!I重要注意事项]
>
>- 管理员必须首先添加自己的公共IP地址，然后才添加其他IP范围。 否则，您可能会遇到错误。
>- 基于IP的访问不适用于私有IP地址。

您最多只能以CIDR格式添加150个不同的公共IP范围。

请按照以下步骤在Adobe Admin Console中启用基于IP的访问：

1. 转到&#x200B;**[!UICONTROL Adobe Admin Console设置](https://adminconsole.adobe.com/settings/identity)**&#x200B;部分。
2. 在选择菜单中选择并展开&#x200B;**[!UICONTROL 隐私和安全性]**，然后选择&#x200B;**[!UICONTROL 身份验证设置]**。
3. 在基于&#x200B;**[!UICONTROL IP的访问]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 添加IP地址]**&#x200B;按钮。
4. 在&#x200B;**[!UICONTROL 添加IP地址]**&#x200B;窗口中：
   - 输入公共IP地址或CIDR块以添加到中。
   - 请使用逗号分隔多个IP地址。
   - 选择&#x200B;**[!UICONTROL 保存]**。

   我们当前仅支持IPv4格式。 下面是一些示例：
   - IP v4地址： 1.3.4.6
   - IP v4子网地址： 1.2.0.0/24

您的IP地址会在几分钟内添加。 关联的用户在下次尝试登录或切换允许的公共IP地址以外的配置文件时，将会看到该限制。 我们建议您将此更改提前通知您的用户。

通过选择每个条目旁边的编辑或删除选项，可以编辑或删除任何列出的IP地址。

>[!NOTE]
>
>- 启用基于IP的访问时，**不会发生强制注销**。 只有在用户登录或在Web上切换配置文件时尝试选择受限配置文件时，用户才会受到影响。
>- 如果您使用安全的Web网关，请确保所有流量都通过该网关路由。 查看[域列表，以便Adobe应用和服务能够正常工作](https://helpx.adobe.com/enterprise/kb/network-endpoints.html)。
>- 如果您由于输入的IP地址无效而被锁定在Admin Console之外，请联系[Adobe客户关怀团队](https://helpx.adobe.com/enterprise/using/support-for-enterprise.html)。

## 加入对话

若要进行协作、提问并与其他管理员聊天，请访问我们的[企业和Teams社区](https://www.adobe.com/go/entcom)。
