---
title: 错误修复（隐藏）
description: 作内部测试用途的测试页面
hide: true
hidefromtoc: true
exl-id: e6270f95-3550-4e35-ad4c-760584bb9b5d
source-git-commit: 0cefcf5bb4a021593a6bbe44eed0ad83e8bd259f
workflow-type: tm+mt
source-wordcount: '1926'
ht-degree: 27%

---

# 错误修复

## 自动激活测试

这些错误都应修复。

## UGP-10866链接在阴影框中不粗体

>[!BEGINSHADEBOX]

**目录**

* [AI 助手入门](note-test.md)
* **[使用AI助手生成电子邮件](syntax-style-guide.md)**
* [使用 AI 助手生成短信](test-page.md)
* [使用AI助手生成推送](tables.md)
* [使用AI助手进行内容试验](test-redirection.md)

>[!ENDSHADEBOX]

无阴影框

**目录**

* [AI 助手入门](note-test.md)
* **[使用AI助手生成电子邮件](syntax-style-guide.md)**
* [使用 AI 助手生成短信](test-page.md)
* [使用AI助手生成推送](tables.md)
* [使用AI助手进行内容试验](test-redirection.md)


## UGP-10584内联徽章不起作用

这些徽章应与项目符号位于同一行。

* [[!DNL Mixpanel]](note-test.md) [!BADGE 注释]{type=Informative}
* [[!DNL Pendo]](tables.md) [!BADGE 表]{type=Positive}
* [[!DNL RainFocus]](syntax-style-guide.md) [!BADGE 语法样式指南]{type=Positive}

## UGP-10560 — 可折叠部分中的徽章

+++ 先前版本

### V1.16发布

_2023 年 2 月 13 日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 目录服务API现在支持产品视频。
![修复](assets/package.png) 现在支持固定价格的捆绑产品。
![修复](assets/package.png) 缺货期权现在显示在PDP构件中。

#### 已知限制

尚不支持以下功能：

* 动态属性有效负载的最大大小为9 MB。
* 组产品价格。 可以用简单的产品价格来计算。
* 在图像数组中，只有第一个图像包含角色。

使用API网格和核心GraphQL API可以解决以下限制：

* 最低广告价格
* [分层定价](https://www.adobe.com/cn)

### V1.13发布

_2023年10月12日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 目录服务支持 `inStock` 产品变型的标记。
![新建](assets/package.png) `urlKey` 和 `externalId` 已添加到GraphQL架构。
![新建](assets/package.png) 现在支持可下载产品和礼品卡。

### V1.12发布

_2023年9月19日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](https://www.adobe.com/cn).
![修复](assets/package.png) 此版本包含服务端的错误修复和改进。

### V1.11发布

_2023年7月18日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 目录服务现在支持 [`recommendations`](https://developer.adobe.com/commerce/services/graphql/recommendations/recommendations/) GraphQL查询产品Recommendations。

### V1.10发布

_2023年6月27日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 目录服务API现在支持“相关产品”。

### V1.7发布

_2023年4月12日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 目录服务现在可以清理已删除的产品变型。
![修复](assets/package.png) 基础架构可扩展性和性能改进。

### V1.6发布

_2023年3月28日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 已将样本添加到 [`products`](https://developer.adobe.com/commerce/services/graphql/catalog-service/products/) 查询。
![新建](https://www.adobe.com/cn).

### V1.5发布

_2023年3月6日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 已添加 [`categories`](https://developer.adobe.com/commerce/services/graphql/schema/catalog-service/categories/) GraphQL功能。
![修复](assets/package.png) 改进了性能和API可扩展性。

### V1.4发布

_2023年2月7日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 已发布目录服务元包以简化安装步骤。
![修复](assets/package.png) API可扩展性和性能改进。

### V1.3发布

_2023年1月17日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 简化并改进了载入体验。
![新建](assets/package.png) 新的客户沙盒端点可用于预生产测试。
![新建](assets/package.png) 添加了对虚拟产品的支持。
![修复](assets/package.png) API可扩展性和性能改进。

### V1.1发布

_2022年11月18日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 目录服务现在支持Adobe [API网格](https://developer.adobe.com/graphql-mesh-gateway/).
![修复](assets/package.png) 改进了API可扩展性和整体性能。

### V1.0发布

_2022年10月4_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 现在支持捆绑产品和分组产品。
![新建](assets/package.png) 添加了B2B可见性覆盖。 产品现在可供搜索，并可添加到特定客户组的购物车中。
![修复](assets/package.png) 服务现在更加稳定并提高了性能。

### 0.3版本 — Beta+

_2022年9月12日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 变体支持的图像：根据所选选项返回产品图像
![新建](assets/package.png) 价格支持角色：仅允许特定客户组的成员查看产品价格
![修复](assets/package.png) 提高了服务的稳定性和性能
![新建](assets/package.png) 从目录中删除产品时会收到更新

### 测试版

_2022 年 9 月 9 日_

[!BADGE 支持]{type=Informative tooltip="受支持"}

![新建](assets/package.png) 此 `products` 和 `refineProduct` 查询返回以下数据：

* 预定义的（系统）产品属性。
* 动态产品属性，并按角色（产品显示页面/产品列表页面）筛选这些属性。
* 产品选项。
* 产品图像并按角色(PDP/PLP)过滤它们。
* 简单产品的具体价格以及可配置产品的价格范围。
* 客户组价格及价格范围。 它们向没有客户群组的购物者返还后备默认价格。
* 使用B2B客户特定定价的产品类型。

+++

## [!BADGE 已弃用]{type=negative}

请参阅以上标题。 还有下一个。

## 测试自动激活

我已在星期五下午添加了此内容，但未单击“立即发布”。

### [!BADGE Beta]{type=Informative}

Bob

## UGP-10565 — 文本突出显示

在此之前的文本 `<div class="preview">`

<div class="preview">

### 添加Workfront本机字段

您可以将Workfront原生字段添加到自定义表单。 将自定义表单附加到对象时，会从对象数据填充字段。 例如，附加到项目的自定义表单上的描述字段将拉入项目描述。 （如果没有可用数据，则字段可能显示“不适用”。）

1. 在屏幕左侧，查找 **原生字段** 然后将其拖动到画布上的某个部分。
1. 在屏幕右侧，配置自定义字段的选项：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">标签</td> 
      <td> <p>（必需）键入要在该字段上方显示的描述性标签。 您可以随时更改标签。</p> <p><b>重要</b>：避免在此标签中使用特殊字符。 它们在报表中无法正确显示。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">名称</td> 
      <td> <p>（必需）此名称是系统标识字段的方式。</p><p> 当您首次配置字段并键入标签时，会自动填充名称字段以匹配它。 但是“标签”和“名称”字段不同步，这使您能够自由更改用户看到的标签，而无需更改系统看到的名称。</p>
      <p><b>重要</b>：
      <ul> 
      <li>虽然可以这样做，但我们建议，在您或其他用户开始使用Workfront中的自定义表单后，不要更改此名称。 如果这样做，系统将不再识别现在可能在Workfront其他区域引用它的字段。</p> </li>
      <li> <p>每个字段名称在贵组织的Workfront实例中必须唯一。 这样，您就可以重复使用已经为其他自定义表单创建的表单。</p> </li>
      <li><p>我们建议您在自定义字段名称中不要使用句点/点字符，以防止在Workfront的不同区域使用字段时出错。</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">说明</td> 
      <td> <p>键入有关该字段的任何其他信息。 当用户填写自定义表单时，可以将光标悬停在问号图标上，以查看包含您在此处键入的信息的工具提示。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">引用字段</td> 
      <td><p>（必需）选择Workfront原生字段。<p><p>仅表单对象的本机字段可用。 例如，如果表单设计器顶部的“对象类型”列表显示“项目”，则您将能够选择项目的本机字段，但不能选择特定于任务的字段。</p></td>
     </tr>
     <tr> 
      <td role="rowheader">大小</td> 
      <td>（可选）根据需要更改字段的显示大小。</td> 
     </tr> 
    </tbody> 
   </table>

1. 要保存更改，请单击 **应用** 并转到另一个部分以继续构建您的表单。

   或

   单击&#x200B;**保存并关闭**。

</div>

突出显示后的文本

## UGP-10566 — 链接文本小于HTML表中的常规文本

另见UGP-9780

<table style="table-layout:auto"> 
<tbody> 
<tr>
<td>输入到</td>
<td>描述</td>
<td>可用于 </td>
</tr>
<tr> 
    <td role="rowheader">标签</td> 
    <td> <p>（必需）键入要显示在自定义字段上方的描述性标签。 您可以随时更改标签。 有关更多信息，请参阅 <a href="https://www.adobe.com/cn" class="MCXref xref">将自定义字段添加到自定义表单</a> 本文章中。</p> <p><b>重要</b>：避免在此标签中使用特殊字符。 它们在报表中无法正确显示。</p> </td> 
    <td>
    <ul>
    <li>单选按钮。 有关更多信息，请参阅 <a href="https://www.adobe.com/cn">将自定义字段添加到自定义表单</a> 本文章中。 （无类）</li>
    <li>复选框组</li>
    <li>下拉列表</li>
    </ul></td>
</tr> 
</tbody> 
</table>

## UGP-9176 — 旧错误

“span”标记在NOTE（和列表）中无法正常工作

有关新的注释体验中可用的功能以及哪些对象的信息，请参阅 [新的评论体验](note-test.md).

1. 转到要向其添加回复的对象。
1. 单击 **更新**，然后单击 **评论** 选项卡，并查找要回复的注释或回复

   或

   <span class="preview">单击 **全部** 选项卡，然后单击 **在评论中回复** 在“注释”选项卡中打开注释并回复注释。 您不能在“全部”选项卡中回复。</span>

1. （可选）要在回复中包含来自先前更新的文本，请单击 **更多** 菜单，然后单击 **引用回复**. 上次更新的文本会显示在输入区域中，以垂直灰色线标记。
1. 单击 **回复**.

   ![](assets/package.png)

   您可以在页面底部看到积极参与对话的用户 **添加回复……** 框后，您可以添加更多内容，或删除不再相关的内容。 这些用户以及订阅了对象的任何用户将在对对象进行更新或回复时收到通知。 您还可以标记更多用户以将其包含在回复中。  要标记更多用户，请参阅 [为其他人标记更新](note-test.md).

   >[!TIP]
   >
   >   要向现有回复添加其他回复，您可以开始键入 **添加回复……** 框，或单击 **回复** 在原始注释上。 您的回复将添加到线程的末尾。

1. 开始键入回复，并使用富文本工具栏中的任何其他选项。 有关使用富文本或其他更新功能的信息，请参阅 [更新工作](note-test.md).

1. 单击 **提交** 以保存回复。

1. （可选）单击 **更多** 菜单，了解更多用于管理回复的选项。 有关更多信息，请参阅 [更新工作](note-test.md).


## UGP-10614 — 带图像的问题表

我觉得 `{width="20"}` 参数导致表格中出现问题。

## 比较 Expert 与 Ultimate 成功计划

|  | Expert 成功计划 | Ultimate 成功计划 |
|--- |--- |--- |
|  | 加入 Expert 成功计划，即可获得有关针对关键业务问题的技术故障排除和指导的&#x200B;**全天候专家服务**。或者，可利用我们的自助资源、独家最佳实践以及 Adobe 专家和同行的网络社区找到快捷的解决方案。 <p> *所有 Adobe Experience Cloud 许可证都附带该计划。* | 加入 Ultimate 成功计划，即可体验&#x200B;**策略指导和主动监测技术运行状况以营造高效的数字体验**。将有一个专家团队支持您的 Adobe 环境，这些专家熟悉您的业务，并集中精力实施一个与您在业务影响方面的目标和优先级相符的路线图。 |
| **成功团队** | 支持工程师的联合团队 | 包括： <ul><li> 指定的技术客户经理 </li><li> 指定的客户成功经理 </li><li> 指定的支持服务经理</li><li> 提供各种成功加速器的技术工程师和策略专家的联合团队 </li><li> 支持工程师的联合团队 </li></ul> |
| **主动的技术和运营支持** | ![不包括图标](../assets/Cross_red_circle.svg){width="20"}不包括 | 包括： <ul><li>升级和迁移审查、发布准备 </li><li>产品路线图审查</li><li> 协调一致的技术和策略路线图</li><li>关键事件准备和规划</li><li>规划相关且及时的赋能活动</li><li>技术方面的最佳实践和行业指导</li><li>支持产品团队/与产品团队保持一致</li><li>实现关键业务目标的统一计划 - 共同行动计划 (MAP)</li></ul> |
| **技术支持** | 包括： <ul><li>**P1**：全天候问题支持</li><li>**P2、P3、P4**：工作时间支持</li><li>标准停机管理</li><li>集中上报管理</li></ul> | 包括： <ul><li>**P1**：全天候问题支持</li><li>**P2/P3**：每周五天全天问题支持</li><li>**P4**：工作时间支持</li><li>优先停机管理</li><li>指定的专家上报管理</li></ul> |
| **成功加速器** | ![不包括图标](../assets/Cross_red_circle.svg){width="20"}不包括 | TAM 和 CSM 定期安排成功加速器<p>*（有关更多信息，请参阅成功加速器目录）* |
| **支持渠道** | 在线、电话、Experience League、论坛 | 个性化在线门户、优先电话、Experience League、论坛 |

{style="table-layout:fixed"}

## 支持附加功能

| 附加功能 | Expert 成功计划 | Ultimate 成功计划 |
|--- |--- |--- |
| **事件管理附加功能**<br>&#x200B;提供管理关键事件的整个生命周期所需的端到端领导和支持 | ![可用图标](../assets/Plus_blue.svg){width="20"}可用 | ![可用图标](../assets/Plus_blue.svg){width="20"}可用 |
| **技术客户总监附加功能**<br>&#x200B;您的首席技术资源，负责提供领导监督和高管参与事宜，并确保有效治理，以使您的业务成果最大化 | ![不可用图标](../assets/Cross_red_circle.svg){width="20"}不可用 | ![可用图标](../assets/Plus_blue.svg){width="20"}可用 |
| **高级云支持附加功能**<br>&#x200B;针对 Adobe Experience Manager as a Cloud Service 客户的顶级服务和价值保证 | ![可用图标](../assets/Plus_blue.svg){width="20"}可用 | ![可用图标](../assets/Plus_blue.svg){width="20"}可用 |
| **导师答疑附加功能**<br>&#x200B;通过适时培训方法提供技能型学习 | ![可用图标](../assets/Plus_blue.svg){width="20"}可用 | ![可用图标](../assets/green_checkmark.svg){width="20"}包括 |
| **开发者提升附加功能**<br>&#x200B;提供与可协助进行维修工作的现场工程专家沟通的渠道 | ![可用图标](../assets/Plus_blue.svg){width="20"}可用 | ![包括图标](../assets/green_checkmark.svg){width="20"}包括 |
| **优先级队列捆绑插件**<br>&#x200B;免排队优先处理您的票据，并获得“导师会议”和“开发者加速”的额外访问权限 | ![可用图标](../assets/Plus_blue.svg){width="20"}可用 | ![包括图标](../assets/green_checkmark.svg){width="20"}包括 |

{style="table-layout:fixed"}
