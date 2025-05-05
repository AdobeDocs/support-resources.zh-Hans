---
title: Self Service Excellence协作文档语法和格式指南
description: Markdown样式设置的基本简介
mini-toc-levels: 1
hide: true
hidefromtoc: true
exl-id: 9f15436b-156a-4c07-bfaf-8557cd948197
source-git-commit: 0c01084577891a2869a2f5538381ca952514ff9c
workflow-type: tm+mt
source-wordcount: '4305'
ht-degree: 13%

---

# Markdown语法样式指南

本页说明了用于使用Markdown (.md)格式创作数字体验技术文档的Markdown组件。 此页包括Adobe员工的详细信息。

EDS

请参阅此处：[Adobe.com](https://www.adobe.com/cn){rel=nofollow}

<!--
* You can [view a basic sample file](sample.md) or [view a sample file with advanced syntax examples](sample-full.md)
-->

>[!TIP]
>
>观看此[AdobeDocs Markdown视频](https://video.tv.adobe.com/v/26165)。

在大多数情况下，我们遵循标准的Git-Flavored Markdown (GFM)语法来设置文本格式。 但是，某些语法（例如水平线）不受支持，并且我们通过多种方式扩展了Markdown以满足我们的文档需求。

## 基本文本格式

Markdown中的段落不需要特殊语法。 在每个段落之间添加一个空白行。

要将文本格式设置为&#x200B;**bold**，请用两个星号将文本括起来：

```
This text is **bold**.
```

要将文本格式设置为&#x200B;*斜体*，请用一个星号将文本括起来：

```
This text is *italic*.
```

要将文本格式同时设置为&#x200B;***粗体和斜体***，请用三个星号括住文本：

```
This is text is both ***bold and italic***.
```

要忽略Markdown格式字符，请在该字符前使用`\`：

`This is not \*italicized\* type.`

已呈现：不是\*斜体\*类型。

## 徽章

进行中。 正在等待Loc。

<!--

See the [dev version of this article](https://experienceleague-dev.corp.adobe.com/docs/authoring-guide-exl/using/markdown/syntax-style-guide.html#badges) for an example. Or [this one](https://experienceleague-dev.corp.adobe.com/docs/internal-test/test/badge.html).

There are two ways to create badges:

* **Metadata badge** - Specify the badge information in metadata so that the badge appears above the title in the article. This is especially useful for adding a badge to all articles in a guide or repo via the TOC.md or metadata.me files.
* **Inline badge** - Specify the badge information on its own line or in a heading, table, or other page element.

![badge examples](assets/badge-examples.png)

**Badge syntax**

*Metadata*: `badge: "Beta Content" type="Informative" url="https://www.example.com" tooltip="Go to example.com"`

*Inline*: `[!BADGE Beta Content]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

**Examples**

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

**Rendered**

|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off his horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|

**More details**

* Only the badge label is required. The `type`, `url`, and `tooltip` parameters are optional. The `type` parameter determines the color. The `url` parameter lets users click the badge to open an article. The `tooltip` parameter displays the tooltip text on mouseover.
* If you want multiple badges to appear at the top of the page, use different badge names. For example, you can create badge names such as `badgeBeta` or `badgeWeb`. Example:

  ```
  badge1: "Beta"
  badge2: "Campaign Web"
  ```

* For metadata badges, make sure that all values are wrapped in quotes. For inline badges, make sure that `url` and `tooltip` are wrapped in quotes.
* Valid type values include *Informative* (default, blue), *Positive* (green), *Negative* (red), *Neutral* (dark gray), and *Caution* (yellow). 

-->

## 块引号

我们的创作系统使用区块引号语法（行首为`>`）来识别用于获取提示、注释和视频的自定义Markdown扩展。 通过在段落前添加`>`字符，可以创建实际的方括号。

>这是块引号。

```
>This is a blockquote quotation.
```

## 代码块（嵌入式）{#code-block}

**何时使用**

用于呈现句子中的内联代码。 非常适合调用不需要全屏代码块的Cookie名称、文件名、值或命令。

代码块中的内容按原样呈现且未本地化。 （此规则的唯一例外是``和``语法，在打包发布时剥离这些语法。）

对于不应验证的示例URL，也使用代码块： `https://www.example.com`

**语法**

代码块使用单个反撇号来封装要高亮显示的代码元素。

```
This is `inline code` within a paragraph of text.
```

**示例**

This is `inline code` within a paragraph of text.

>[!TIP]
>
>您还可以使用三个反撇号(&amp;amp；grave；&amp;amp；grave；&amp;amp；grave；)将文本换行，以创建内联代码块。 当需要引用内联代码块中的反撇号字符时，此功能特别有用。 示例：
>
>&amp;amp；grave；&amp;amp；grave；&amp;amp；grave；`Use a back tick (`&amp;amp；grave；`) for formatting`&amp;amp；grave；&amp;amp；grave；&amp;amp；grave；

## 代码块（受保护）

**何时使用**

使用代码块显示代码语法。 受防护的代码块使用三个反撇号来封装要高亮显示的代码元素。 在受防护的代码块上方和下方添加空白行。

请注意，代码块未本地化。

>[!TIP]
>
>在创建受防护的代码块时指定语言。 指定语言时，允许特定于该语言的语法突出显示，并为用户显示&#x200B;**复制**&#x200B;按钮。 如果您指定语言，也可以显示行号。

**语法**

在代码行前后使用三个反撇号(&amp;amp；grave；&amp;amp；grave；&amp;amp；grave； )。 确保打开和关闭的背面刻度缩进的空格数相同。 要获得最佳渲染，请指定代码语言。

&amp;amp；grave；&amp;amp；grave；&amp;amp；grave；`javascript`

**示例**

```javascript
var visitor = Visitor.getInstance("INSERT-MARKETING-CLOUD-ORGANIZATION ID-HERE", {
     trackingServer: "INSERT-TRACKING-SERVER-HERE", // same as s.trackingServer
     trackingServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE", // same as s.trackingServerSecure

     // To enable CNAME support, add the following configuration variables
     // If you are not using CNAME, DO NOT include these variables
     marketingCloudServer: "INSERT-TRACKING-SERVER-HERE",
     marketingCloudServerSecure: "INSERT-SECURE-TRACKING-SERVER-HERE" // same as s.trackingServerSecure
});
```

### 代码块的语法突出显示

Experience League 支持代码块的语法突出显示。确保在开始的那组反撇号之后指定 `java` 等语言以确保正确地突出显示语法。有关有效语言的列表，请参阅 [https://prismjs.com](https://prismjs.com/#supported-languages)。如果缺少任何语言，请记录 JIRA 工单。

### 代码块中的行编号

在语言之后添加 `{line-numbers="true"}` 以启用行编号。

具有行号的示例 (&grave;&grave;&grave;`html {line-numbers="true"}`)：

```html {line-numbers="true"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

**在第 _ 行上开始编号**

在行号语法之后添加 `start-number="n"` 以从 1 以外的数字开始编号。

具有新起始行的示例 (&grave;&grave;&grave;`html {line-numbers="true" start-line="7"}`)：

```html {line-numbers="true" start-line="7"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### 代码块中的行突出显示

在行号语法之后添加 `highlight="n"` 以突出显示代码块中的行。指定 `11-13, 16` 将突出显示第 11 行到第 13 行和第 16 行。

具有行突出显示的示例 (&grave;&grave;&grave;`html {line-numbers="true" start-line="7" highlight="11-13, 16"}`)：

```html {line-numbers="true" start-line="7" highlight="11-13, 16"}
<!DOCTYPE html>
<html>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>
<p>My second paragraph.</p>

</body>
</html>
```

### 代码块中的变量格式

代码块中不支持变量语法，如`<i>italic</i>`。 要指示可变文本，一个选项是使用尖括号`< >`。

## 可折叠部分

您可以创建默认隐藏的可折叠部分（有时称为&#x200B;**可折叠项**）。 用户可以单击标题以展开或折叠部分。

可折叠文本可用于简化复杂内容，例如简化常见问题解答页面或使用嵌套列表去除复杂过程的杂凑。 例如，您可以将子步骤折叠到“查看详细信息”部分中，而不是显示一组子步骤。

**语法**

```
+++See details
This is text inside a collapsible section.

* Bullet one
* Bullet two
* Bullet three

+++
```

**示例**

+++查看详细信息
这是可折叠部分中的文本。

* 项目符号1
* 项目符号2
* 项目符号3

+++

**注释**

+++* 请勿在可折叠部分内嵌套可折叠部分。 嵌套的可折叠部分无法正确呈现。 但是，它们不会导致验证失败，因此用户将看到嵌套节的``语法。
* 请确保在可折叠部分中添加项目符号列表和代码块等项目上方和下方的空白行，否则会出现验证错误。
* 可以在可折叠部分中添加标题，但不建议这样做。
* [折叠并不总是桌面上复杂内容的答案](https://www.nngroup.com/articles/accordions-complex-content/)
* 可折叠部分的一个历史缺点是&#x200B;**在页面**&#x200B;中查找(Ctrl/Cmd+F)会忽略折叠文本。 虽然在Safari中仍然如此，但在Chrome中不再如此；在页面中查找可检测Chrome中的折叠文本。
* 使用可折叠部分的[维护更新](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=en)页面的示例。

## 注释和备注

注释不会出现在渲染的帮助系统中。 使用注释为自己或其他作者留下注释。 也可以对文本的草稿部分使用注释。

对于注释，请记住，虽然未在帮助系统中呈现这些注释，但是编辑GitHub.com上的Markdown文件的用户仍可以看到这些注释。 请勿在注释中包含机密信息。

```
<!-- standard comment code -->

DO NOT USE the following:
<!--> bad comment syntax <-->
```

除非您正在编辑文档，否则您应该看不到此下面的文本（“您无法看到我”）。

<!--
You can't see me (unless you're editing in Git).
-->

**提醒：**&#x200B;评论（备注）未出现在面向公众的帮助文章中。 但是，它会出现在用户可以查看和编辑的面向公众的 Markdown 文件中。

>[!IMPORTANT]
>
>避免在块组件（如项目符号列表）中添加注释，尤其是嵌套的项目符号列表。 注释可以更改项目符号列表的呈现方式。
>
>在TOC.md文件中，不要注释掉TOC列表中间位置的行。 这可能会破坏目录列表并导致验证错误。 相反，将目录中的注释移动到文件末尾。

## CONTEXTUALHELP

作者可以与产品团队合作，在Experience Cloud或Experience Platform产品UI中添加帮助弹出框。 示例：

```markdown
>[!CONTEXTUALHELP]
>id="platform_destinations_activate_mandatorykey_4"
>title="About mandatory attributes"
>abstract="Select the XDM schema attributes that all exported profiles should include. Profiles without the mandatory key are not exported to the destination. Not selecting a mandatory key exports all qualified profiles regardless of their attributes."
>additional-url="http://www.adobe.com/go/destinations-mandatory-attributes-en" text="Learn more in documentation"
```

## 定义列表

对于定义列表，我们尚不支持标准Markdown语法。 请改用手动格式设置，例如：

```
**Frog** - An amphibious green creature. Likes flies.
```

呈现效果：

**青蛙** — 两栖绿色生物。 喜欢苍蝇。

<!--
A definition list is a Markdown extension that supports the Definition List component in AEM. A definition list consists of a term and its definition.

**When to use**

Using a definition list is optional. To define lists of features or options, you can use either the definition list syntax or use basic Markdown formatting, such as applying bold to option names.

**Syntax**

```
Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
```

**Example**

Frog
: An amphibious green creature. Likes flies.

Cat
: A less amphibious creature than frogs.
-->

## 下载文件

将.zip或其他可下载文件上传到assets目录，然后链接到它。 如果它是.zip文件，则单击该链接将下载该文件。 如果文件类型(如PDF或PNG)可以在浏览器中打开，则单击该链接将打开一个新选项卡。 对于此类文件，请考虑压缩它们或提供右键单击链接和下载的说明。

`Download` &amp;amp；lbrack；`download-test.zip`&amp;amp；rbrack；`(assets/download-test.zip)`

呈现效果：

下载[下载测试zip](assets/download-test.zip)

>[!NOTE]
>
>下载文件和图像的最大文件大小为100 MB。 这就是github.com的限制。 git.corp.adobe.com限制更高(250 MB)，但我们需要能够将文件复制到github.com镜像。

## 标题 {#headings}

在Markdown中，使用井号(`#`)标识标题级别。 第一级(`#`)是文章标题，该标题也在元数据标题中指定 — 请保持这些相同。 第二级(`##`)表示将包含在mini-TOC中的页面上的主标题。 如果您习惯使用AEM (chl-author)进行编写，则2级标题(`##`)将映射到AEM中的“标题1”组件。

标题的最大字符数：69个字符（英语）/120个字符(LOC)。

```
# This is level 1 (article title)

## This is level 2
   
### This is level 3
```

**标题最佳实践**

* 确保每篇文章中的元数据后面都有一行空白的1级标题(`#`)。
* 请勿跳过级别，例如从级别2 (`##`)跳到级别4 (`####`)。
* 每个标题在&#x200B;*之前*&#x200B;和&#x200B;*之后*&#x200B;均包括空白行。
* 如果标题包含数字，请指定不以数字开头的显式标题ID，如`## Release notes for 2016 {#release-notes-2016}`。
* 我们建议仅使用3个标题级别。 级别4及更高级别当前未正确呈现。
* 标题显示在右侧导航中，以便用户可以单击跳转到部分。 默认情况下，右侧导航中显示两个级别的标题。 如果要更改级别数，请使用`mini-toc-levels`元数据，如`mini-toc-levels: 3`。

**标题ID**

标题ID（也称为&#x200B;*锚点ID*）用于创建指向文章中分区的自定义深层链接。 要指定标题ID，请使用此格式：

```
## Creating processing rules {#processing-rules}
```

标题ID应小写并使用连字符。

如果没有为标题指定标题ID，则默认标题ID为“简写”（小写并连字）标题。 例如，`## Creating widgets and Such`标题将具有`#creating-widgets-and-such`锚点。

## HTML语法 {#html}

出于各种原因（包括安全性和可访问性），我们限制了可在Markdown中使用的HTML语法。 下表显示了支持的HTML语法。 此列表中没有的任何HTML语法都将导致验证错误。

```html
<table>
<tbody>
<td>
<tfoot>
<thead>
<th>
<tr>
<col>
<colgroup>
<p> (paragraph break)
<ul> (unordered list / numbered list)
<ol> (ordered list / bullet list)
<li> (list item)
<br> (line break)
<b>
<caption>
<i>
<strong> (bold)
<u> (underline)
<s> (strikethrough)
<span>
<sub> (subscript)
<sup> (superscript)
<a>
<img>
<div>
<em> (emphasis, italics)
<pre> (codeblock)
<code>
<codeblock>
```

<!--
Bob: Check above no space char. (ignore the space; I can't add a codeblock inside this codeblock)
-->

如果您希望将HTML语法添加到此列表，请记录票证或联系SSE团队。

## 图像 {#images}

对图像使用`![]()`语法。 括号`[ ]`包含替换文本，括号`( )`包含图像位置和可选悬停文本（工具提示）。 感叹号将图像与链接区分开来。

```
![alt text](assets/logo.png "Hover text")
```

![替换文本](assets/logo.png "悬停文本")

对于共享图像，您可以将图像放在根资源文件夹中，然后使用可从存储库内任何文件工作的根链接：

```
/help/assets/imagename.png
```

### 调整图像大小和对齐

**图像属性（使用右对齐的图像）** ![替换文本](assets/premium.png "高级悬停文本"){align="right"}

使用如下语法更改页面视图或表格单元格中的默认图像宽度或居中或右对齐图像。

```
![Dive image alt text](assets/maui-dive.jpg "Hover text - Maui dive width is 300 pixels and centered"){width="300" align="center"}
```

呈现效果：

Bob — 宽度=下方300像素

![潜水图像替换文本](assets/maui-dive.jpg "悬停文本 — Maui潜水宽度为300像素且居中"){width="300" align="center"}

* 对于大图像，我们建议您创建足够大的图像以适合页面宽度（至少640像素宽）进行缩放。 建议的宽度为1500像素。 无需创建大于2500像素或500 KB的图像。 图像的最大文件大小为100 MB。
* 对于小图像，请使用所需的宽度（以像素为单位）创建图像，或者使用width参数，如`{width="250"}` （像素）或`{width="50%"}` （查看区域的百分比，而不是原始图像大小）。 图像按比例缩放。 请注意，图像可以放大或缩小，因此请注意像素化。
* 在某些情况下，来自同一界面的图像在页面上看起来会不成比例，因为较宽的图像（例如工具栏）会按比例缩小，而较窄的图像（例如面板）则不会按比例缩小。 在这种情况下，请考虑缩小较宽的图像以提高视觉一致性。
* 您可以更改视图区域中图像的对齐方式。 使用`{align="center"}`或`{align="right"}`。 不支持`valign`参数。

>[!NOTE]
>
>图像的最大文件大小为100 MB。 这就是github.com的限制。 git.corp.adobe.com限制更高(250 MB)，但我们需要能够将文件复制到github.com镜像。

### 图像链接

如果要允许用户单击图像以跳转到其他页面，请使用此格式。

**语法**

```
[![image](assets/core-services_96.png)](https://www.adobe.com)
```

**示例**

单击此图像可转到Adobe网站。

[![图像](assets/core-services_96.png)](https://www.adobe.com/cn)

### 单击以缩放图像

使用`zoomable`参数允许用户单击图像以查看图像的放大版。 当用户将鼠标悬停在可缩放图像上时，指针将变为放大镜。 单击时，图像将展开到浏览器的整个宽度。 可以使用关闭按钮将其取消。

**示例**

![潜水图像](/help/data-sheets/hidden/assets/maui-dive.jpg "在Maui中潜水"){width="100" zoomable="yes"}

**语法**

```
![Diving image](/help/data-sheets/hidden/assets/maui-dive.jpg "Diving in Maui"){width="100" zoomable="yes"}
```

## 链接和交叉引用 {#links-and-cross-references}

外部链接是直接的，可以呈现为链接标题或纯URL。

```
[Adobe](https://www.adobe.com)
```

呈现效果：

[Adobe](https://www.adobe.com/cn)

如果将URL直接添加到文本，则不会自动将其转换为链接。 如果您希望URL显示为链接，请添加`< >`语法。 示例：

```
https://www.adobe.com

<https://www.adobe.com>
```

呈现效果：

https://www.adobe.com/cn

<https://www.adobe.com>

文章链接（交叉引用）可能更加复杂。

**选项1：标准相对链接**

以下是标准相对链接的外观：

```
See [Overview example article](collaborative-doc-instructions/overview.md)
```

路径名需要同时考虑源文件和目标文件的位置。 您可以使用所有相对链接操作数，如`./` （当前目录）、`../` （上一个目录）和`../../` （上一个目录）。

**选项2：根相对链接**

此类链接的优点是，它只需要考虑目标文件。 它可以从存储库中的任何源文件工作，而不管源文件位置如何。

```
/help/using/docile-rules/introduction.md
```

**深层链接**

要链接到文章中的标题，目标标题必须具有显式标题ID（也称为“锚点ID”）。 示例：

`## Creating audience segments {#creating-audience-segments}`

要链接到同一页面中的此标题，请使用标题ID作为链接：

`See [Creating audience segments](#creating-audience-segments)`

要从存储库中的其他文章链接到此标题，请在链接的末尾添加标题ID后缀：

`See [Audiences: Creating audience segments](audiences.md#creating-audience-segments)`

**在新标签页中打开**

如果您希望链接打开新选项卡，例如当您跳转到其他指南时，请使用链接中的`{target="_blank"}`属性。

示例：

`[See What's new](whats-new.md){target="_blank"}`

## 元数据

将元数据添加到Markdown文件的顶部。 元数据行（和空白行）之后的下一行必须是文章标题（#标题）。

```
---
title: Title for search optimization
description: This is the article description used for search optimization. Use common search keywords and synonyms.
---

# Article title
```

## 本地化标记： UICONTROL、DNL和DONOTLOCALIZE

我们所有的 Markdown 帮助内容最初都是使用机器翻译进行本地化的。如果帮助内容从未本地化，那么我们会保留机器翻译。不过，如果帮助内容以前已经本地化，那么在人工翻译过程中，机器翻译的内容将充当占位符。

## 更多与此类似的内容

使用“更多与此类似的内容”组件可在文章末尾显示相关链接。 在呈现时，MORELIKETHIS组件将呈现为“相关文章”（并以其他语言进行本地化）。

**语法**

![更多与此语法相似的内容](assets/morelikethis.png)

**示例**

>[!MORELIKETHIS]
>
>* [Article 1](https://helpx.adobe.com/cn/support/analytics.html)
>* [Article 2](https://helpx.adobe.com/cn/support/audience-manager.html)

## 注释/告诫

我们扩展了Markdown以格式化各种类型的注释：注释、提示、重要和警告。

**语法**

```
>[!NOTE]
>
>This is a standard NOTE block.
```

**示例**

>[!NOTE]
>
>这是标准 NOTE 块。

**语法**

```
>[!TIP]
>
>This is a standard tip.
```

**示例**

>[!TIP]
>
>这是标准提示。

**语法**

```
>[!WARNING]
>
>This is a standard warning block.
```

**示例**

>[!WARNING]
>
>这是一个标准的警告块。

**语法**

```
>[!IMPORTANT]
>
>This is a standard important block.
```

**示例**

>[!IMPORTANT]
>
>这是一个标准的重要区块。

**语法**

```
>[!NOTE]
>
>This is a standard NOTE block.
>
>It includes multiple paragraphs.
```

**示例**

>[!NOTE]
>
>这是标准 NOTE 块。
>
>它包括多个段落。

新的支持的注释类型：

>[!ADMIN]
>
>这是管理员注释。 仅限 EXL。

>[!AVAILABILITY]
>
>这是可用性注释。仅限 EXL。

>[!PREREQUISITES]
>
>这是先决条件注释。仅限 EXL。

>[!INFO]
>
>这是信息注释。仅限 EXL。

>[!ERROR]
>
>这是错误注释。仅限 EXL。

>[!SUCCESS]
>
>这是成功注释。仅限 EXL。

## 编号列表和项目符号列表 {#lists}

要创建编号列表，请在行首使用`1.`或`1)`，但选择一种方法并在文章中一致地使用它。 您无需指定编号。GitHub 会为您完成此操作。

编号列表中的每一步都使用编号`1`。

在列表之前和之后添加空白行。

**语法**

```
1. This is step 1.

1. This is the next step.

   1. This is a sub-step

   1. This is a sub-step

1. This is yet another step, the third.
```

**示例**

1. This is step 1.

   1. 子步骤

   1. 子步骤

1. This is the next step.

1. This is yet another step, the third.

要创建项目符号列表，请在行首使用`*`、`-`或`+`，但选择一种方法并在文章中一致地使用它。 （如果混合使用`*`和`+`等格式，则在签入文件时将会出现Markdown验证错误。）

**最佳实践：**&#x200B;将`*`用于项目符号。 Visual Studio Code为项目符号应用星号，因此使用星号更容易自动创建无序列表。 (您可能已经注意到TOC.md文件对列表使用了加号`+`。 这是移民留下的烂摊子。 任何有效的项目符号字符只要在文章中一致即可。)

**语法**

```
* First item in an unordered list.
* Another item.
* Here we go again.
```

**示例**

* First item in an unordered list.
* Another item.
* Here we go again.

您还可以在列表中嵌入列表并在列表项之间添加内容。 在列表项之间缩进内容以避免启动新列表。 步骤之间的项应缩进到文本的开头 — 3个空格表示编号列表，2个空格表示项目符号列表。

```
1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)
   
1. Make sure that your table looks like this: 

   | Hello | World |
   |---|---|
   | How | are you? |
   
1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.
   
1. Do another step.

   This is an indented line.
```

**示例**

1. Set up your table and code blocks.
1. Perform this step.

   ![screen](assets/core-services_96.png)

1. Make sure that your table looks like this:

   | Hello | World |
   |---|---|
   | How | are you? |

1. This is the fourth step.

   >[!NOTE]
   >
   >This is note text.

1. Do another step.

   这是缩进行。

注意：如果缩进得过深，例如6个空格而不是3个，则该行中的内容将被视为代码块。

## 阴影框

阴影框可用于从页面的其余部分设置内容的区域。 例如，Workfront团队喜欢添加包含文本、图像和代码示例的“示例”框来实现特定目的。 对于“自助”或“用例”部分，或者对于扩展的注释或提示，阴影框可能也很有用。

要创建阴影框，请在部分的开头添加`>[!BEGINSHADEBOX]`，在结尾添加`>[!ENDSHADEBOX]`。 这些开始和结束标记之间的所有内容都将具有灰色背景。 将标签添加到`BEGINSHADEBOX`(如`>[!BEGINSHADEBOX "Use Case]`是创建粗体阴影框标题的可选方式。 您还可以在下一行添加粗体文本或标题。

示例：

>[!BEGINSHADEBOX]

**正在删除HTML表中的边框**

在某些情况下，您可以使用HTML表来创建平衡设计，但不希望内容看起来像表格。 要关闭单行HTML表的边框，请使用以下语法：

```
<table>
<tr style="border: 0;">
```

>[!NOTE]
>
>不要过度使用。 对于普通表格，我们希望跨内容保持一致的设计。

![表提示](assets/table-no-border.png)

在三列表格中，您还可以添加`<td align="center">`和`<td align="right">`以平均将单元格内容分布到视图区域。 如果不是这样，我早就告诉你了。

这是阴影框的最后一行。

>[!ENDSHADEBOX]

## 代码片段和

要在存储库中的文章之间共享文本，请在`help`文件夹中创建一个`_includes`文件夹。 此`_includes`文件夹可以包含可从存储库中的其他文件引用（包括）的.md文件。 此外，此存储库中的`snippets.md`文件可以包含可从存储库中的任何文件引用的Head2锚点。

在snippets.md文件中引用H2： `{{id-name}}`

引用包含文件： `{{$include /help/_includes/filename.md}}`

## 表格

在Markdown中，表格可能会有问题。 从以前的创作系统迁移表时，会将简单表（每个单元格一行）格式化为本机Markdown表（首选）。 更多高级表的格式为HTML。

>[!TIP]
>
>观看[Markdown表格视频](https://video.tv.adobe.com/v/26220)

在Markdown中，原生表通常看起来更好。 将根据列的内容调整其大小。 HTML表使用等宽列呈现。

默认情况下，Markdown不支持在单元格中使用多个行或列表。 但是，我们扩展了Markdown表，以允许单元格中的多行（使用`<p>`或`<br>`）或基本列表（使用`<ul><li>`等）。

>[!IMPORTANT]
>
>将这些HTML代码添加到Markdown表中时要小心。 如果语法不正确，您会收到一个令人困惑的验证错误，该错误无法准确描述问题。 检查您的HTML语法以确保其格式正确。

不允许在任何表中使用：iframe、单元格范围、嵌入表。

不允许在本地Markdown表格中使用：嵌套列表或复杂列表。

查看[表](tables.md)

**语法**

```
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

**示例**

| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | row 1 column 2 | row 1 column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |

Markdown 中可轻松处理简单的表格。但是，如果表格单元格中包含多个段落或列表，就会很难处理。对于此类内容，我们建议使用不同的格式，例如标题和文本。

**带有段落分隔符和列表的Markdown表**

```
| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | first paragraph in cell<p>second paragraph in cell(`<p>`)<br>line break (`br`) | row 1 column 3 |
| row 2 | bullet list<ul><li>item 1</li><li>item 2</li><li>item 3</li></ul> | row 2 column 3 |
```

**示例**

| Header | Another header | Yet another header |
|------------|----------|----------------|
| row 1 | 单元格中的第一段<p>单元格(`<p>`)<br>换行符(`br`)中的第二段落 | row 1 column 3 |
| row 2 | 项目符号列表<ul><li>项目1</li><li>项目2</li><li>项目3</li></ul> | row 2 column 3 |

**带有换行符和伪列表的Markdown表**

使用手动项目符号可解决此问题。

```
| Color | Things to Do |
|--- |--- |
| Red | * Read <br> * Write <br> * Study |
| Blue | * Swim <br> * Run <br> * Lift <br> **Note**: Remember to train smart.|
```

**示例**

| 颜色 | 待办事项 |
|--- |--- |
| 红色 | *读取<br> *写入<br> *研究 |
| 蓝色 | *游泳<br> *运行<br> *提升<br> **注意**：请记住训练智能型。 |


## 选项卡

选项卡是位于区域顶部的可单击区域，可显示不同的内容。 单击某个选项卡时，将显示该选项卡的内容，并隐藏其他选项卡的内容。

要创建选项卡集，请在选项卡集的开头添加`>[!BEGINTABS]`，并在最后一个选项卡之后添加`>[!ENDTABS]`。 为每个选项卡部分添加`>[!TAB <tab title>]`标记，并将每个选项卡的内容添加到其下方。

**Tab语法**

```
>[!BEGINTABS]

>[!TAB iOS]

This content appears in the iOS tab.

>[!TAB Android]

This content appears in the Android tab.

>[!TAB Windows]

This content appears in the Windows tab.

>[!TAB MacOS]

This content appears in the MacOS tab.

>[!TAB Linux]

This content appears in the Linux tab.

>[!ENDTABS]
```

**已呈现**

>[!BEGINTABS]

>[!TAB iOS]

此内容显示在“iOS”选项卡中。

>[!TAB Android]

此内容显示在“Android”选项卡中。

>[!TAB Windows]

此内容显示在Windows选项卡中。

>[!TAB MacOS]

此内容显示在“MacOS”选项卡中。

>[!TAB Linux]

此内容显示在Linux选项卡中。

>[!ENDTABS]

**制表符备注**

* 用户无法使用页面内搜索(Ctrl+F/Cmd+F)在未显示的选项卡中查找内容。
* 如果选项卡标题超出用户浏览器中的页面视图宽度，则会显示水平滚动条。
* 不能设置选项卡标题的格式。 您添加的任何语法都将作为标题的一部分传递。 例如，`>[!TAB **iOS**]`将显示为`**iOS**`。
* 可以在一个页面上创建多个选项卡集，但不能在另一个选项卡集中嵌套一个选项卡集。
* 着色背景将应用于选项卡集，以便用户能够看到将选项卡内容与其他内容区分开。

## 文本突出显示

Workfront 团队要求可使用黄色突出显示以指示即将推出的功能的预览。其工作方式如下。

示例：

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

呈现效果：

不应突出显示整个此段落。<span class="preview">突出显示的句子中的这个词为&#x200B;**粗体**。</span>而这就是最后一个句子。

作为一般规则，使用`<span class="preview">`突出显示段落中的段落或文本，并为多个段落和组件使用`<div class="preview">`。

>[!NOTE]
>
>我们仍在努力改进某些页面元素（如注释和表格）的突出显示显示。 如果您看到不正确的渲染，请随时记录JIRA错误。 进行中。
>
>VSC预览尚不支持高亮显示。

## 视频

视频不会在Markdown中以本机方式呈现。 要显示内联视频，请使用组件指示器`[!VIDEO]`，然后使用URL。

**语法**

```
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

**示例**

>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)

## 其他Markdown语法信息

### 扩展Markdown组件

我们需要扩展Markdown以支持常见Markdown中未包含的项目。

特殊组件在包含块引号中声明时，使用方括号、感叹号以及块类型参照。 例如，下面是如何声明注释：

```
>[!NOTE]
>
>This is a note.
```

* 注释（告诫），包括注释、重要、提示、警告和警告
* 嵌入式视频
* 更多此类内容（相关文章）
* 用于本地化的各种UI标记
* 标题、图像和代码块的组件属性
* 可折叠部分
* 文本突出显示
* 页面选项卡

在每行的开头使用Markdown块引用( `>` )可将基于段落的组件（如注释）绑定在一起。 要改善预览，请在节的开头后立即添加一个仅具有块引号(`>`)的行。 要结束部分，请添加一个空白行。

如果需要在组件中使用子组件，请为该子组件部分添加额外级别的块引用(`>  >`)。 例如，DONOTLOCALIZE部分中的NOTE应以`>  >`开头。

在某些情况下，我们需要支持Markdown元素的特定设置，例如标题。 如果需要更改默认设置，请将参数添加到组件后面的大括号`{# }`中。

### 空白行

您可以将一些喘息空间添加到带有空白行的文本墙上。 使用`<br>&nbsp;`作为解决方法以添加空白行。

示例：这是可能非常长的文本的第一句。 让我在此段落和下一段落之间插入一个空白行。

<br> 

这看起来可能不太令人印象深刻，但当你感觉自己的页面太拥挤时，可以尝试使用空白行。

### 用于“转义”的字符 {#characters-to-escape}

多个字符(`# { } [ ] < > * + - . !`)在Markdown或HTML中具有特殊的含义，可用于创建标题、图像、列表和其他组件。 使用这些字符时，渲染引擎认为您正在添加代码。 但是，在某些情况下，您希望在文本中显示这些字符。 要实现此目的，您需要“转义”字符。 最简单的转义方法是在字符前面加上反斜杠(`\`)。 例如，如果要以`#`字符作为行首以便不将其解释为标题，则应键入`\#`：

`\# This is not a heading`

**已呈现：**

\#这不是标题

反斜杠仅适用于以下字符： `# { } [ ] * + - . !`。 如果需要转义字符(如尖括号（如`<yourname>`）)，您可以用反撇号将文本括起来以应用内联代码块，或者使用HTML实体代码而不是字符。 常见HTML代码示例：

* `&lt;` (&lt;)
* `&gt;` (>)
* `&amp;` (&amp;)
* `&Hat;` (^)
* `&mdash;` (—)
* `&ndash;` (-)

[Freeformatter网站](https://www.freeformatter.com/html-entities.html)上提供了HTML实体的完整列表。 这将允许您查找所有特殊字符。

>[!NOTE]
>
>对于链步骤，例如“选择文件>另存为”，您无需转义`>`字符，因为它不位于其他字符旁边。 对于变量（如`<filename>`），您需要使用代码块`backticks`或字符代码(`&lt;filename&gt;`)来转义尖括号。

如果在代码块中使用HTML实体，则实体文本不会转换为特殊字符。 例如，`&gt;`在代码块中显示为“ `&gt;`”而不是“ > ”。

要跳转反撇号(&amp;amp；grave； )，请使用`&grave;`或将反撇号插入三反撇号中，以包裹内联代码块。

### 不支持的项目

我们计划不支持一些Git风格的Markdown项目。 您使用的预览工具可能会启用其中的一些功能，但并不依赖这些功能。

**任务列表**

不支持

```
* [x] Set up Jersey Shore recording
* [x] Buy donuts with sprinkles
* [x] Take nap
* [ ] Wash ferret
```

**表情符号**

不支持

```
:bowtie:
```

**水平线**

不支持

```
***
```

**块引号**

我们使用块引号（`>`位于行的开头）来指示扩展Markdown语法，例如注释和视频，如下所述。 但您也可以使用`>`语法来创建块引用部分。

>[!NOTE]
>
>如果缩进得过深（如六个空格而不是三个空格），则内容将呈现为块引号。 使用适当的缩进量，以避免将内容错误地呈现为块引用。
