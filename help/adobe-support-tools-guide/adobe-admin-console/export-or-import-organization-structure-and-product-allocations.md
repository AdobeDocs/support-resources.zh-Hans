---
title: 导出或导入组织结构和产品分配
description: 了解全局管理员如何使用JSON、CSV或XLSX在Global Admin Console中导出和导入组织层次结构和产品分配数据。 适用于企业。
feature-set: Experience Cloud Services
solution: Admin Console
feature: Admin Console
exl-id: 3220086a-4603-465f-a3e3-194193ca10ba
source-git-commit: ee2da1708a19eb7871ffb03f2840c0b7d82bd159
workflow-type: tm+mt
source-wordcount: '4423'
ht-degree: 3%

---

# 导出或导入组织结构和产品分配

**应用于：**&#x200B;企业

了解全局管理员如何通过Global Admin Console中的导出和导入功能简化组织和产品管理。

访问&#x200B;**[!UICONTROL Global Admin Console]**&#x200B;中的[组织](https://helpx.adobe.com/cn/enterprise/global-admin-console/adopt-global-administration.html)选项卡以导出或导入组织结构。 转到分配数据的&#x200B;**[!UICONTROL 产品分配]**&#x200B;选项卡。 使用&#x200B;**[!UICONTROL 更多选项]** **⋮**&#x200B;图标选择导出或导入。 [登录到Global Admin Console](https://global-admin-console.adobe.com)。

## 导出组织结构

作为[全局管理员](https://helpx.adobe.com/cn/enterprise/global-admin-console/manage-administrators.html)，您可以导出组织层次结构。 您可以下载整个组织层次结构或其子集的JSON、CSV或XLSX表示形式。 然后，您可以使用此数据进行分析或修改。

选择的导出格式会影响导出数据的结构：

- CSV格式 — 允许一次仅导出一种数据。 以CSV格式导出产品用户档案时，用户档案和资源将合并到一个表中。 产品配置文件有多个条目，每个资源一个。
- XLSX格式 — 导致每个组织详细信息显示在单独的工作表中。 记录通过引用ID连接在不同对象类型之间。 在某些情况下，特定对象（例如，当存在与给定资源关联的一组值时，资源对象）可能有多行。
- JSON格式 — 最灵活。 它可以利用导出对象之间的结构关系（例如，组织中的产品直接出现在组织元素中）。 相同的字段会以所有三种格式导出，但某些值在JSON格式中是多余的。

### 导出步骤

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)。 在&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡中，使用组织选取器选择要导出的组织层次结构。 将导出层次结构中所有组织的数据。
2. 选择&#x200B;**[!UICONTROL 更多选项]**⋮图标，然后选择&#x200B;**[!UICONTROL 导出]**。

   ![导出组织结构](./assets/export-org-structure.png)

3. 在&#x200B;**[!UICONTROL 导出]**&#x200B;对话框中，选择要导出的内容以及导出数据的格式。

   ![Admin Console导出对话框](./assets/export-12.png)

4. 选择&#x200B;**[!UICONTROL 导出]**。 生成导出文件可能需要几分钟时间。 完成后，要下载报表，请导航到&#x200B;**[!UICONTROL Global Admin Console]** > **[!UICONTROL 分析]** > **[!UICONTROL 导出报表]**。

>[!NOTE]
>
>JSON文件将以zip格式导出。 您可以使用zip实用程序或操作系统的zip功能来打开它们。

下载文件后，您可以处理数据，然后将其导入回。 导入的更新将显示在Global Admin Console中，就像您手动编辑数据一样。

## 导入组织结构

作为[全局管理员](https://helpx.adobe.com/cn/enterprise/global-admin-console/manage-administrators.html)，您可以导入可能修改的数据。 上传后，新数据与当前数据进行比较，所有更改都应用于组织层次结构。 所有导入操作均在组织层次结构的更新副本上执行。 如果您有任何挂起的更改，导入更改将添加到层次结构中挂起的更改之上。

### 导入步骤

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com)。 在&#x200B;**[!UICONTROL 组织]**&#x200B;选项卡中，使用组织选取器选择要执行导入的组织层次结构。
2. 选择&#x200B;**[!UICONTROL 更多选项]** **⋮**&#x200B;图标并选择&#x200B;**[!UICONTROL 导入]**。 根据导入文件的大小和复杂性，处理过程可能需要几秒钟到几分钟的时间。
3. 选择&#x200B;**[!UICONTROL 选择一个文件]**，然后选择要上载的JSON、CSV或XLSX文件。 对于CSV，一次只能导入一个组织详细信息，并且不支持导入产品。 导入的更改看起来就像是手动编辑数据一样。
4. 选择&#x200B;**[!UICONTROL 关闭]**。
5. 选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 然后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/execute-jobs.html)。 在执行更改之前，挂起的操作将以与在Global Admin Console中手动编辑时相同的方式显示。

## 导出和导入架构

使用CSV文件导入数据时，字段可以按任意顺序显示，但必须始终与其标题行匹配。

导入数据时，必须为每个元素指定一个操作。 该操作可以是以下任一操作：

- 更新：表示编辑。
- 创建：指示创建新对象（例如，组织、用户组或管理员）。
- 删除：指示删除对象（例如，组织、用户组或管理员）。

忽略不含或空白操作字段的输入记录。

### 组织

<table>
  <tr>
    <th>字段名称</th>
    <th>描述</th>
    <th>注释</th>
  </tr>

<tr>
    <td>ID</td>
    <td>
      组织ID。<br><br>
      添加新组织时，此值可以为空或设置为占位符标识符，例如，
      new_org_1。 在其他导入条目需要引用时，将使用占位符标识符
      加入这个组织。 创建后，将分配一个实际的组织ID，并将替换所有
      占位符组织id的使用。
    </td>
    <td>当operation=create时，可以设置为临时值</td>
  </tr>

<tr>
    <td>name</td>
    <td>
      组织简单名称。 最小长度4，最大100。
      名称最多可包含3个字节的UTF-8字符，
      不支持4字节字符。
    </td>
    <td>
      可分别在operation=create或operation=update时设置或更新
    </td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>国家或地区代码</td>
    <td>
      必须在operation=create时设置，可在operation=update时更新
    </td>
  </tr>

<tr>
    <td>类型</td>
    <td>组织类型</td>
    <td>只读</td>
  </tr>

<tr>
    <td>parentOrgId</td>
    <td>
      父组织ID。 对于根组织为空。
      更新时，会应用重大限制，包括新父项必须位于同一层次结构中，而且
      拥有组织中已有的产品。
    </td>
    <td>
      可分别在operation=create或operation=update时设置或更新
    </td>
  </tr>

<tr>
    <td>管理员计数</td>
    <td>管理员数量</td>
    <td>只读</td>
  </tr>

<tr>
    <td>domaincount</td>
    <td>域数</td>
    <td>只读</td>
  </tr>

<tr>
    <td>用户计数</td>
    <td>用户数量</td>
    <td>只读</td>
  </tr>

<tr>
    <td>userGroup计数</td>
    <td>用户组数</td>
    <td>只读</td>
  </tr>

<tr>
    <td>管理员</td>
    <td>表示该组织管理员的管理员对象集</td>
    <td rowspan="6">
      如果未选择导出，则可能缺失。 它显示在XLSX文件的单独选项卡中。
    </td>
  </tr>

<tr>
    <td>域</td>
    <td>表示此组织中域的一组域对象</td>
  </tr>

<tr>
    <td>产品</td>
    <td>表示此组织中产品的一组产品对象</td>
  </tr>

<tr>
    <td>产品配置文件</td>
    <td>表示此组织中产品配置文件的一组产品配置文件对象</td>
  </tr>

<tr>
    <td>用户组</td>
    <td>表示此组织中用户组的一组用户组对象</td>
  </tr>

<tr>
    <td>orgPolicy</td>
    <td>表示策略及其值的结构</td>
  </tr>

<tr>
    <td>操作</td>
    <td>
      “创建”、“更新”或“删除”之一。 导入数据时要执行的操作。
    </td>
    <td>导出时始终为空。</td>
  </tr>
</table>


**导入要求：**

- 对于更新或删除，orgId必须引用层次结构中的现有组织。
- 如果要创建新组织，可将orgId字段留空，或将其设置为可组成的唯一id（如new-1或new-2）。 这将提供一个ID，可用于引用待创建的组织。
- 国家/地区代码应有效。
- 组织层次结构中应已存在&#x200B;*更新*&#x200B;和&#x200B;*删除*&#x200B;操作的orgId。
- 对于具有&#x200B;*更新*&#x200B;或&#x200B;*创建*&#x200B;操作的组织，不应选择标记为&#x200B;*删除*&#x200B;的orgId作为parentOrgId。
- 处于相同级别和相同父项的子组织不应具有相同的orgNames。
- 在创建组织或更新组织名称时，组织名称不能与同一父项的现有子项名称匹配。

### 管理员

<table>
  <tr>
    <th>字段名称</th>
    <th>描述</th>
    <th>使用</th>
  </tr>

<tr>
    <td>orgId</td>
    <td>对管理员所在组织的引用。</td>
    <td>用作查找包含或关联对象的引用。</td>
  </tr>

<tr>
    <td>firstName</td>
    <td>
     管理员用户名字。
Adobe ID用户的名字和姓氏可在用户接受邀请时替换为用户提供的值。
    </td>
    <td rowspan="4">
      可分别在operation=create或operation=update时设置或更新
    </td>
  </tr>

<tr>
    <td>姓氏</td>
    <td>管理员用户姓氏</td>
  </tr>

<tr>
    <td>电子邮件</td>
    <td>管理员用户电子邮件地址。 这是用户的主键，必须是唯一的。</td>
  </tr>

<tr>
    <td>countryCode</td>
    <td>
用户操作所在的国家/地区代码。 仅适用于Federated Id和Enterprise Id类型。
    </td>
  </tr>

<tr>
    <td>用户类型</td>
    <td>“Adobe ID”、“Enterprise ID”或“Federated ID”之一。</td>
    <td>只读</td>
  </tr>

<tr>
    <td>adminType</td>
    <td>“全局管理员”、“全局查看器”、“系统管理员”、“用户组管理员”、“产品管理员”、“产品配置文件管理员”、“部署管理员”和“存储管理员”之一。</td>
    <td rowspan="4">当operation=Create时可以设置</td>
  </tr>

<tr>
    <td>groupId</td>
    <td>此用户为其管理员的组的组ID。 仅与用户组和产品配置文件管理员相关。</td>

</tr>

<tr>
    <td>licenseId</td>
    <td>此用户为其管理员的产品的产品许可证ID。 仅与产品管理员相关。</td>

</tr>

<tr>
    <td>域</td>
    <td>如果未使用电子邮件域，则为用户的域名</td>

</tr>

<tr>
    <td>用户名</td>
    <td>如果未使用电子邮件地址，则为用户的用户名</td>
    <td></td>
  </tr>

<tr>
    <td>操作</td>
    <td>“创建”、“更新”或“删除”之一。 导入数据时要执行的操作。</td>
    <td></td>
  </tr>
</table>


**导入要求：**

- orgId、email、adminType和userType必须包含有效值。
- countryCode必须有效。
- 如果用户已存在且正在更新，则userType必须与用户匹配。
- 检查组织中是否有重复的电子邮件地址。

### 产品配置文件

产品配置文件的导出和导入包含两部分：产品配置文件详细信息以及一组与产品配置文件关联的资源。 这些资源标识可以配置的服务，通常只是为了启用或禁用它们。

- 资源对象以JSON格式嵌套在产品配置文件中。
- 当将CSV或XLSX与产品配置文件结合使用时，配置文件和资源将合并到一个表中。 产品配置文件将有多个条目，每个资源各一个。
- 资源中的“选定”字段控制服务是否已启用。
- 导入产品配置文件时，必须对产品配置文件本身以及要更新或创建的任何资源对象执行创建或更新操作。


<table>
  <tr>
    <th>字段名称</th>
    <th>描述</th>
    <th>使用</th>
  </tr>

<tr>
    <td>productProfileId</td>
    <td>
     <br><br>
      产品配置文件的标识符
可以在创建时使用占位符值，以便其他对象可以引用新配置文件。
    </td>
    <td>当operation=create时，可设置为临时值</td>
  </tr>

<tr>
    <td>productProfileName</td>
    <td>
     产品配置文件的名称。 它不能与同一组织中的其他产品配置文件或用户组重复。
    </td>
    <td rowspan="2">
   可分别在operation=create或operation=update时设置或更新
    </td>
  </tr>

<tr>
    <td>productProfileDescription</td>
    <td>产品配置文件的文本描述</td>
  </tr>

<tr>
    <td>licenseId</td>
    <td>产品的许可证ID引用</td>
    <td rowspan="2"> 用作查找包含或关联对象的引用
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>
包含用户组的组织
    </td>
  </tr>

<tr>
    <td>通知</td>
    <td>True或False，指示在添加用户或从此产品配置文件中删除用户时，是否应向他们发送电子邮件通知</td>
    <td>可分别在operation=create或operation=update时设置或更新</td>
  </tr>

<tr>
    <td>资源</td>
    <td> 与此产品配置文件关联的资源数组。
资源字段仅可用于JSON格式。 对于CSV和XLSX格式，资源由以下附加字段表示：resourceName、resourceId、resourceDescription、icon、selected、quota、resourceType。 有关这些字段的详细信息，请参阅[产品和资源](#products-and-resources)。
如果产品配置文件有多个资源，则将显示多个行，每个资源对应一行。 其他字段将具有每个资源的相同值。 </td>
    <td></td>
  </tr>

<tr>
    <td>操作</td>
    <td>“创建”、“更新”或“删除”之一。 导入数据时要执行的操作。</td>  
    <td></td>
  </tr>
</table>



**导入要求：**

- productProfileId、licenseId和orgId必须具有有效值。
- 创建产品配置文件时，productProfileName必须是有效的名称，并且不得与同一组织中的其他产品配置文件名称或用户组名称重复。
- 配额字段必须具有设备类型的有效值。 当resourceType=QUOTA或为空时，该值为数值或“无限制”。
- 通知字段必须为true或false。
- 对于CSV和XLSX导入，请验证productProfileId；其所有条目必须具有相同的orgId、licenseId和productProfileName。
- 验证输入文件和组织中重复的productProfileName。
- 要更新和删除的用户档案必须存在于组织中。
- 配置文件中必须存在要更新和删除（已停用）的资源。
- 对于要创建的用户档案，请确保以下各项：
   - orgId应为新组织或现有组织。
   - licenseId应为新产品或现有产品。
   - 验证用户档案的资源。

### 产品配置文件中的资源

<table>
  <tr>
    <th>字段名称</th>
    <th>描述</th>
    <th>使用</th>
  </tr>

<tr>
    <td>resourceName</td>
    <td>资源的名称</td>
    <td>只读</td>
  </tr>

<tr>
    <td>resourceId</td>
    <td>资源的标识符</td>
    <td>只读</td>
  </tr>

<tr>
    <td>resourceDescription</td>
    <td>资源的文本描述</td>
    <td>只读</td>
  </tr>

<tr>
    <td>图标</td>
    <td>资源图像的URL</td>
    <td>只读</td>
  </tr>

<tr>
    <td>已选择</td>
    <td>
      对于配置条目，是否启用该功能。
      此字段仅在JSON中存在。
    </td>
    <td rowspan="2">
      当operation=create或operation=update时，可以分别设置或更新。
    </td>
  </tr>

<tr>
    <td>配额</td>
    <td>
      可以通过此产品配置文件提供给用户的主要资源数量。
      此字段仅在JSON中存在。
    </td>
  </tr>


<tr>
    <td>resourceType</td>
    <td>
      如果存在，则值为SERVICE。 它指示此资源表示服务可以
      根据选定字段的值启用或禁用。
      此字段仅在JSON中存在。
    </td>
    <td>只读</td>
  </tr>

<tr>
    <td>操作</td>
    <td>
      “创建”、“更新”或“删除”之一。 导入数据时要执行的操作。
    </td>
    <td></td>
  </tr>
</table>


**导入要求：**

- 当资源所属的产品配置文件的操作设置为&#x200B;*删除*&#x200B;或&#x200B;*创建*&#x200B;时，将忽略资源的操作字段。
- 不应将任何资源标记为删除；这是一个无效的操作。
- 对于要创建的产品配置文件，资源数应与源产品配置文件的资源数匹配。
- 对于具有&#x200B;*更新*&#x200B;操作的资源，该资源必须存在于产品配置文件中。

### 用户组

<table>
  <tr>
    <th>字段名称</th>
    <th>描述</th>
    <th>使用</th>
  </tr>

<tr>
    <td>userGroupId</td>
    <td>
      用户组的标识符。 可以在创建时使用占位符值，以便
      其他对象可以引用新的用户组。
    </td>
    <td>当operation=create时，可设置为临时值</td>
  </tr>

<tr>
    <td>userGroupName</td>
    <td>用户组的名称</td>
    <td rowspan="2">
      当operation=create或operation=update时，可以分别设置或更新。
    </td>
  </tr>

<tr>
    <td>userGroupDescription</td>
    <td>用户组的文本描述</td>
  </tr>

<tr>
    <td>用户计数</td>
    <td>用户组中的用户数</td>
    <td>只读</td>
  </tr>

<tr>
    <td>轮廓</td>
    <td>
      用户组关联的产品配置文件ID数组。
      XLSX的每个值有一行，其他字段的值相同。
    </td>
    <td>
      当operation=create或operation=update时，可以分别设置或更新。
    </td>
  </tr>

<tr>
    <td>orgId</td>
    <td>包含用户组的组织</td>
    <td>用作查找包含或关联对象的引用</td>
  </tr>

<tr>
    <td>操作</td>
    <td>
      “创建”、“更新”或“删除”之一。 导入数据时要执行的操作。
    </td>
    <td></td>
  </tr>
</table>

**导入要求：**

- orgId必须引用现有组织或在同一导入中创建的组织。
- userGroupId必须引用要更新或删除的现有组，并且可以是您为新用户组定义的ID。
- 对于更新或创建，userGroupName不能为空，并且不得与同一组织中的其他用户组或产品配置文件名称重复。
- 确保userGroupName在输入文件和组织中不重复。
- 要更新和删除的用户组必须存在于组织中。
- 要从用户组中删除的配置文件必须存在于用户组中。 无法对用户组的配置文件执行更新操作。
- 对于要创建的用户组，请确保以下各项：
   - orgId应为新组织或现有组织。
   - 该licenseId （如果适用）应当为新产品或现有产品。
   - productProfileId应该是新产品配置文件或现有产品配置文件。

### 域

域信息提供有关每个组织中可用域的只读信息。 此数据不可编辑。


| 字段名称 | 描述 | 使用 |
| ------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| orgId | 引用列出此域的组织 | 用作查找包含或关联对象的引用。 |
| 域名 | 域的名称(例如，adobe.com)。 | 只读 |
| directoryName | 列出域的目录的名称 | 只读 |
| 目录类型 | Federated ID或Enterprise ID之一。 | 只读 |
| domainstatus | “活动”、“已保留”、“无人认领”、“已认领”、“已验证”、“已撤回”、“已过期”之一。 | 只读 |


### 产品和资源 {#products-and-resources}

在XLSX文件中，有两个工作表，一个用于产品，另一个用于资源。 在JSON中，资源对象嵌套在产品对象中。

**产品**


| 字段名称 | 描述 | 使用 |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| licenseId | 标识产品的ID。 每个产品在列出它的组织中具有唯一的许可证ID。 添加新产品时，此项可以为空或使用占位符标识符（例如，new_product_1）。 创建后，会分配一个实际许可证ID以替换占位符许可证ID的所有使用。 | 当operation=create时，可设置为临时值 |
| 产品名称 | 产品的名称 | 只读 |
| 产品描述 | 产品的文本描述 | 只读 |
| 允许过度分配 | 布尔值，指示是否允许过度分配此产品实例。 过度分配是指向子组织授予的数量多于授予的能力。 | 可分别在operation=create或operation=update时设置或更新 |
| 图标 | 产品图标的URL | 只读 |
| sourceLicenseId | 从中分配此产品的组织中产品实例的许可证ID。 如果此实例不是已分配产品，而是已购买产品，则值为空。 | 当operation=Create时可以设置 |
| productId | 产品的标识符。 | 只读 |
| orgId | 包含此产品实例的组织的标识符 | 用作查找包含或关联对象的引用 |
| 可再分发 | 布尔值，表明此产品是否具有可授予子组织的资源。 | 只读 |
| 资源 | 包含表示此产品中的资源和设置的一组资源对象的对象 |                                                                               |
| 操作 | “创建”、“更新”或“删除”之一。 导入数据时要执行的操作。 |                                                                               |


**导入要求：**

- 对于create，licenseId必须是您创建的唯一id。
- 对于更新，licenseId必须是指定组织中现有产品的ID。
- orgId必须引用现有组织或在同一导入操作中创建的组织。
- 对于create，sourceLicenseId必须引用现有产品，或您为在同一导入操作中创建的产品定义的ID。
- 对于具有&#x200B;*创建*&#x200B;操作的产品，licenseId和sourceLicenseId不应相同。
- 验证产品的组织；组织应为新组织或组织层次结构中已存在组织。
- 对于&#x200B;*更新*&#x200B;和&#x200B;*删除*&#x200B;操作，组织层次结构中应该已存在产品。
- 标记为&#x200B;*Delete*&#x200B;的licenseId不应用作具有&#x200B;*创建*&#x200B;和&#x200B;*更新*&#x200B;操作的产品的sourceLicenseId。
- 对于具有&#x200B;*Create*&#x200B;操作的产品，请验证sourceLicenseId应存在于父组织中。

产品的&#x200B;**资源**

资源对象可以显示在产品和产品配置文件中。


| 字段名称 | 描述 | 使用 |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| resourceName | 资源的名称 | 只读 |
| resourceId | 资源的标识符 | 只读 |
| resourceDescription | 资源的文本描述 | 只读 |
| 图标 | 资源图像的URL | 只读 |
| 产品名称 | 此资源所属产品的名称。 | 只读 |
| licenseId | 此资源所属产品的许可证ID（产品实例）。 | 用作查找包含或关联对象的引用 |
| grantedQuantity | 此资源的授权数量：此组织可用于本地使用或分配给子组织的资源数量。 | 可分别在operation=create或operation=update时设置或更新 |
| 单位 | 授予数量的单位名称。 | 只读 |
| currentquantity | 此组织中的当前可用数量。 这是分配给子组织的grantedQuantity减去资源。 此值显示在Admin Console中的此产品/资源中。 | 只读 |
| provisionquantity | 实际配置的数量：可以小于授权或当前，如果存在某些限制，则可以小于currentQuantity。 | 只读 |
| 操作 | “创建”、“更新”或“删除”之一。 导入数据时要执行的操作。 |                                                                               |


**导入要求：**

当资源所属的产品具有设置为&#x200B;*删除*&#x200B;或&#x200B;*创建*&#x200B;的操作时，资源上的操作字段将被忽略。
- 不应将任何资源标记为删除；这是一个无效的操作。
- 对于要创建的产品，资源的数量应该与源产品的资源数量匹配。
- 对于具有&#x200B;*更新*&#x200B;操作的资源，该资源必须存在于产品中。

## 导入和导出产品分配数据

作为[全局管理员](https://helpx.adobe.com/cn/enterprise/global-admin-console/manage-administrators.html)，您可以将产品分配数据导出为JSON或CSV文件。 然后，您可以处理此数据并将其上载回以导入更改。 上传可能修改的数据后，将新数据与当前数据进行比较，所有更改都应用于产品分配数据。 然后，您可以查看并提交待定更改以使它们生效。

## 导出产品分配模型

要导出产品分配模型，请执行以下操作：

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)，然后导航到&#x200B;**[!UICONTROL 产品分配]**&#x200B;选项卡。
2. 选择&#x200B;**[!UICONTROL 更多选项]**⋮图标，然后选择&#x200B;**[!UICONTROL 导出CSV]**&#x200B;或&#x200B;**[!UICONTROL 导出JSON]**。 您的文件已下载。 [了解导出格式的更多信息](#export-and-import-formats-for-product-allocation)。

## 导入产品分配模型

您可以导出数据、修改数据，然后导入修改后的文件。 要导入产品分配模型，请执行以下操作：

1. 登录到[Global Admin Console](https://global-admin-console.adobe.com/)，然后导航到&#x200B;**[!UICONTROL 产品分配]**&#x200B;选项卡。
2. 选择&#x200B;**[!UICONTROL 更多选项]**⋮图标，然后选择&#x200B;**[!UICONTROL 导入]**。
3. 选择要上载的JSON或CSV文件。
4. 选择&#x200B;**[!UICONTROL 审阅挂起的更改]**。 查看更改后，选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以[执行更改](https://helpx.adobe.com/cn/enterprise/global-admin-console/execute-jobs.html)。

## 导出和导入产品分配的格式

导出和导入格式相同。 以CSV格式导入时，字段可以按任意顺序显示，但它们必须与标题行匹配。 以JSON格式导入时，这些字段可以按任意顺序显示。

导入产品分配数据时必须指定操作。 该操作可以是以下操作之一：

- 更新：指示编辑（更改为grantedQuantity、allowOverAllocation值）。
- 创建：指示将产品资源添加到指定组织。
- 删除：指示删除产品。

如果未给出任何操作，则在CSV中为该行导入数据或在JSON中导入对象时，不会发生任何更改。

在导出的文件中，每个产品资源都有一个行或记录。 某些产品具有多个资源。

如果产品具有多个资源，则更新操作可应用于独立资源，删除操作会从组织中删除产品（包括所有资源），而创建操作需要导入文件中每个资源的记录，以便指定每个资源的适当数量。 allowOverAllocation字段在产品范围内并且此字段更新所在的资源无关紧要。

### 标题描述


| 字段名称 | 描述 | 使用 |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| 产品名称 | 产品的名称。 | 只读 |
| licenseId | 产品的ID（特定于组织中的产品）。 添加新产品时，此项可以为空或设置为占位符标识符（例如，new_product_1）。 当其他导入的条目需要引用此产品时，将使用占位符标识符。 创建后，将分配实际许可证ID并替换占位符许可证ID的所有用法。 | 当operation=Create时可以设置 |
| sourceLicenseId | 父产品的ID。 如果它表示购买而非分配，则为空或为null。 | 当operation=Create时可以设置 |
| productId | 标识此产品类的ID。 此ID在同一类型的产品之间共享，并且与标识此产品实例的licenseId不同。 | 只读 |
| resourceName | 此产品资源的名称。 例如，用户许可证。 | 只读 |
| resourceId | 标识此产品资源的ID。 | 当operation=Create时可以设置 |
| orgPathName | 此产品资源所在的组织的路径名。 以“/”分隔的区段。 | 只读 |
| orgName | 包含此产品资源的组织的简单名称。 这是orgPathName的最后一个区段。 | 只读 |
| orgId | 包含此产品资源的组织的组织ID。 | 当operation=Create时可以设置 |
| grantedQuantity | 此组织的父级授予此组织的资源数量单位数，如果此产品资源条目表示采购，则为采购额。 此字段可更新，但全局管理员无权更改已购买的产品或根分配除外。 | 当operation=Update或operation=Create时可以更新 |
| 单位 | 资源单位的名称。 例如，用户。 | 只读 |
| 总计分配 | 此组织针对此产品资源向子组织授予的授权总和。 此值包括对直接子女的直接赠款以及来自这些组织的超额拨款。 例如，如果该组织授予儿童10，然后该儿童分配其儿童25，则totalAllocations将为25：授予该儿童的10加上该儿童的15岁超额。 | 只读 |
| grantOverage | totalAllocations超过grantedQuantity的金额。 如果totalAllocations未超过grantedQuantity，则此值为null或零。 | 只读 |
| localLicensedQuantity | 在扣除分配给子项的数量后，分配给此组织的剩余资源量。 这是Admin Console中显示的可用数量。 此值可以为零，但绝不为负，即使此组织过度分配资源给其子项也是如此。 | 只读 |
| localUsage | 此组织中使用的资源单位数。 例如，将用户许可证委派给用户将计为1个使用单位。 | 只读 |
| totalUsage | 此组织和所有子级使用的资源单位数。 这显示了此资源在以此组织为根的组织层次结构部分中的使用情况。 | 只读 |
| useOverage | 组织授权的总使用量（组织和子级已使用比可用资源更多的资源）。 当totalUsage超出localLicensedQuantity时，此设置将显示非零值。 | 只读 |
| allowOverallocation | 指示是否允许用户向儿童授予更多资源，即使没有更多资源可授予（尽管授予过多，仍允许授予）。 此值适用于此产品的所有资源。 如果尝试将同一产品的多个资源的allowOverallocation更新为不同的值，则结果为随机的。 | 当操作=更新时可以更新 |
| isPurchasedProduct | 如果产品是购买产品（未由父级分配），则为true。 这等同于具有空值的sourceLicenseId。 | 只读 |
| 可再分发 | 如果产品可分配给子项，则为true；如果为false，则表示产品仅在显示产品的组织中可用，且资源无法分配给其他组织。 | 只读 |
| 操作 | “创建”、“更新”或“删除”之一。 导入数据时要执行的操作。 |                                                          |


**导入要求**

**数据验证**

- 操作字段必须具有有效的操作。
- 产品导入数据必须具有必填字段的属性和值。
- 产品导入数据属性的类型必须正确。
- 不得为不同资源提供产品策略字段(overAllocation)。
- grantedQuantity字段：
   - 如果不是&#x200B;*unlimited*，则无法更改为&#x200B;*unlimited*。
   - 必须为非负整数或字符串值&#x200B;*无限制。*

**权限/可访问的验证**

- 与导入数据关联的组织必须存在。 如果要更新，请确保与导入数据关联的产品和资源确实存在。

**添加产品验证**

- SourceLicenseId必须存在。
- 必须存在与新产品关联的组织。
- 正在创建的产品不得存在（licenseId相同的产品）。
- 与正在创建的产品关联的资源必须具有与该产品匹配的相应productId。
