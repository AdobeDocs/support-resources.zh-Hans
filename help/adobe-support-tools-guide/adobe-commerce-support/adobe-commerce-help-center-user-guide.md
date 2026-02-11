---
title: 适用于Adobe Commerce的Experience League支持用户指南
description: 了解如何向Experience League支持提交支持工单、提供对帐户的共享访问以及导航Adobe Commerce知识库。
feature: Support, Roles/Permissions, Tools and External Services, Admin Workspace, Iaas, Marketing Tools
feature-set: Commerce
solution: Commerce
source-git-commit: 7c09a33efee7a2e62b47758ab1af37e663776374
workflow-type: tm+mt
source-wordcount: '3275'
ht-degree: 0%

---

# 适用于Adobe Commerce的Experience League支持用户指南

在本指南中，了解如何向[Experience League支持](https://experienceleague.adobe.com/home#support)提交支持票证，并提供对Adobe Commerce帐户的共享访问权限。

>[!NOTE]
>
>Adobe Commerce支持已从Adobe Commerce帮助中心迁移到Experience League。 使用[此处](#what-is-experience-support)描述的Experience League案例表单流程提交支持案例。

>[!NOTE]
>
>目前，要查看您之前在Adobe Commerce帮助中心提交的案例，您必须转到https://support.magento.com/hc/en-us/requests ，因为这些案例尚未迁移到新的支持票证系统。 帮助中心现在为只读；要继续获得对原始问题的支持，您必须向[Experience League支持](https://experienceleague.adobe.com/home#support)提交跟进票证。

>[!NOTE]
>
>Adobe Commerce帮助中心的知识库部分已迁移到Adobe Experience League门户。 在创建支持工单时，将向您推荐相关的知识库文章，以及Adobe Experience League中的其他相关Adobe Commerce文档。

**主要更新：** 2024年7月29日

**[EXPERIENCE LEAGUE支持什么？](#what-is-experience-support)**

**[支持案例](#support-cases)**

* [登录到Experience League支持](#sign-in-experience-support)
* [提交支持案例](#support-case)

   * [Adobe Experience League起始页](#experience-league-start-page)
   * [Adobe Commerce帐户页面](#submit-case-adobe-commerce-account-page)
   * [*请验证您的电子邮件地址*](#verify-email-address-error)

* [跟踪您的支持案例](#track-support-cases)
* [您案例中的备注](#comments-in-your-case)
* [结案](#close-case)
* [重新打开您的案例](#reopen-case)
* [使用Cloud Console提交票证](#cloud-console)
* [Adobe Commerce P1热线](#P1-hotline)
* [Adobe Commerce共同责任运营模式](#shared-responsibility-operational-model)

**[共享访问权限：授予其他用户访问您帐户的权限](#shared-access)**

* [谁可以提供共享访问权限](#who-can-provide-shared-access)
* [提供共享访问](#provide-shared-access)
* [撤销（删除）共享访问权限](#revoke-shared-access)

   * [如何删除通过Cloud项目被授予共享访问权限的用户？](#remove-cloud-shared-access-users)

* [访问共享帐户（切换帐户）](#switch-accounts)
* [共享访问疑难解答](#troubleshooting-shared-access)

**[ADOBE COMMERCE的计费常见问题解答](#billing-faq)**


## Experience League支持什么？ {#what-is-experience-support}

Experience League支持是Adobe的支持门户，符合条件的Adobe Commerce客户可以在这里提交和管理支持工单。 您还可以在该处查看故障排除文章。

## 支持案例 {#support-cases}

Adobe Experience League支持案例管理允许通过案例与支持人员合作，解决在根据合同为所有Adobe产品使用Adobe Commerce等Adobe Commerce产品时遇到的特定问题。

## 登录EXPERIENCE LEAGUE支持 {#sign-in-experience-support}

登录允许您提交、更新和响应工程师有关支持票证的问题。

要登录Adobe Experience League支持，请执行以下步骤：

1. 导航到[experienceleague.adobe.com](https://experienceleague.adobe.com/)。
1. 使用您的Adobe登录凭据登录。

![登录experience-league](/help/adobe-support-tools-guide/assets/experience_league_sign_in.png)

### 提交支持案例 {#support-case}

以帐户所有者或Shared Access用户身份成功登录后，您可以使用Adobe Experience League主页、Adobe Commerce帐户页面和Adobe Commerce Cloud帐户页面提交支持案例。

>[!NOTE]
>
>Adobe Commerce Marketplace团队的支持请求无法通过Experience League提交，因为其支持系统在未与Experience League集成的单独平台上运行。
>
>如果以下陈述属实，您可以提交支持案例：
>
>* 相关组织将在左栏中命名，并在(Commerce)中结束。 您的问题与该组织或与其关联的帐户相关。
>* 您的问题是无法登录Marketplace帐户，或者对于部署扩展有疑问。
>* 您提出的问题不仅仅是为所购买的Marketplace产品申请退款。
>
>对于与发布扩展、在购买过程中遇到问题或在[Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/)中请求退款相关的问题，您必须直接访问https://commercemarketplace.adobe.com/以联系[!DNL Commerce Marketplace]团队。 导航到页面底部，然后单击&#x200B;**[!UICONTROL 联系我们]**，这将打开一个表单以提交Marketplace支持票证。

#### Adobe Experience League起始页 {#experience-league-start-page}

要使用Adobe Experience League的起始页提交新的支持案例，请参阅[使用Experience League创建支持工单](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-customer-support-experience#create-a-support-ticket-with-experience-league)。

>[!INFO]
>
>1. 要提交案例，您必须有权支持相应的产品(例如，Adobe Commerce、Adobe Commerce Intelligence、Adobe Commerce支付服务、Experience Platform等)。 如果您无权获得支持，页面顶部将显示一个栏，告知您您您不是组织中有权获得支持的用户。
>1. 如果您属于多个组织，或者有多个组织具有相似的名称(每个组织都表示该组织订阅的任何其他Adobe产品)，则需要首先从左列（以&#x200B;*[!DNL (Commerce)]*&#x200B;结尾）的下拉菜单中选择相应的组织。
>1. 如果在提交案例时&#x200B;**[!UICONTROL 选择产品]**&#x200B;下拉列表为空，则您可能使用Adobe Commerce合作伙伴帐户。 只有具有支持权利商家的[共享访问权限](#shared-access)的用户才能提交票证。 对于商家问题，请求共享访问权限。 有关合作伙伴问题，请联系spphelp@adobe.com。

>[!NOTE]
>
>在提交案例之前，请确保您选择了正确的组织，并且您选择的组织拥有您请求支持的产品的相应权利。 例如，如果您的问题与Adobe Commerce有关，但您选择了Adobe Commerce Intelligence或Adobe Experience Platform作为产品，并且案例已成功提交，这可能会导致案例的路由错误和响应时间的延迟。
>
>此外，如果在提交案例时选择了错误的组织，您的团队将无法在&#x200B;**[!UICONTROL 我的案例]**&#x200B;下查看适当/正确的组织案例。 Adobe Commerce支持团队无法更改与案例关联的组织；要解决此问题，您必须关闭现有案例，并提交包含提供/选择的相应详细信息的新案例。

>[!NOTE]
>
>如果您在云基础架构&#x200B;**[!DNL Commerce]上使用“**”提交票证，并且组织列出了多个项目，则将提示您选择适当的&#x200B;**[!UICONTROL 项目ID]**。 如果您找不到所需的&#x200B;**[!UICONTROL 项目ID]**，请确保在票证上添加一条注释，指明您正在为其他“项目X”寻求帮助。<br>如果您打算在Managed Services **[!DNL Commerce]”票证上提交“**”，并且在&#x200B;**[!DNL Commerce]上云基础架构**，但在云基础架构&#x200B;**[!DNL Commerce]上看不到**&#x200B;是可用的产品：<br>1。 在&#x200B;**[!UICONTROL 案例标题]**&#x200B;中输入问题的主题。<br>2. 在&#x200B;**[!UICONTROL 案例描述]**&#x200B;中输入问题的描述。<br>3. 输入这两个项目后，将显示下面的&#x200B;**[!UICONTROL 云项目URL]**&#x200B;字段。

>[!IMPORTANT]
>
>如果您在登录experienceleague.adobe.com时无法在组织下拉菜单中看到您的组织，则在请求支持或管理现有支持案例之前，可能需要将您的配置文件与accounts.magento.com同步。
>
>1. 导航到accounts.magento.com ，然后使用您将用于管理Adobe Experience League中的支持案例的相同配置文件（企业、学校或个人）登录。
>1. 成功登录accounts.magento.com配置文件后，请导航回experienceleague.adobe.com并登录。
>1. 从组织下拉菜单中选择您的组织。
>1. 如果贵组织仍未出现，请联系Commerce管理员以获取支持委派权限。 有关其他信息，请参阅[Commerce帐户共享](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-share)帮助文章。

>[!NOTE]
>
>为什么组织/产品很重要
>
>**示例A**：您仅共享了对一家公司的访问权限，该公司拥有两个Adobe产品的权利：Product1和Product2。
>
>1. 由于每个组织代表一种产品，因此您会在下拉列表中看到两个组织，例如OrgA-Product1和OrgB-Product2。
>1. 如果您选择了产品= Product1，但您的问题与Product2有关，则案例将被转接至Product2支持部门，在将案例转接至Product1支持部门时会有所延迟。
>1. 如果您提交了OrgA-Product1的案例，并且希望将来查看该组织的&#x200B;**[!UICONTROL 我的案例]**，那么如果选择OrgA-Product2作为组织，您将不会看到该案例（与Example B相比，您只需选择另一个组织即可）。
>
>**示例B**：您已共享对两家公司的访问权限，并且每家公司只拥有Adobe Commerce的权利。
>
>1. 如果您为OrgA提交了案例，但问题实际影响OrgB，则OrgB的成员将来将无法在&#x200B;**[!UICONTROL 我的案例]**&#x200B;下看到此案例。
>1. 此外，OrgA成员将能够查看&#x200B;**[!UICONTROL 我的案例]**&#x200B;下实际用于OrgB的案例，这可能会导致隐私问题。

>[!NOTE]
>
> 为确保您获得最快、最准确的支持，请在创建支持请求时选择正确的详细信息。 准确的选择有助于将您的案例直接发送到正确的团队，并减少响应时间。
>
>如果贵组织有权使用Adobe Commerce Intelligence/Commerce报表(MBI)，但您需要有关高级报表的帮助，请不要选择&#x200B;**Commerce报表**&#x200B;作为产品。 Commerce报表团队不支持高级报表问题。
>
>如果无法选择其他产品（例如，**[!UICONTROL 选择产品]**&#x200B;下拉列表为空或未显示），则通常是由以下原因之一造成的：
>
>* 您的Commerce授权已过期或处于非活动状态（例如，由于未解决的计费或许可问题）。
>* 对于在云基础架构(PaaS)上的Adobe Commerce上托管的实例，尚未将您添加到云项目。
>
>对于云项目上的Adobe Commerce，请联系您的帐户所有者，并请求将其添加到相应的云项目。 有关详细信息，请参阅[在云基础架构上管理Adobe Commerce的用户访问权限](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/project/user-access)。
>
>在您获得共享访问权限并添加到云项目后：
>
>1. 转到[Adobe支持](https://experienceleague.adobe.com/home?lang=en#support)页面。
>1. 在左侧的组织下拉列表中，选择名称以&#x200B;**(Commerce)**&#x200B;结尾的组织。
>1. 提交相应产品的票证，对于与高级报告具体相关的问题，请勿选择&#x200B;**Commerce报告**。

您必须同时在https://account.adobe.com和https://account.magento.com拥有帐户才能登录Experience League以提交支持案例。 在登录之前，您将无法提交支持案例。

如果您已在https://account.magento.com上拥有帐户，但无法登录，则可能尚未在https://account.adobe.com上注册帐户（自2022年8月起，必须注册）。

要解决此问题：

1. 在https://account.adobe.com上使用与您的广告ID相同的电子邮件地址创建一个帐户。
1. 转到https://account.magento.com ，将您的Adobe ID与MAG ID关联起来。

#### Adobe Commerce帐户页面 {#submit-case-adobe-commerce-account-page}

要使用Adobe Commerce帐户页提交新的支持工单，请执行以下步骤：

1. 登录到您的Adobe Commerce帐户。 请参阅我们的用户指南中的[详细说明](https://experienceleague.adobe.com/docs/commerce-admin/start/commerce-account/commerce-account-create.html?lang=en#create-a-commerce-account)。
1. 单击&#x200B;**支持**&#x200B;选项卡。

   ![magento_account_support_tab](/help/adobe-support-tools-guide/assets/magento_account_support_tab.png){width="800"}

1. 系统会为您加载Adobe Experience League支持页面。
1. 从左侧菜单中选择&#x200B;**[!UICONTROL 打开票证]**。
1. 填写[字段](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-support-ticket-contact-reason-descriptions)。
1. 单击&#x200B;**提交**。

#### *请在Adobe Commerce帐户页面上验证您的电子邮件地址*&#x200B;错误 {#verify-email-address-error}

如果您收到“请验证您的电子邮件地址”错误(类似于[Adobe Commerce帐户](https://account.magento.com/)页面上的以下错误)，您将无法提交支持票证。

![验证电子邮件地址错误](/help/adobe-support-tools-guide/assets/Verify_Email_Address_Error.png)


### 跟踪您的Commerce支持案例 {#track-support-case}

您的支持案例包括：

* 已经亲自提交了。
* 已通过CC（抄送）添加到作为观察者。

>[!NOTE]
>
>如果您有在Commerce之外提交的其他Adobe产品支持案例，则无法从同一屏幕跟踪这些工单 — 您必须先切换到与产品权利关联的组织。
>例如，您之前选择了以“(Commerce)”结尾的组织来跟踪您的Commerce案例，同时您还具有AEP支持案例 — 这些案例不会显示在此处。

#### 查看您的案例

单击左侧菜单中的&#x200B;**[!UICONTROL 我的案例]**，可以查看您个人提交的Commerce案例。 确保您选择了以“(Commerce)”结尾的正确组织。

![查看支持案例](/help/adobe-support-tools-guide/assets/view_support_cases.png)

#### 从Adobe Commerce帮助中心查看历史案例

详细了解如何从Adobe Commerce知识库的&#x200B;**停用Adobe Commerce帮助中心**&#x200B;中的Adobe Commerce帮助中心[查看您的历史案例](https://experienceleague.adobe.com/zh-hans/docs/commerce-knowledge-base/kb/announcements/news/decommissioning-of-adobe-commerce-help-center)。

#### 查看您的观察案例

通过单击左侧菜单中的&#x200B;*我的组织的案例*，您可以查看您作为观察者&#x200B;**[!UICONTROL 添加的Commerce案例]**。

<!-- TODO: Add image here -->


#### 搜索案例

若要查找案例，请在&#x200B;*[!UICONTROL 搜索]*&#x200B;字段中键入搜索查询，然后在键盘上按&#x200B;*Enter*。

![搜索案例](/help/adobe-support-tools-guide/assets/search_cases.png)

#### 升级您的案例

如果您认为某个案例需要进一步关注，并且我们的初始响应时间已过，您可以升级该案例。 要做到这一点，

1. 单击屏幕右侧&#x200B;**[!UICONTROL 案例详细信息]**&#x200B;面板右下角的&#x200B;*[!UICONTROL 呈报到管理]*。

   ![升级至管理](/help/adobe-support-tools-guide/assets/escalate_to_management.png)

1. 单击后，将显示一个弹出表单。 填写表单，然后单击&#x200B;**[!UICONTROL 上报]**。

   ![确认提升](/help/adobe-support-tools-guide/assets/confirm_escalation.png)

   *升级原因可能包括*：代理沟通技能、代理技术知识、等待回叫/更新、问题紧迫性更改、解决未达到预期或解决时间。

#### 在支持案例中添加观察程序

您可以添加观察者来支持组织成员提交的案例。 当提交新案例或更新现有案例时，观察者将收到电子邮件通知。

1. 要将观察程序添加到现有案例，请打开案例，然后单击屏幕右侧“案例详细信息”面板中“观察程序”旁边的铅笔图标。

   ![添加观察者](/help/adobe-support-tools-guide/assets/add_watchers.png)

1. 单击铅笔后，您可以在列表中添加或删除观察者。

   ![更新观察者](/help/adobe-support-tools-guide/assets/update_watchers.png)

>[!NOTE]
>
>有关如何为案例添加和删除观察者的详细信息，请参阅[添加和删除观察者、关闭和重新打开票证视频](https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/help-and-support/add-remove-watchers-close-reopen-support-ticket)。

### 您案例中的备注 {#comments-in-your-case}

您案例中的注释包含您或Adobe Commerce支持团队编写的所有注释。 注释按最新（顶部）到最早（底部）顺序显示。
要添加评论，请执行以下步骤：

1. 滚动到票证的底部。
1. 将您的评论写入&#x200B;**[!UICONTROL 评论]**&#x200B;字段，然后单击&#x200B;**[!UICONTROL 添加评论]**。

![添加备注](/help/adobe-support-tools-guide/assets/add_comments.png)

### 结案 {#close-case}

要关闭案例，请单击&#x200B;**[!UICONTROL 案例详细信息]**&#x200B;面板右下角的&#x200B;*[!UICONTROL 关闭案例]*。

![close-case](/help/adobe-support-tools-guide/assets/close_case.png)

>[!NOTE]
>
>有关如何关闭案例的更多信息，请参阅[添加和删除观察者、关闭和重新打开票证视频](https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/help-and-support/add-remove-watchers-close-reopen-support-ticket)。

### 重新打开您的案例 {#reopen-case}

>[!NOTE]
>
>**您只能在案例关闭后的14天内重新打开案例。**&#x200B;如果您已超过案例关闭的14天，但仍想请求有关问题的帮助，则需要打开一个新案例。<br>有关关闭和重新打开案例的详细信息，请参阅[添加和删除观察者、关闭和重新打开票证视频](https://experienceleague.adobe.com/en/docs/commerce-learn/tutorials/help-and-support/add-remove-watchers-close-reopen-support-ticket)。

>[!NOTE]
>
>无法通过响应来自已关闭票证的电子邮件通知来重新打开案例。 要重新打开案例，请确保帐户所有者已授予您[共享访问权限](https://experienceleague.adobe.com/zh-hans/docs/experience-cloud-kcs/kbarticles/ka-26164)。

### 使用Cloud Console提交票证 {#cloud-console}

要使用Cloud Console提交新的支持工单，请执行以下步骤：

1. 登录到[云控制台](https://console.adobecommerce.com)。
1. 在用户菜单中选择&#x200B;**[!UICONTROL 支持]**。
1. 加载&#x200B;**[!UICONTROL 我的票证]**&#x200B;页面。
1. 单击右上角的&#x200B;**[!UICONTROL 提交票证]**。
1. 填写[字段](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-support-ticket-contact-reason-descriptions)。
1. 单击&#x200B;**[!UICONTROL 提交]**。

### Adobe Commerce P1热线 {#P1-hotline}

[Adobe Commerce P1热线](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/adobe-commerce-p1-notification-hotline.html)文章提供了Adobe Commerce在P1事件期间寻求帮助时的P1热线号码，并解释了要提供的信息。

### Adobe Commerce共同责任运营模式 {#shared-responsibility-operational-model}

请参阅关于[Adobe Commerce分担责任运营模型](https://experienceleague.adobe.com/en/docs/commerce-operations/security-and-compliance/shared-responsibility#operational-responsibilities-summary)的文章，
旨在厘清我们专业基础设施服务的运营责任。

### 打开跟进票证 {#follow-up}

打开跟进票证将确保原始问题链接到跟进票证以实现连续性。

要打开跟进票证，请单击您要创建跟进的票证底部的“*创建跟进*”链接。

## 共享访问：授予其他用户访问您帐户的权限 {#shared-access}

您可以为其他Adobe Commerce帐户持有人授予对您帐户的有限访问权限。 特别是，使用&#x200B;**共享访问**&#x200B;功能，您可以为受信任的员工和服务提供商提供使用帮助中心帐户的权限，以便他们可以使用您的支持票证。

您可以使用位于[https://account.magento.com](https://account.magento.com/)的Adobe Commerce帐户页提供和管理共享访问权限。

### 谁可以提供共享访问权限 {#who-can-provide-shared-access}

只有具有相应权限的帐户所有者（主帐户所有者）才能为其他用户提供共享访问权限。

管理用户及其访问权限是客户的责任，在共享访问方面尤其如此。 因此，Adobe Commerce支持团队无法代表客户提供对Adobe Commerce帐户的共享访问权限。 建议客户使用[Adobe Commerce帐户页面](https://account.magento.com/)自行添加具有共享访问权限的用户。

已被提供共享访问权限的用户不能向其他用户转移或授予此类访问权限。

### 提供共享访问 {#provide-shared-access}

有关设置共享帐户的详细步骤，请参阅Adobe Commerce快速入门指南的[共享Commerce帐户](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-share)部分。

>[!NOTE]
>
>在授予用户共享访问权限之前，该用户必须具有现有帐户 — 有关更多详细信息，请参阅[创建Commerce帐户](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account)。

为新用户提供共享访问后，相关信息可在您的Adobe Commerce帐户页面的&#x200B;**共享访问** > **管理权限**&#x200B;中获得。

>[!NOTE]
>
>共享访问不会自动授予对Commerce Cloud Console的访问权限。 您需要[单独将用户添加到云项目](https://experienceleague.adobe.com/en/docs/commerce-on-cloud/user-guide/project/user-access#add-a-user-to-the-project)。

![magento-account-shared-manage-permissions](/help/adobe-support-tools-guide/assets/magento_account_shared_manage_permissions.png)

### 撤销（删除）共享访问权限 {#revoke-shared-access}

1. 在[https://account.magento.com](https://account.magento.com/)登录到您的Adobe Commerce帐户。
1. 在左侧面板中的“共享访问”下，选择&#x200B;**管理权限。**
1. 找到要撤销其共享访问权限的用户，然后单击用户行（![操作](/help/adobe-support-tools-guide/assets/remove_icon.png){width="25"}列）中的&#x200B;**删除图标**。
1. 单击&#x200B;**删除用户**&#x200B;以撤销访问权限，或者单击X在顶角取消撤销。

   ![revoke_shared_access](/help/adobe-support-tools-guide/assets/revoke_shared_access.png){width="800"}

   您还可以使用&#x200B;**编辑**&#x200B;菜单撤销共享访问权限：

1. 在[https://account.magento.com](https://account.magento.com/)登录到您的Adobe Commerce帐户。
1. 在左侧面板中的“共享访问”下，选择&#x200B;**管理权限。**
1. 找到要撤销其共享访问权限的用户，然后单击用户行（**操作**&#x200B;列）中的&#x200B;**编辑**。
1. 单击页面底部的&#x200B;**删除此用户**。
1. 在确认弹出窗口中，单击&#x200B;**删除用户**&#x200B;以撤销访问权限，或者单击顶角的X以取消撤销。

### 如何删除通过Cloud项目被授予共享访问权限的用户？ {#remove-cloud-shared-access-users}

<u>受影响的产品和版本</u>

* Adobe Commerce Cloud（所有版本）

<u>原因</u>

如果您拥有Adobe Commerce Cloud项目并且在该项目中添加了用户，则他们可能已自动获得对项目所有者的图像ID的共享访问权限。 这通常显示在&#x200B;**[!UICONTROL 共享名称]**&#x200B;列中，显示来自MAG *XYZ[的]*&#x200B;云共享访问。

>[!NOTE]
>
>如果缺少DELETE链接，则表示通过Commerce Cloud自动授予共享访问权限。

<u>解决方案</u>

如果未在此页面&#x200B;*上添加/给定[，则无法从MAG]* XYZ[中删除共享名称为](https://account.magento.com/grantor/manage/)Cloud Shared Access的共享访问用户列表。 保留它们是为了提供信息/进行审核。

但是，一旦您撤销了这些共享访问用户的权限，他们将不再拥有该访问权限。

1. 在[https://account.magento.com](https://account.magento.com/)登录到您的Adobe Commerce帐户。
1. 在左侧面板的&#x200B;*[!UICONTROL 共享访问]*&#x200B;下，选择&#x200B;**[!UICONTROL 管理权限]**。
1. 找到要撤销其共享访问权限的用户，然后单击用户行（**[!UICONTROL 操作]**&#x200B;列）中的&#x200B;*[!UICONTROL 编辑]*。
1. 取消选中&#x200B;*[!UICONTROL 授予帐户权限]*&#x200B;下的所有资源。

![grant-account-permissions-image](/help/adobe-support-tools-guide/assets/help-center-user-guide-grant-account-permissions-image.png){width="800"}

有关更多信息，请参阅我们的Commerce on Cloud Infrastructure指南上的[管理用户访问权限](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html#manage-users-from-the-project-web-interface)文档。

### 访问您的共享帐户（切换帐户） {#switch-accounts}

>[!NOTE]
>
>提交Adobe Commerce的票证不需要执行此步骤。
>有关提交Adobe Commerce票证的演示，[请观看此视频](https://experienceleague.adobe.com/en/playlists/support-requests)。

要使用为您提供的共享访问权限，请执行以下步骤：

1. 在[https://account.magento.com](https://account.magento.com/)登录到您的Adobe Commerce帐户。
1. 单击&#x200B;**切换帐户**&#x200B;菜单并选择帐户。

   ![magento-account-shared-switch](/help/adobe-support-tools-guide/assets/magento_account_shared_switch.png){width="800"}

要了解您当前使用哪个帐户（您自己的本机帐户或共享访问权限），请参阅&#x200B;**切换帐户**&#x200B;菜单：该菜单显示活动帐户。

### 共享访问疑难解答 {#troubleshooting-shared-access}

请参阅我们的支持知识库中的[共享访问疑难解答文章](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)。


