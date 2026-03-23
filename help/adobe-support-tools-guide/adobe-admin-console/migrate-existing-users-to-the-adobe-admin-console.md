---
title: 将现有用户迁移到Adobe Admin Console
description: 面向使用Adobe订阅许可证并需要将Admin Console中的现有用户迁移到其他购买计划或许可证类型的组织的指南。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: 42ab19551ba5c70712245236ffc7daf687486fb2
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---

# 将现有用户迁移到Adobe Admin Console

适用于企业和团队。

本文档适用于通过企业定期许可协议(Creative Cloud)或Value Incentive Plan (VIP)订阅拥有现有ETLA、Document Cloud和Acrobat许可证，并且正在迁移到其他购买计划或许可证类型的组织。

>[!NOTE]
>
>如果您在北美洲，并且需要客户经理的帮助来续订您的年度Adobe VIP合同，请发送电子邮件至&#x200B;**renewalhelp@adobe.com**，我们将会很快与您联系。

要帮助避免最终用户产品访问中断，请在现有VIP订阅期限结束之前在Adobe Admin Console中分配许可证。

* 对于ETLA客户，允许至少30天的产品重叠。 在周年日期之前完成迁移，以便用户保留对Adobe应用程序和服务的访问权限。 有关ETLA合同到期详细信息，请参阅[ETLA合同的自动到期阶段](https://helpx.adobe.com/cn/enterprise/using/contract-expiry.html)。
* 对于VIP客户，请在周年日期之前购买许可证，并在您当前VIP期限的续订窗口关闭之前分配许可证。
* CLP或TLP客户可以使用[许可](https://helpx.adobe.com/cn/enterprise/using/licensing.html)中的迁移说明从序列化Acrobat或Creative Suite迁移到命名用户许可证。

>[!NOTE]
>
>如果贵组织的许可证类型发生更改，最终用户必须注销任何Adobe产品或服务，然后使用相同的凭据重新登录。
>
>对于Photoshop、Acrobat和Illustrator等桌面产品，请使用“帮助”菜单中的“注销”和“登录”选项。 在Adobe.com上，使用右上角的图标注销，然后重新登录。

## 快速许可证分配（VIP到VIP）

通过VIP为企业或Acrobat （适用于企业）购买Creative Cloud的当前VIP成员可以在续订窗口期间使用快速许可证分配快速分配许可证。 符合条件的客户符合以下条件。

* 产品是相同的

   1. 续订窗口打开（VIP协议周年日期之前或之后30天）。
   2. 订单上的企业产品是相当于当前术语中团队版本的新SKU。
   3. 企业许可证订购数量大于或等于现有的团队许可证数量。

* 产品价值更高

   1. 续订窗口打开。
   2. 订单上的企业产品是新的SKU，与当前术语中的团队产品相比，这些产品的价值更高。
   3. 企业许可证订购数量大于或等于现有的团队许可证数量。

* 在以下情况下，快速许可证分配不可用

   * 订单上的企业许可证数量少于现有的团队许可证数量。
   * 订购的是价值较高的企业产品，但订购的企业许可数量小于现有的团队许可数量。
   * 无论数量如何，订单都会混合团队和企业产品。
   * 客户在续订期间之前已购买团队和企业产品。
   * 企业续订SKU用于新的企业订单。
   * 企业产品订单适用于其他VIP协议编号。
   * 当前的团队产品包括没有企业版本的项目。

Adobe处理您的企业采购订单后，您会收到一封包含相关说明的确认电子邮件，其中包括必须在用户失去访问权限之前将其从团队许可证转移到Admin Console中的企业许可证的日期。

在Admin Console中，系统会提示您使用“快速许可证分配”来分配许可证：

1. 确认分配的许可证数量。

   ![转移许可证](assets/migrate-transfer-licenses.png)

2. 确认正在取消分配的团队产品许可证与正在分配的企业许可证相匹配。

3. 该流程完成后，您将收到一封电子邮件。

   ![许可证分配确认](assets/migrate-license-assignment.png)

在Admin Console中下载[结果报告](https://helpx.adobe.com/cn/enterprise/using/users.html#main-pars_header_1346350355)以确认已分配所有许可证。 如果您在确认电子邮件中的日期之前完成，最终用户将不会遇到服务中断。

安排Adobe入门培训专家（如果没有）的1:1入门培训通话，了解有关Admin Console的更多信息，包括[管理角色](https://helpx.adobe.com/cn/enterprise/using/admin-roles.html)和[身份](https://helpx.adobe.com/cn/enterprise/using/identity.html)。

>[!NOTE]
>
>快速许可证分配不会在Team Admin Console中迁移具有待定邀请的用户。

## 批量许可证分配（VIP到VIP）

使用[!DNL Admin Console]中的CSV模板通过批量操作分配许可证。 在下列情况下使用此方法：

* 您是不符合快速许可证分配要求的VIP客户，或者
* 您需要在续订窗口之外分配许可证。

1. 在访问[Adobe Admin Console](https://adminconsole.adobe.com/enterprise)并添加许可证后，转到&#x200B;**[!UICONTROL 用户]** > **[!UICONTROL 用户]**。
2. 单击![用户](assets/migrate-more-options.png)页面右上角的&#x200B;**[!UICONTROL 更多选项菜单]**，然后选择&#x200B;**[!UICONTROL 通过CSV编辑用户详细信息]**。
3. 在&#x200B;**[!UICONTROL 通过CSV编辑用户]**&#x200B;对话框中，单击&#x200B;**[!UICONTROL 下载CSV模板]**&#x200B;并选择&#x200B;**[!UICONTROL 当前用户列表]**。

   ![通过CSV编辑用户](assets/migrate-edit-users-by-csv.png)

   有关下载文件中的字段说明，请参阅[CSV文件格式](https://helpx.adobe.com/cn/enterprise/using/users.html#main-pars_header)。
4. 将许可证分配添加到CSV，然后将更新的文件拖到&#x200B;**[!UICONTROL 通过CSV编辑用户]**&#x200B;对话框中，然后单击&#x200B;**[!UICONTROL 上传]**。 操作完成后，您将收到一封电子邮件。

   ![用户编辑完成](assets/migrate-user-edit-complete.png)

下载[结果报表](https://helpx.adobe.com/cn/enterprise/using/users.html#main-pars_header_1346350355)以验证分配。 然后，安排与Adobe入门培训专家一起上线以了解[管理角色](https://helpx.adobe.com/cn/enterprise/using/admin-roles.html)和[身份](https://helpx.adobe.com/cn/enterprise/using/identity.html)。

## 批量许可证分配（VIP到ETLA）

如果您已订阅VIP并且要将用户移动到ETLA，请使用此批量流程：

1. 登录到[Adobe Admin Console](https://adminconsole.adobe.com/enterprise)并打开包含您的VIP用户的组织。
2. 转到&#x200B;**[!UICONTROL 用户]** > **[!UICONTROL 用户]**。
3. 单击右上角的![更多选项菜单](assets/migrate-more-options.png)，然后选择&#x200B;**[!UICONTROL 将用户列表导出到CSV]**。
4. 打开您想要这些用户访问的ETLA组织。
5. 转到&#x200B;**[!UICONTROL 用户]** > **[!UICONTROL 用户]**。
6. 单击&#x200B;**[!UICONTROL 通过CSV添加用户]**。
7. 单击&#x200B;**[!UICONTROL 下载CSV模板]**，然后从您在步骤3中导出的CSV中添加VIP用户。
8. 上传更新的CSV。

将用户添加到ETLA组织后，您将收到一封电子邮件。

在VIP迁移到ETLA后添加了![个用户](assets/migrate-users-added-vip-etla.png)

下载[结果报表](https://helpx.adobe.com/cn/enterprise/using/users.html#main-pars_header_1346350355)以验证分配。 安排Adobe入门培训专家为[管理员角色](https://helpx.adobe.com/cn/enterprise/using/admin-roles.html)和[身份](https://helpx.adobe.com/cn/enterprise/using/identity.html)上线。

有关批量上传问题，请参阅[批量用户上传疑难解答](https://helpx.adobe.com/cn/enterprise/kb/troubleshoot-bulk-user-csv-upload.html)。

## 批量许可证分配（ETLA到VIP）

如果您已订阅ETLA并且要将用户迁移到VIP：

1. 登录到[Adobe Admin Console](https://adminconsole.adobe.com/enterprise)并打开包含您的ETLA用户的组织。
2. 转到&#x200B;**[!UICONTROL 用户]** > **[!UICONTROL 用户]**。
3. 单击右上角的![更多选项菜单](assets/migrate-more-options.png)，然后选择&#x200B;**[!UICONTROL 将用户列表导出到CSV]**。

   ![导出用户列表菜单](assets/migrate-export-user-list.png)

4. 打开您想要这些用户访问的VIP组织。
5. 转到&#x200B;**[!UICONTROL 用户]** > **[!UICONTROL 用户]**。
6. 单击&#x200B;**[!UICONTROL 通过CSV添加用户]**。
7. 单击&#x200B;**[!UICONTROL 下载CSV模板]**，然后从您在步骤3中导出的CSV中添加ETLA用户。
8. 上传更新的CSV。

将用户添加到VIP组织后，您将收到一封电子邮件。

在ETLA迁移到VIP后添加了![个用户](assets/migrate-users-added-etla-vip.png)

下载[结果报表](https://helpx.adobe.com/cn/enterprise/using/users.html#main-pars_header_1346350355)以验证分配。 安排Adobe入门培训专家为[管理员角色](https://helpx.adobe.com/cn/enterprise/using/admin-roles.html)和[身份](https://helpx.adobe.com/cn/enterprise/using/identity.html)上线。

有关批量上传问题，请参阅[批量用户上传疑难解答](https://helpx.adobe.com/cn/enterprise/kb/troubleshoot-bulk-user-csv-upload.html)。


