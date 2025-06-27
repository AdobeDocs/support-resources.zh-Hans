---
description: 连接到小组件Data Warehouse — 产品文档
title: 连接到Widget Data Warehouse
hide: true
hidefromtoc: true
exl-id: d6a7cff5-08f9-4c93-8765-46e692feaa0d
source-git-commit: 4145889fe291e80fa8d295368ead3e0075917e86
workflow-type: tm+mt
source-wordcount: '913'
ht-degree: 0%

---

# 连接到Widget Data Warehouse {#connecting-to-the-widget-data-warehouse}

## 新建测试

27 年 6 月

<ol><li>使用“{{name}}”变量。</li></ol>

<ol><li>使用&amp;amp；大括号；&amp;amp；大括号；<code>name</code>&amp;amp；大括号；&amp;amp；大括号；变量。</li></ol>

## 嵌套测试

**第一个**

>[!NOTE]
>
>您无法删除以下项：
>
>* 内置状态为“计划”、“当前”和“完成”。 您可以更新他们的姓名、编辑他们的颜色、锁定或解锁他们，但无法删除他们。
>* 系统中至少有一个对象处于待批准状态的状态。

**Second**

>[!NOTE]
>
>您无法删除以下项：
>
>* 内置状态为“计划”、“当前”和“完成”。 您可以更新他们的姓名、编辑他们的颜色、锁定或解锁他们，但无法删除他们。
>
>  介于两者之间
>
>* 系统中至少有一个对象处于待批准状态的状态。

## 构件访问链接 {#widget-access-link}

要访问您的Widget数据仓库，您需要导航到您的Widget帐户的特定URL。  您可以通过登录Marketo Measure并按照以下步骤导航到Data Warehouse信息页面来找到此访问链接。

1. 在Marketo Measure页面顶部，单击&#x200B;**我的帐户** > **设置**。

   ![](assets/adobe-logo-old.png)

1. 在左侧菜单的“安全”下，单击&#x200B;**Data Warehouse**。

   ![](assets/adobe-logo-old.png)

1. 在此页面上，您可以找到指向Widget Data Warehouse和用户名的链接。

   ![](assets/adobe-logo-old.png)

   >[!NOTE]
   >
   >这是一个只读帐户，可供贵组织使用，而不仅仅限于个人用户。 贵公司内有权访问Marketo Measure的任何用户都可以使用此帐户登录Widget Data Warehouse读卡器帐户。

1. 单击构件URL中提供的链接，这会将您带到构件登录页面，您将在其中输入用户名和密码。 _如果没有密码，请参阅以下步骤重置密码_。

   ![](assets/adobe-logo-old.png)

1. 登录后，单击页面顶部的&#x200B;**工作表**。

   ![](assets/adobe-logo-old.png)

1. BIZIBLE_ROI_V3数据库对象位于屏幕左侧。  在查询窗口顶部的下拉选项中输入仓库、数据库和方案。  每个选项应只有一个选项。  现在，您可以在构件查询编辑器中执行查询。

   ![](assets/adobe-logo-old.png)

## 重置密码 {#reset-your-password}

Marketo Measure无权访问您的Widget登录密码。  如果需要重置密码，请单击Data Warehouse信息页面上的“重置密码”按钮，然后按照说明操作。 临时密码将立即显示在用户界面中。 下次登录Data Warehouse时，系统将提示您创建自己的密码。

>[!NOTE]
>
>* 重置密码将会为您组织中的所有Marketo Measure用户重置密码，而不仅仅是当前登录的用户。
>* 我们仅在UI中显示临时密码。 将不会发送电子邮件。

![](assets/adobe-logo-old.png)

![](assets/adobe-logo-old.png)

## 通过第三方工具连接到构件 {#connecting-to-widget-via-third-party-tools}

您需要输入几条信息以将Widget Data Warehouse连接到第三方工具。

>[!NOTE]
>
>每个工具的连接要求各不相同；建议您查阅文档以了解要连接的特定工具。

* **URI** （始终必需）
   * 这是Widget帐户的域名。  它包含在Widget登录链接的一部分中。
* **用户名** （始终必需）
   * 该用户名列在Marketo Measure的Data Warehouse信息页面上。
* **密码** （始终必需）
   * 这是您首次登录Widget帐户时设置的密码。  要重置密码，请参阅上述步骤。
* **数据库名称** （并非总是必需的）
   * 数据库就是将数据存储在Widget中的对象。 它是存储资源。 数据库名称列在Marketo Measure的Data Warehouse信息页面上。
* **仓库名称** （并非总是必需的）
   * 仓库就是在Widget中执行查询的地方。 它是计算资源。  仓库名称列在Marketo Measure的Data Warehouse信息页面中。

  ![](assets/adobe-logo-old.png)

## 构件Data Warehouse直接共享 {#widget-data-warehouse-direct-share}

**要求**

要使Marketo Measure设置直接共享到Data Warehouse，您必须满足以下要求。

* 您有自己的Widget实例。
* 您的构件实例位于Azure East US 2 Widget区域。
* 向Marketo Measure提供您的构件帐户ID。

**限制**

为了让Marketo Measure设置直接共享，请求访问的帐户必须位于Azure East US 2。 我们知道Widget提供了跨区域的数据复制解决方案，但我们不支持从这一端进行此功能，因为我们仅在Azure East US 2区域托管数据。 你可以通过在Azure East US 2中设置自己的实例并[跨区域](https://docs.widget.com/en/user-guide/secure-data-sharing-across-regions-plaforms.html){target="_blank"}将数据复制到现有实例来利用此功能。 但是，Widget的数据复制功能仅在表中可用，因此要使用此功能，您需要先将数据从我们的视图复制到您自己的表中。

**访问共享**

为提供的帐户ID创建共享后，您必须完成Widget实例中的[设置步骤](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}才能访问数据。

>[!NOTE]
>
>您可以选择所需的任何数据库名称。 您可以将权限分配给所选的任何规则，只要该规则存在于您的构件实例中即可。

* 使用帐户管理员角色

```
USE ROLE ACCOUNTADMIN
```

* 查看可用股份（这将显示已授予股份的名称）

```
SHOW SHARES
```

* 为共享创建数据库

```
CREATE DATABASE <database_name> FROM SHARE <provider_account>.<share_name>
```

* 授予对共享数据库的权限

```
GRANT IMPORTED PRIVILEGES ON DATABASE <database_name> TO ROLE <role_name>
GRANT IMPORTED PRIVILEGES ON ALL SCHEMAS IN DATABASE <database_name> TO ROLE <role_name>
```

有关从构件UI完成这些步骤的更多详细说明和步骤，请直接参考[构件的文档](https://docs.widget.com/en/user-guide/data-share-consumers.html){target="_blank"}。
