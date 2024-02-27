---
title: 表格
description: 使用Markdown表和HTML表。
hide: true
hidefromtoc: true
source-git-commit: cd9f841a3f720ee366b33f3a78f7ca731c0b865a
workflow-type: tm+mt
source-wordcount: '1420'
ht-degree: 3%

---

# 表格

马特一次又一次地来到这里

标准Markdown仅支持基本表。 对于AdobeDocs Markdown，您可以选择以下选项：

* 基本Markdown表
* HTML表
* 使用段落分隔符HTML语法有限的Markdown表(`<p>`)，换行符(`<br>`)和基本列表(`<ul>`， `<ol>`)。

## 将HTML表转换为Markdown表

在某些情况下，您需要将HTML表转换为Markdown表或Markdown文本。 您可能需要改进外观、解决验证错误，或者简化以后的编辑工作。

遗憾的是，我们未能找到一种能够很好地转换HTML表的工具。 我们通常使用一些工具组合来拼凑出一个不错的Markdown表格。

| 工具 | 作用 |
|--- |--- |
| [Markdown表格生成器](https://www.tablesgenerator.com/markdown_tables) | 适合从头开始创建Markdown表格。 |
| [高级表转换器](https://tableconvert.com/html-to-markdown) | 将表格从任何格式转换为任何格式。 <p>**注意：** 转换时，链接和图像将被拼合。 |
| [基本表html > markdown转换器](https://jmalarcon.github.io/markdowntables/) | 简单的HTML转换器 <p>**注意：** 转换时，链接和图像将被拼合。 |
| [非表HTML> Markdown转换器](https://codebeautify.org/html-to-markdown) | 将HTML表转换为非表Markdown语法。 与上述工具结合使用以复制链接、图像和任何其他展平项目。 |

## 基本Markdown表

* 确保在确定表属性的第二行中至少添加三个连字符。 示例： `|--- |--- |--- |` 用于3列表。
* Markdown表必须至少有一个标题行和一个正文行。 无法创建单行或单单元格Markdown表(请改用HTML)。
* 确保每行的管道字符(&amp;vert；)数量相同。 如果需要在表单元格中包含管道字符，请通过在它前面添加反斜杠(`\|`)或使用HTML实体代码(`&vert;`)。
* 在表中使用代码块时要小心。 内联代码块可能会导致列宽不成比例。
* 您可以通过指定“自动”或“固定”来更改表的呈现方式。 请参阅 [更改表的呈现方式](#table-rendering).

## 创建具有额外的HTML的Markdown表

为了便于迁移，我们已扩展Markdown表格以支持HTML段落分隔符(`<p>`)，换行符(`<br>`)和基本HTML列表(`<ul>` 和 `<ol>`)。

**带有换行符和列表的Markdown表**

```
| Header 1 | Header 2 | Header 3 |
|--- |--- |--- |
| Normal row | row 1 column 2 | row 1 column 3 |
| Line break | first line in cell<br>second line in cell | row 1 column 3 |
| Bullet list | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul> | row 2 column 3 |
| Bullet list with line break | Bullet list:<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul><br>This is a new line after the bullet list | row 2 column 3 |
```

**示例**

| 页眉1 | 页眉2 | 页眉3 |
|--- |--- |--- |
| 正常行 | row 1 column 2 | row 1 column 3 |
| 换行符 | 单元格中的第一行<br>单元格中的第二行 | row 1 column 3 |
| 项目符号列表 | 项目符号列表：<ul><li>第 1 项</li><li>第 2 项</li><li>第 3 项</li></ul> | row 2 column 3 |
| 带换行符的项目符号列表 | 项目符号列表：<ul><li>第 1 项</li><li>第 2 项</li><li>第 3 项</li></ul><br>这是项目符号列表后的新行 | row 2 column 3 |

>[!IMPORTANT]
>
>如果决定在本机表中使用HTML，请确保使用正确的HTML语法。 HTML语法中的错误会导致验证错误，这些错误难以理解。 仔细检查你的工作。

## 使用HTML表

迁移工具尝试从原始表中保留尽可能多的格式。 此HTML语法中的大多数都会被忽略，而此语法中的某些语法会导致验证错误。

**已迁移HTML表的示例**

```
<table> 
 <tbody>
  <tr>
   <th>Property</th> 
   <th>Type</th> 
   <th>Value Description</th> 
  </tr>
  <tr>
   <td>badgingPath</td> 
   <td>String[]</td> 
   <td><p><i>(Required)</i> A multi-value string of badge images up to the number of badgingLevels. The badge image paths must be ordered so the first is awarded to the highest expert. If there are less badges than indicated by badgingLevels, the last badge in the array fills out the rest of the array. Example entry:</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>Long</td> 
   <td><i><p>(Optional)</i> Specifies the levels of expertise to be awarded. For example, if there should be an <code>expert </code>and an <code>almost expert</code> (two badges), then the value should be set to 2. The badgingLevel should correspond with the number of expert-related badge images listed for the badgingPath property. Default is 1.</p></td> 
  </tr>
  <tr>
   <td>badgingType</td> 
   <td>String</td> 
   <td><p><i>(Required)</i> Identifies the scoring engine as either "basic" or "advanced". Set to "advanced" else the default is "basic".</p></td> 
  </tr>
 </tbody>
</table>
```

**已呈现**

<table> 
 <tbody>
  <tr>
   <th>属性</th> 
   <th>类型</th> 
   <th>值说明</th> 
  </tr>
  <tr>
   <td>徽章路径</td> 
   <td>String[]</td> 
   <td><p><i>（必需）</i> 徽章图像的多值字符串，最大数量为badgingLevels。 必须订购徽章图像路径，以便将第一个授予最高的专家。 如果徽章的数量少于badgingLevels所指示的数量，则数组中的最后一个徽章将填充数组的其余部分。 示例条目：</p><p> <code>/etc/community/badging/images/expert-badge/jcr:content/expert.png</code></p></td> 
  </tr>
  <tr>
   <td>badgingLevels</td> 
   <td>长</td> 
   <td><p><i>（可选）</i> 指定要授予的专业知识级别。 例如，如果应该有一个 <code>expert </code>和 <code>almost expert</code> （两个徽章），则值应设置为2。 badgingLevel应与badgingPath属性中列出的专家相关徽章图像数量相对应。 默认值为1。</p></td> 
  </tr>
  <tr>
   <td>徽章类型</td> 
   <td>字符串</td> 
   <td><p><i>（必需）</i> 将评分引擎标识为“基本”或“高级”。 设置为“高级”，否则默认值为“基本”。</p></td> 
  </tr>
 </tbody>
</table>

**何时使用HTML表**

* 以平衡列。
* 要忽略表标题（markdown表必须具有标题行），请执行以下操作：
* 要删除单行表的边框(`<tr style="border: 0;">`)。
* 添加列或行范围。
* 在表格单元格内对齐文本。

**使用HTML表的注意事项**

* 请勿在HTML表中使用Markdown语法。 例如，如果添加 `[!NOTE]` 对于HTML表，它将按原样呈现(`[!NOTE]`)。 请改用HTML语法来表示注释和图像等。

  Loc标记是此规则的例外，因为在呈现页面之前，UICONTROL和DNL标记会被去除。

* 表中并非所有HTML语法都受支持。 在EXL中呈现时，Width、height、color和其他HTML语法元素将被忽略。 您可以保留这些值，除非它们会导致验证错误。
* 要对齐文本，请使用 `align: "left|center|right"` HTML中。 例如，要将表单元格的内容居中，请使用 `<td align="center">`.
* HTML表不能包含嵌套表。

>[!TIP]
>
>如果要关闭单行HTML表的边框，请使用以下语法：
>
>```
><table>
><tr style="border: 0;">
>```

## 指定表的呈现方式 {#table-rendering}

我们可以通过两种方式呈现表格：

* **固定** （当前为默认值） — 包含用于呈现表的自定义规则，包括带有图像的HTML表。 表格呈现为全宽而没有滚动，这有时会导致文本重叠。
* **自动**  — 与Git-flavored Markdown (GFM)类似。 允许滚动表，因此文本不重叠。

在大多数情况下，这些表将以相同的外观呈现。 但是，如果您的表格包含重叠文本，则需要应用 `auto` 标记之前。 或者，如果包含图像卡的HTML表未正确呈现，则可能需要应用 `fixed` 标记之前。

我们正在考虑将默认设置从 `fixed` 到 `auto`.

## 编辑Markdown表格

如果要指定本机Markdown表的呈现方式，请在表后添加以下语法行之一，并在前后添加空白行：

* `{style="table-layout:auto"}`
* `{style="table-layout:fixed"}`

![表渲染](assets/table-render.png)

### 编辑HTML表

如果要指定HTML表的呈现方式，请在表的第一行中使用以下语法行之一：

* `<table style="table-layout:auto">`
* `<table style="table-layout:fixed">`

```
<table style="table-layout:fixed">
  <tr>
    <th>Month</th>
    <th>Savings</th>
  </tr>
  <tr>
    <td>January</td>
    <td>$100</td>
  </tr>
</table>
```

### 何时使用自动或固定

**重叠文本**

使用 `auto` 对于具有长代码块或导致文本重叠的文本的表，如果 `fixed` （默认）处于选中状态。

*固定（默认）*

| 分析量度 | 描述 | ID查询参数 |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | 一个数据集或所有数据集的无效“类型”消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.range.count** | 一个数据集或所有数据集的“范围”无效消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.format.count** | 一个数据集或所有数据集的“格式”无效消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.pattern.count** | 一个数据集或所有数据集的无效“模式”消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.presence.count** | 一个数据集或所有数据集的无效“存在”消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.enum.count** | 一个数据集或所有数据集的无效“枚举”消息总数。 | 数据集Id |

{style="table-layout:fixed"}

*自动*

| 分析量度 | 描述 | ID查询参数 |
| ---- | ---- | ---- |
| **timeseries.data.collection.validation.category.type.count** | 一个数据集或所有数据集的无效“类型”消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.range.count** | 一个数据集或所有数据集的“范围”无效消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.format.count** | 一个数据集或所有数据集的“格式”无效消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.pattern.count** | 一个数据集或所有数据集的无效“模式”消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.presence.count** | 一个数据集或所有数据集的无效“存在”消息总数。 | 数据集Id |
| **timeseries.data.collection.validation.category.enum.count** | 一个数据集或所有数据集的无效“枚举”消息总数。 | 数据集Id |

{style="table-layout:auto"}

**具有平衡图像的HTML表**

使用 `fixed` 用于需要平衡图像的HTML表，这些图像在 `auto` 已选中。 在本例中，图像大小相同，但中间列中有更多文本。

*自动*

<table style="table-layout:auto">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="潜在客户" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Adobe潜在客户的工作流</strong></a>
    </div>
    <em>主要作者的主编辑工作流。</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="不频繁" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>面向不常见用户的工作流</strong></a>
    </div>
    <em>不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="验证" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>验证</strong></a>
    </div>
    <em>了解如何解决验证错误。</em>
    <br>
  </td>
</tr>
</table>

*已修复（通过多种方式）*

<table style="table-layout:fixed">
<tr>
  <td>
    <a href="table-breaks.md">
    <img alt="潜在客户" src="assets/leads-home.png"/>
    </a>
    <div>
    <a href="table-breaks.md"><strong>Adobe潜在客户的工作流</strong></a>
    </div>
    <em>主要作者的主编辑工作流。</em>
    <br>
  </td>
  <td>
    <a href="syntax-style-guide.md">
      <img alt="不频繁" src="assets/infrequent.png">
    </a>
    <div>
    <a href="syntax-style-guide.md"><strong>面向不常见用户的工作流</strong></a>
    </div>
    <em>不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。 不是主笔吗？ 了解做出贡献的最简单方法。</em>
    <br>
  </td>
  <td>
    <a href="note-test.md">
      <img alt="验证" src="assets/validation.png">
    </a>
    <div>
    <a href="note-test.md"><strong>验证</strong></a>
    </div>
    <em>了解如何解决验证错误。</em>
    <br>
  </td>
</tr>
</table>
