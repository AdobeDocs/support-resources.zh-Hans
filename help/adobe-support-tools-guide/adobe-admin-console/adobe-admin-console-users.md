---
title: Adobe Admin Console用户
description: 规划在Adobe Admin Console上管理用户的策略 — 添加管理员和最终用户，选择用户管理方法并分配许可证。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
source-git-commit: d92f4190b68a480409f4126a877de3469ed836f0
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 3%

---

# Adobe Admin Console用户

适用于企业和团队。

面对这些问题吗？ 选择问题以查看解决方案。

- [管理管理员角色](https://helpx.adobe.com/enterprise/using/admin-roles.html)
- [下载安装问题](https://helpx.adobe.com/download-install.html)
- [重置Enterprise ID用户密码](https://helpx.adobe.com/enterprise/kb/enterprise-id-faq.html#faq)
- [解决Federated ID错误](https://helpx.adobe.com/enterprise/kb/tshoot-fed-id.html)
- [删除用户或恢复已删除的用户](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)

**Adobe Admin Console — 用户** — [在YouTube上观看](https://youtu.be/w8b36YX2TEM)

## 为何要将用户添加到Adobe Admin Console

>[!NOTE]
>
>作为Adobe Admin Console的管理员，在您选择了[标识类型](https://helpx.adobe.com/cn/enterprise/using/identity.html)和[设置标识](https://helpx.adobe.com/cn/enterprise/using/set-up-identity.html)后，您的下一个任务是将用户添加到Admin Console。

Adobe enterprise和teams大致定义了两种类型的用户：

### 管理员（管理员）

企业管理员或团队管理员在Admin Console上执行管理任务。 您可以添加管理员以定义灵活的管理层次结构，从而更精细地管理Adobe产品访问、使用和其他管理任务。

必须将所有管理员添加到Admin Console。 添加管理员时，管理权限基于其[管理角色](https://helpx.adobe.com/enterprise/using/admin-roles.html)。

### 最终用户

最终用户是贵组织或机构中使用Adobe产品和服务的用户，这些产品和服务是贵组织或机构与Adobe签署的协议中所包含的内容。

## 决定您的用户管理策略

根据您的要求，您可以&#x200B;*单独添加、删除或更新用户*，或者使用可用的&#x200B;*批量上传方法*&#x200B;之一。 使用以下矩阵作为规划用户管理的指南。

>[!NOTE]
>
>如果您是新的Adobe企业或团队客户，我们建议您先浏览下表，然后再开始在Admin Console上管理您的用户。 现有客户可以使用此项，尤其是如果他们计划从一种标识类型迁移到另一种标识类型时（请参阅[编辑标识类型](https://helpx.adobe.com/enterprise/using/switch-user-identity.html)）。

<table>
<thead>
<tr>
<th scope="col"></th>
<th scope="col"><strong>单独(Admin Console)</strong></th>
<th scope="col"><strong>CSV批量上传(Admin Console)</strong></th>
<th scope="col"><strong>Azure/Google连接器</strong></th>
<th scope="col"><strong>用户同步工具</strong></th>
<th scope="col"><strong>用户管理REST API</strong></th>
</tr>
</thead>
<tbody>
<tr>
<th scope="row"><strong>应用于</strong></th>
<td colspan="2">Adobe团队和企业客户</td>
<td colspan="3">Adobe企业客户</td>
</tr>
<tr>
<th scope="row"><strong>描述</strong></th>
<td>在Admin Console中单独管理用户。</td>
<td>在Admin Console中使用CSV文件上传功能管理用户。</td>
<td>基于现有Azure AD门户或Google联盟管理用户（和组）。</td>
<td colspan="2">根据您组织的LDAP管理用户（和组）。</td>
</tr>
<tr>
<th scope="row"><strong>添加用户</strong></th>
<td><strong>Admin Console</strong>中的<strong>用户</strong>选项卡。 <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#add-users">了解详情</a>。</td>
<td>在<strong>Admin Console</strong>中使用<strong>通过CSV添加用户</strong>。 <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">阅读更多信息</a>。<em>（使用默认CSV模板。）</em></td>
<td>在<a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a>或<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>中添加用户。 或通过<strong>Admin Console</strong>。</td>
<td colspan="2">应将用户添加到您组织的LDAP中。</td>
</tr>
<tr>
<th scope="row"><strong>删除用户</strong></th>
<td>在<strong>Admin Console</strong>中选择并移除用户。 <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#remove-users">了解详情</a>。</td>
<td>在<strong>Admin Console</strong>的<strong>用户</strong>选项卡中选择<strong>通过CSV删除用户</strong>。 <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#remove-users">阅读更多信息</a>。<em>（使用默认CSV模板。）</em></td>
<td>必须在<a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a>或<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>中删除用户。</td>
<td colspan="2">确保用户信息同步。 <strong>警告：</strong>从Admin Console中删除不在您组织的LDAP中的用户。</td>
</tr>
<tr>
<th scope="row"><strong>编辑用户详细信息</strong></th>
<td>选择该用户，然后在Admin Console中<strong>编辑用户详细信息</strong>。 <a href="https://helpx.adobe.com/enterprise/using/manage-users-individually.html#edit-user-details">了解详情</a>。</td>
<td>在<strong>Admin Console</strong>的<strong>用户</strong>选项卡中选择<strong>通过CSV编辑用户详细信息</strong>。 <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html#edit-user-details">阅读更多信息</a>。<em>（使用默认CSV模板。）</em></td>
<td>必须在<a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">Azure</a>或<a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">Google</a>中更改所有用户信息。</td>
<td colspan="2">确保用户信息同步。</td>
</tr>
<tr>
<th scope="row"><strong>支持的身份类型</strong></th>
<td colspan="2">全部</td>
<td>Federated ID</td>
<td colspan="2">Federated ID和Enterprise ID</td>
</tr>
<tr>
<th scope="row"><strong>最大 每个操作的更新</strong></th>
<td>10</td>
<td>25,000 （<em>5,000以获得最佳性能</em>）</td>
<td colspan="3">无限制（映射到组织的LDAP）</td>
</tr>
<tr>
<th scope="row"><strong>需要</strong></th>
<td>Adobe Admin Console</td>
<td>创建和更新.csv文件格式，最好使用Microsoft Excel</td>
<td>您必须设置Azure AD或Google联合</td>

<td>
  <ul>
    <li>macOS终端或Windows命令提示符</li>
    <li>了解LDAP</li>
  </ul>
</td>

<td>掌握编程语言（如Python）以使用REST API的工作知识</td>
</tr>
<tr>
<th scope="row"><strong>了解更多信息</strong></th>
<td><a href="https://helpx.adobe.com/cn/enterprise/using/manage-users-individually.html">管理个人用户</a></td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/bulk-upload-users.html">
        管理用户|批量上传CSV
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/kb/troubleshoot-bulk-user-csv-upload.html">
        批量用户CSV上传疑难解答
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/sso-setup-azure.html">
        Azure AD连接器
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/setup-sso-google.html">
        Google联盟连接器
      </a>
    </li>
  </ul>
</td>

<td>
  <ul>
    <li>
      <a href="https://adobe-apiplatform.github.io/user-sync.py/en/">
        关于用户同步
      </a>
    </li>
    <li>
      <a href="https://github.com/adobe-apiplatform/user-sync.py">
        Git存储库
      </a>
    </li>
    <li>
      <a href="https://helpx.adobe.com/enterprise/using/user-sync.html">
        分步指南
      </a>
    </li>
  </ul>
</td>
<td><a href="https://developer.adobe.com/umapi/">关于UMAPI</a></td>
</tr>
</tbody>
</table>

## 后续步骤

### 创建包

添加后，您的用户即准备好分配其指定的应用程序和服务。

根据您的许可方法为最终用户分配许可证：

- **命名用户许可：**&#x200B;将这些用户添加到&#x200B;**产品** （[适用于团队](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)）或&#x200B;**产品配置文件** （[适用于企业](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html)），以授予他们Adobe产品和服务授权。 有关更多详细信息，请参阅如何[创建指定用户授权包](https://helpx.adobe.com/enterprise/using/create-nul-packages.html)和[产品配置文件](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#create-product-profile)。
- **共享设备许可：** [添加的用户](https://helpx.adobe.com/enterprise/using/sdl-deployment-guide.html#add-users-admin-console)可以使用配置的共享设备，只有&#x200B;**组织用户才能访问**。 有关详细信息，请参阅[创建SDL包](https://helpx.adobe.com/enterprise/using/create-sdl-packages.html)。

### 部署包

创建包后，使用以下方法之一将其部署到客户端计算机：

- 转到客户端计算机，然后双击包文件（Windows或macOS）。
- 使用Windows命令提示符或macOS终端。
- 使用第三方工具：
   - [Microsoft Intune](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ms-intune.html)
   - [Microsoft System Center Configuration Manager (SCCM)](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-sccm.html)
   - [Apple远程桌面(ARD)](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-ard.html)
   - [JAMF Pro](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-jamf-pro.html)
   - [Munki](https://helpx.adobe.com/enterprise/kb/deploy-packages-using-munki.html)

## 相关阅读

- [管理用户|单独](https://helpx.adobe.com/cn/enterprise/using/manage-users-individually.html)
- [管理用户|批量CSV上传](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)
- [管理目录用户](https://helpx.adobe.com/enterprise/using/manage-directory-users.html)
- [管理控制台](https://helpx.adobe.com/enterprise/using/admin-console.html)
- [将用户分配给产品配置文件（适用于企业和机构）](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html#assign-users)
- [将许可证分配给团队用户](https://helpx.adobe.com/enterprise/using/assign-licenses-to-teams-users.html)
- [业务存储模型](https://helpx.adobe.com/enterprise/kb/business-storage-model-introduction.html)