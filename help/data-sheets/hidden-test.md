---
title: 隐藏测试页面
description: 从搜索和目录中隐藏此页面
hide: true
hidefromtoc: true
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="下载 Premium"
badgeExam: label="考试 ADO-E903" type="neutral"
source-git-commit: 75bb972a5ada66343dfb8a406b1cf63a1071df31
workflow-type: ht
source-wordcount: '804'
ht-degree: 100%

---

# 隐藏测试页面

激活？下午 3:10 左右重新检查提交。是否将在下午 3:30 上线？

## 预览问题

以下段落无法在 VSC 预览中正确呈现。我不清楚为什么。

如果 [!DNL Adobe] 管理您的密码，则您可[在您的 Adobe 帐户中更改密码](https://helpx.adobe.com/cn/manage-account/using/change-or-reset-password.html){target="_blank"}。

## 注释类型

所有支持的注释类型。

>[!NOTE]
>
>这是标准 NOTE 块。

>[!TIP]
>
>这是标准提示。

>[!IMPORTANT]
>
>这是重要注释。

>[!WARNING]
>
>这是警告。

>[!CAUTION]
>
>这是提醒。

>[!ADMIN]
>
>这是呈现为 ADMINISTRATION 的管理员注释。仅限 EXL。

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

>[!MORELIKETHIS]
>
>* 页面 1
>* 页面 2

## 徽章

徽章是用作内容指示器的彩色标签。例如，可添加徽章以将文章标为 _Beta_ 或将部分标为 _Premium_。可更改徽章的颜色并关联 URL 和工具提示。

[!BADGE 徽章示例]

有两种类型 of 徽章，其中每个徽章的语法不尽相同：

* **元数据** - 在页面顶部附近显示徽章
* **内联** - 在语法所在的地方现实徽章

### 元数据徽章

在元数据中添加徽章语法将在文章中的页面标题 (H1) 上方放置徽章。

可使用 _badge1_ 或 _badge2_ 等为徽章命名。或者，还可更有创意（只要名称以 _badge_ 开头即可）。

元数据示例：

```
badgePremium: label="Premium" type="Positive" url="https://www.premium-product.com" tooltip="Download Premium"
badgeExam: label="Exam ADO-E903" type="neutral"
```

* **badgePremium：**&#x200B;此示例显示带 URL 和工具提示的 Premium 徽章。

* **badgeExam：**&#x200B;此示例显示带考试 ID 号的黑色徽章。

#### 内联徽章

在徽章自身所在的行上或在标题、表格或其他页面元素中指定徽章信息。

以下是带 beta 标签、蓝色、URL 和工具提示的内联徽章的语法：

`[!BADGE Beta]{type=Informative url="https://www.example.com" tooltip="Go to example.com"}`

### 可用的徽章颜色

徽章使用在 Adobe Spectrum 中定义的颜色：

| 类型 | 徽章 |
|---|---|
| 信息性（默认） | [!BADGE Beta]{type=Informative url="https://www.example.com"} |
| 正面 | [!BADGE 新增功能]{type=Positive url="https://www.example.com" tooltip="转到 example.com"} |
| 负面 | [!BADGE 已停用]{type=negative tooltip="此功能现已停止使用"} |
| 中性 | [!BADGE 可能]{type=Neutral tooltip="一位骑手摔下马..."} |
| 提醒 | [!BADGE 注意]{type=Caution tooltip="黄色状态"} |

语法示例

```
|Type|Badge|
|---|---|
|Informative (default)|[!BADGE Beta]{type=Informative url="https://www.example.com"}|
|Positive|[!BADGE New Feature]{type=Positive url="https://www.example.com" tooltip="Go to example.com"}|
|Negative|[!BADGE Discontinued]{type=negative tooltip="This feature is now end of life"}|
|Neutral|[!BADGE Maybe]{type=Neutral tooltip="A rider fell off the horse..."}|
|Caution|[!BADGE Attention]{type=Caution tooltip="Yellow status"}|
```

### 对徽章的要求

* 元数据中只允许有两个徽章。可配置此规则，请告知我们您是否需要例外情况。
* 仅徽章标签为必需。`type`、`url` 和 `tooltip` 参数为可选。`type` 参数决定颜色。通过 `url` 参数，用户单击徽章即可打开文章或页面。`tooltip` 参数在鼠标悬停时显示工具提示文本。
* 将徽章添加到 `TOC.md` 文件将在指南中的每篇文章上都显示该徽章。如果您为徽章指定 URL 以跳转到文章，请确保使用根链接（如 `/help/guide/article.md`）而非相对链接（如 `article.md`）表明不同文件夹中的文章。
* 将徽章添加到 `metadata-new.md` 将在存储库中的每篇文章上都显示该徽章。
* 对于元数据徽章，请确保在引号中引起所有值。对于内联徽章，请确保在引号中引起 `url` 和 `tooltip`。
* 有效的类型值包括&#x200B;*信息性*（默认，蓝色）、*正面*（绿色）、*负面*（红色）、*中性*（深灰色）和&#x200B;*提醒*（黄色）。
* 徽章标签已进行本地化。
* 如果指定了多个元数据徽章，则根据徽章名称（如 `badge1:` 或 `badgeWeb`）按字母顺序显示徽章。
* 如果要在新标签页中打开该 URL，请使用此语法：

  ```
  [!BADGE Open in new tab]{type=Negative url="https://www.adobe.com newtab=true" tooltip="Open adobe.com in new tab"}
  ```

  呈现效果：

  [!BADGE 在新标签页中打开]{type=Negative url="https://www.adobe.com newtab=true" tooltip="在新标签页中打开 adobe.com"}

## 文本突出显示

Workfront 团队要求可使用黄色突出显示以指示即将推出的功能的预览。其工作方式如下。

示例 1：

```
This entire paragraph should NOT be highlighted. <span class="preview"> This word is **bold** inside a highlighted sentence.</span> And this is just the last sentence.
```

呈现效果：

不应突出显示整个此段落。<span class="preview">突出显示的句子中的这个词为&#x200B;**粗体**。</span>而这就是最后一个句子。

示例 2：

```
Highlighting should start after this paragraph.

<div class="preview">

Start of DIV.

This is a new paragraph, then an image

![image](/help/data-sheets/assets/BusinessSupportThumbnail.png)

Last highlighted item.

</div>

Not highlighted
```

呈现效果：

突出显示应在此段落之后开始。

<div class="preview">

DIV 的开始。

这是新段落，然后是图像

![image](/help/data-sheets/assets/BusinessSupportThumbnail.png)

突出显示的最后一项。

</div>

不突出显示

## 代码块的语法突出显示

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