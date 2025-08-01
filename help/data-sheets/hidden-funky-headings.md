---
title: 标记库
description: 通过Granite、CQ和Sling标记库，可访问在模板和组件的JSP脚本中使用的特定函数
contentOwner: Guillaume Carlino
products: SG_EXPERIENCEMANAGER/6.5/SITES
topic-tags: platform
content-type: reference
solution: Experience Manager, Experience Manager Sites
hide: true
hidefromtoc: true
role: Developer
exl-id: d024b7e9-1e8e-4aa3-bbb8-7bc92d143a1f
source-git-commit: 3128bd389ee7998736993f7b17c9ac53d146e929
workflow-type: tm+mt
source-wordcount: '2458'
ht-degree: 0%

---

# 标记库{#tag-libraries}

通过Granite、CQ和Sling标记库，可访问在模板和组件的JSP脚本中使用的特定函数。

## **粗体标题**

以上是一个大胆的标题。

2025年7月31日

## *斜体标题*

这是上方的斜体标题。

## Granite标记库 {#granite-tag-library}

Granite标记库包含有用的函数。

在开发Granite UI组件的jsp脚本时，建议在脚本顶部包含以下代码：

```xml
<%@include file="/libs/granite/ui/global.jsp"%>
```

全局还声明Sling库。

```xml
<%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling" %>
```

### &lt;ui:includeClientLib> {#ui-includeclientlib}

`<ui:includeClientLib>`标记包含AEM html客户端库，该库可以是js、css或主题库。 对于不同类型的多个包含项（例如js和css），必须在jsp中多次使用此标记。 此标记是` [com.adobe.granite.ui.clientlibs.HtmlLibraryManager](https://helpx.adobe.com/experience-manager/6-5/sites/developing/using/reference-materials/javadoc/com/adobe/granite/ui/clientlibs/HtmlLibraryManager.html)`服务接口周围的方便包装。

它具有以下属性：

**类别** — 逗号分隔的客户端库类别的列表。 这包括给定类别的所有JavaScript和CSS库。 将从请求中提取主题名称。

等同于： `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeIncludes`

**主题** — 逗号分隔的客户端库类别的列表。 这包括给定类别的所有与主题相关的库（CSS和JS）。 将从请求中提取主题名称。

等同于： `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeThemeInclude`

**js** — 逗号分隔的客户端库类别的列表。 这包括给定类别的所有JavaScript库。

等同于： `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeJsInclude`

**css** — 逗号分隔的客户端库类别的列表。 这包括给定类别的所有CSS库。

等同于： `com.adobe.granite.ui.clientlibs.HtmlLibraryManager#writeCssInclude`

**主题** — 应包含仅指示主题库或非主题库的标志。 如果省略，则包含两个集。 仅适用于纯JS或CSS includes（不适用于类别或主题包含）。

`<ui:includeClientLib>`标记可在jsp中按如下方式使用：

```xml
<%-- all: js + theme (theme-js + css) --%>
<ui:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<ui:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<ui:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<ui:includeClientLib css="cq.collab.calendar, cq.security" />
```

## CQ标记库 {#cq-tag-library}

CQ标记库包含有用的函数。

要在脚本中使用CQ标记库，脚本必须以以下代码开头：

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %>
```

>[!NOTE]
>
>当`/libs/foundation/global.jsp`文件包含在脚本中时，将自动声明taglib。

在开发AEM组件的jsp脚本时，建议在脚本顶部包含以下代码：

```xml
<%@include file="/libs/foundation/global.jsp"%>
```

它声明了sling、CQ和jstl taglibs，并公开由[`<cq:defineObjects />`](#amp-lt-cq-defineobjects)标记定义的常规使用的脚本对象。 这会缩短并简化组件的jsp代码。

### &lt;cq:text> {#cq-text}

`<cq:text>`标记是一个便利的标记，可在JSP中输出组件文本。

它具有以下可选属性：

**属性** — 要使用的属性的名称。 该名称相对于当前资源。

**value** — 要用于输出的值。 如果此属性存在，则会覆盖属性属性的使用。

**oldValue** — 用于差异输出的值。 如果此属性存在，则会覆盖属性属性的使用。

**escapeXml** — 定义是否应将结果字符串中的字符&lt;、>、&amp;、&#39;和&#39;&#39;转换为相应的字符实体代码。 默认值为false。 转义在可选格式设置之后应用。

**格式** — 用于设置文本格式的可选java.text.Format。

**noDiff** — 隐藏差异输出的计算，即使存在差异信息也是如此。

**tagClass** — 将包围非空输出的元素的CSS类名称。 如果为空，则不会添加任何元素。

**tagName** — 将包围非空输出的元素的名称。 默认为DIV。

**占位符** — 在编辑模式下用于null或空文本的默认值，即占位符。 默认检查在可选格式化和转义之后执行，即按原样写入输出。 默认为：

`<div><span class="cq-text-placeholder">&para;</span></div>`

**默认值** — 用于Null或空文本的默认值。 默认检查在可选格式化和转义之后执行，即按原样写入输出。

如何在JSP中使用`<cq:text>`标记的一些示例：

```xml
<cq:text property="jcr:title" tagName="h2"/>
<cq:text property="jcr:description" tagName="p"/>

<cq:text value="<%= listItem.getTitle() %>" tagName="h4" placeholder="" />
<cq:text value="<%= listItem.getDescription() %>" tagName="p" placeholder=""/>

<cq:text property="jcr:title" value="<%= title %>" tagName="h3"/><%
    } else if (type.equals("link")) {
        %><cq:text property="jcr:title" value="<%= "\u00bb " + title %>" tagName="p" tagClass="link"/><%
    } else if (type.equals("extralarge")) {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h1"/><%
    } else {
        %><cq:text property="jcr:title" value="<%= title %>" tagName="h2"/><%

<cq:text property="jcr:description" placeholder="" tagName="small"/>

<cq:text property="tableData"
               escapeXml="false"
               placeholder="<img src=\"/libs/cq/ui/resources/0.gif\" class=\"cq-table-placeholder\" alt=\"\">"
    />

<cq:text property="text"/>

<cq:text property="image/jcr:description" placeholder="" tagName="small"/>
<cq:text property="text" tagClass="text"/>
```

### &lt;cq:setContentBundle> {#cq-setcontentbundle}

`<cq:setContentBundle>`标记创建了一个i18n本地化上下文并将其存储在`javax.servlet.jsp.jstl.fmt.localizationContext`配置变量中。

它具有以下属性：

**语言** — 要检索资源包的区域设置的语言。

**source** — 应从中获取区域设置的源。 可以将其设置为以下值之一：

* **static** — 区域设置取自`language`属性（如果可用），否则取自服务器默认区域设置。

* **page** — 区域设置获取自当前页面或资源的语言（如果可用），否则获取自`language`属性（如果可用），否则获取自服务器默认区域设置。

* **请求** — 区域设置取自请求区域设置(`request.getLocale()`)。

* **auto** — 区域设置取自`language`属性（如果可用），否则取自当前页面或资源的语言（如果可用），否则取自请求。

如果未设置`source`属性：

* 如果设置了`language`属性，`source`属性将默认为“ `static`”。

* 如果未设置`language`属性，`source`属性将默认为`auto`。

“内容包”可供标准JSTL `<fmt:message>`标记使用。 按键查找消息是双重的：

1. 首先，将搜索渲染的基础资源的JCR属性以查找翻译。 这允许您定义一个简单的组件对话框来编辑这些值。
1. 如果节点不包含与键完全相同的名称属性，则回退是从sling请求( `SlingHttpServletRequest.getResourceBundle(Locale)`)加载资源捆绑。 此包的语言或区域设置由`<cq:setContentBundle>`标记的语言和源属性定义。

`<cq:setContentBundle>`标记可在jsp中按如下方式使用。

对于定义其语言的页面：

```xml
... %><cq:setContentBundle source="page"/><%  %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

对于用户个性化页面：

```xml
... %><cq:setContentBundle scope="request"/><% %>
<div class="error"><fmt:message key="Hello"/>
</div> ...
```

### &lt;cq:include> {#cq-include}

`<cq:include>`标记包含当前页面中的资源。

它具有以下属性：

**刷新**

* 一个布尔值，定义是否在包含目标之前刷新输出。

**路径**

* 当前请求处理中包含的资源对象的路径。 如果此路径是相对路径，则会将其附加到当前资源的路径，该资源的脚本包含给定资源。 必须指定path和resourceType或脚本。

**resourceType**

* 要包含的资源的资源类型。 如果设置了资源类型，则路径必须是资源对象的确切路径：在这种情况下，不支持向路径添加参数、选择器和扩展。
* 如果要包含的资源使用无法解析为资源的路径属性指定，则标记可能会创建路径之外的合成资源对象以及此资源类型。
* 必须指定path和resourceType或脚本。

**脚本**

* 要包含的jsp脚本。 必须指定path和resourceType或脚本。

**ignoreComponentHierarchy**

* 一个布尔值，用于控制是否应忽略组件层次结构以实现脚本解析。 如果为true，则仅遵循搜索路径。

**示例：**

```xml
<%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><div class="center">
    <cq:include path="trail" resourceType="foundation/components/breadcrumb" />
    <cq:include path="title" resourceType="foundation/components/title" />
    <cq:include script="redirect.jsp"/>
    <cq:include path="par" resourceType="foundation/components/parsys" />
</div>
```

您应该使用`<%@ include file="myScript.jsp" %>`或`<cq:include script="myScript.jsp" %>`来包含脚本吗？

* `<%@ include file="myScript.jsp" %>`指令通知JSP编译器将完整文件包含到当前文件中。 就好像将所包含文件的内容直接粘贴到原始文件中一样。
* 使用`<cq:include script="myScript.jsp">`标记时，文件在运行时包含。

您应该使用`<cq:include>`还是`<sling:include>`？

* 在开发AEM组件时，Adobe建议您使用`<cq:include>`。
* `<cq:include>`允许您在使用脚本属性时直接按名称包含脚本文件。 这考虑到了组件和资源类型继承，通常比使用选择器和扩展严格遵守Sling的脚本解析更简单。

### &lt;cq:includeClientLib> {#cq-includeclientlib}

>[!CAUTION]
>
>`<cq:includeClientLib>`自AEM 5.6起已弃用。应改用`<ui:includeClientLib>`。

`<cq:includeClientLib>`标记包括AEM html客户端库，该库可以是js、css或主题库。 对于不同类型的多个包含项（例如js和css），必须在jsp中多次使用此标记。 此标记是`com.day.cq.widget.HtmlLibraryManager`服务接口周围的方便包装。

它具有以下属性：

**类别** — 逗号分隔的客户端库类别的列表。 这包括给定类别的所有JavaScript和CSS库。 将从请求中提取主题名称。

等同于： `com.day.cq.widget.HtmlLibraryManager#writeIncludes`

**主题** — 逗号分隔的客户端库类别的列表。 这包括给定类别的所有与主题相关的库（CSS和JS）。 将从请求中提取主题名称。

等效于：`com.day.cq.widget.HtmlLibraryManager#`writeThemeInclude

**js** — 逗号分隔的客户端库类别的列表。 这包括给定类别的所有JavaScript库。

等同于： `com.day.cq.widget.HtmlLibraryManager#writeJsInclude`

**css** — 逗号分隔的客户端库类别的列表。 这包括给定类别的所有CSS库。

等同于： `com.day.cq.widget.HtmlLibraryManager#writeCssInclude`

**主题** — 应包含仅指示主题库或非主题库的标志。 如果省略，则包含两个集。 仅适用于纯JS或CSS includes（不适用于类别或主题包含）。

`<cq:includeClientLib>`标记可在jsp中按如下方式使用：

```xml
<%-- all: js + theme (theme-js + css) --%>
<cq:includeClientLib categories="cq.wcm.edit" />

<%-- only js libs --%>
<cq:includeClientLib js="cq.collab.calendar, cq.security" />

<%-- theme only (theme-js + css) --%>
<cq:includeClientLib theme="cq.collab.calendar, cq.security" />

<%-- css only --%>
<cq:includeClientLib css="cq.collab.calendar, cq.security" />
```

### &lt;cq:defineObjects> {#cq-defineobjects}

`<cq:defineObjects>`标记公开以下定期使用的脚本对象，开发人员可以引用这些对象。 它还公开由[`<sling:defineObjects>`](#amp-lt-sling-defineobjects)标记定义的对象。

**componentContext**

* 请求的当前组件上下文对象(com.day.cq.wcm.api.components.ComponentContext接口)。

**组件**

* 当前资源的当前AEM组件对象(com.day.cq.wcm.api.components.Component interface)。

**currentDesign**

* 当前页面的当前设计对象(com.day.cq.wcm.api.designer.Design界面)。

**当前页面**

* 当前的AEM WCM页面对象(com.day.cq.wcm.api.Page接口)。

**currentStyle**

* 当前单元格的当前样式对象(com.day.cq.wcm.api.designer.Style接口)。

**设计器**

* 用于访问设计信息的设计器对象(com.day.cq.wcm.api.designer.Designer接口)。

**editContext**

* AEM组件的编辑上下文对象(com.day.cq.wcm.api.components.EditContext接口)。

**页面管理器**

* 用于页面级操作的页面管理器对象(com.day.cq.wcm.api.PageManager接口)。

**pageProperties**

* 当前页面的页面属性对象(org.apache.sling.api.resource.ValueMap)。

**属性**

* 当前资源的属性对象(org.apache.sling.api.resource.ValueMap)。

**资源设计**

* 资源页的设计对象(com.day.cq.wcm.api.designer.Design接口)。

**resourcePage**

* 资源页面对象(com.day.cq.wcm.api.Page接口)。
* 它具有以下属性：

**requestName**

* 继承自sling

**responseName**

* 继承自sling

**资源名称**

* 继承自sling

**nodeName**

* 继承自sling

**日志名称**

* 继承自sling

**resourceResolverName**

* 继承自sling

**slingName**

* 继承自sling

**componentContextName**

* 特定于wcm

**editContextName**

* 特定于wcm

**属性名称**

* 特定于wcm

**pageManagerName**

* 特定于wcm

**currentPageName**

* 特定于wcm

**resourcePageName**

* 特定于wcm

**pagePropertiesName**

* 特定于wcm

**componentName**

* 特定于wcm

**designerName**

* 特定于wcm

**currentDesignName**

* 特定于wcm

**resourceDesignName**

* 特定于wcm

**currentStyleName**

* 特定于wcm

**示例**

```xml
<%@page session="false" contentType="text/html; charset=utf-8" %><%
%><%@ page import="com.day.cq.wcm.api.WCMMode" %><%
%><%@taglib prefix="cq" uri="https://www.day.com/taglibs/cq/1.0" %><%
%><cq:defineObjects/>
```

>[!NOTE]
>
>当脚本中包含`/libs/foundation/global.jsp`文件时，将自动包含`<cq:defineObjects />`标记。

### &lt;cq:requestURL> {#cq-requesturl}

`<cq:requestURL>`标记将当前请求URL写入JspWriter。 两个标记[`<cq:addParam>`](#amp-lt-cq-addparam)和[`<cq:removeParam>`](#amp-lt-cq-removeparam)可用于此标记正文中，以便在写入当前请求URL之前对其进行修改。

利用该区域，可使用各种参数创建指向当前页面的链接。 例如，它使您能够转换请求：

`mypage.html?mode=view&query=something`到`mypage.html?query=something`。

使用`addParam`或`removeParam`只会更改给定参数的出现次数，所有其他参数不受影响。

`<cq:requestURL>`没有任何属性。

示例：

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:addParam> {#cq-addparam}

`<cq:addParam>`标记将具有给定名称和值的请求参数添加到封闭[`<cq:requestURL>`](#amp-lt-cq-requesturl)标记中。

它具有以下属性：

**name**

* 要添加的参数的名称

**值**

* 要添加参数的值

**示例：**

```xml
<a title="filter results" href="<cq:requestURL><cq:addParam name="language" value="${bucket.value}"/></cq:requestURL>">${label} (${bucket.count})</a>
```

### &lt;cq:removeParam> {#cq-removeparam}

`<cq:removeParam>`标记从封闭[`<cq:requestURL>`](#amp-lt-cq-requesturl)标记中删除具有给定名称和值的请求参数。 如果未提供任何值，则删除具有给定名称的所有参数。

它具有以下属性：

**name**

* 要删除的参数名称

示例：

```xml
<a href="<cq:requestURL><cq:removeParam name="language"/></cq:requestURL>">remove filter</a>
```

## Sling标记库 {#sling-tag-library}

Sling标记库包含有用的Sling函数。

在脚本中使用Sling标记库时，脚本必须以下列代码开头：

```xml
<%@ taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %>
```

>[!NOTE]
>
>当`/libs/foundation/global.jsp`文件包含在脚本中时，将自动声明sling taglib。

### &lt;sling:include> {#sling-include}

`<sling:include>`标记包含当前页面中的资源。

它具有以下属性：

**刷新**

* 一个布尔值，定义是否在包含目标之前刷新输出。

**资源**

* 要包含在当前请求处理中的资源对象。 必须指定资源或路径。 如果同时指定了两者，则资源优先。

**路径**

* 当前请求处理中包含的资源对象的路径。 如果此路径是相对路径，则会将其附加到当前资源的路径，该资源的脚本包含给定资源。 必须指定资源或路径。 如果同时指定了两者，则资源优先。

**resourceType**

* 要包含的资源的资源类型。 如果设置了资源类型，则路径必须是资源对象的确切路径：在这种情况下，不支持向路径添加参数、选择器和扩展。
* 如果要包含的资源使用无法解析为资源的路径属性指定，则标记可能会创建路径之外的合成资源对象以及此资源类型。

**replaceSelectors**

* 调度时，选择器将替换为此属性的值。

**addSelectors**

* 调度时，此属性的值将添加到选择器中。

**replaceSuffix**

* 在调度时，后缀将替换为此属性的值。

>[!NOTE]
>
>`<sling:include>`标记中包含的资源和脚本的分辨率与普通sling URL分辨率相同。 默认情况下，也会将当前请求中的选择器、扩展等用于包含的脚本。 它们可以通过标记属性进行修改：例如，`replaceSelectors="foo.bar"`允许您覆盖选择器。

示例：

```xml
<div class="item"><sling:include path="<%= pathtoinclude %>"/></div>
```

```xml
<sling:include resource="<%= par %>"/>
```

```xml
<sling:include addSelectors="spool"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include resource="<%= par %>" resourceType="<%= newType %>"/>
```

```xml
<sling:include replaceSelectors="content" />
```

### &lt;sling:defineObjects> {#sling-defineobjects}

`<sling:defineObjects>`标记公开以下定期使用的脚本对象，开发人员可以引用这些对象：

**slingRequest**

* SlingHttpServletRequest对象，提供对HTTP请求标头信息的访问权限 — 扩展标准HttpServletRequest — 并提供对特定Sling的项的访问权限，如资源、路径信息和选择器。

**slingResponse**

* SlingHttpServletResponse对象，为服务器创建的HTTP响应提供访问权限。 这与它所扩展的HttpServletResponse相同。**请求**
* 标准JSP请求对象，它是一个纯HttpServletRequest。**响应**
* 标准JSP响应对象，它是一个纯HttpServletResponse。

**resourceResolver**

* 当前ResourceResolver对象。 它与slingRequest.getResourceResolver()相同

。**sling**

* SlingScriptHelper对象，包含方便的脚本方法，主要是sling.include(&#39;/some/other/resource&#39;)，用于在响应中包含其他资源的响应（例如，嵌入标头html代码片段）和sling.getService(foo.bar.Service.class)，以检索Sling中提供的OSGi服务（类表示法，具体取决于脚本语言）。

**资源**

* 要处理的当前资源对象，具体取决于请求的URL。 它与slingRequest.getResource()相同。

**currentNode**

* 如果当前资源指向JCR节点（Sling中通常会出现这种情况），则可以直接访问Node对象。 否则，不会定义此对象。

**日志**

* 提供了一个SLF4J日志记录器，用于从脚本中登录到Sling日志系统，例如log.info（“执行我的脚本”）。

* 它具有以下属性：

**requestName**

**responseName**

**nodeName**

l **ogName resourceResolverName**

**slingName**

**示例：**

```xml
<%@page session="false" %><%
%><%@page import="com.day.cq.wcm.foundation.forms.ValidationHelper"%><%
%><%@taglib prefix="sling" uri="https://sling.apache.org/taglibs/sling/1.0" %><%
%><sling:defineObjects/>
```

## JSTL标记库 {#jstl-tag-library}

[JavaServer Pages标准标记库](https://www.oracle.com/java/technologies/java-server-tag-library.html)包含许多有用的标准标记。 核心、格式和函数taglibs由`/libs/foundation/global.jsp`定义，如下面的代码片段所示。

### /libs/foundation/global.jsp的提取 {#extract-of-libs-foundation-global-jsp}

```xml
<%@taglib prefix="c" uri="https://java.sun.com/jsp/jstl/core" %>
<%@taglib prefix="fmt" uri="https://java.sun.com/jsp/jstl/fmt" %>
<%@taglib prefix="fn" uri="https://java.sun.com/jsp/jstl/functions" %>
```

按前文所述导入`/libs/foundation/global.jsp`文件后，您可以使用`c`、`fmt`和`fn`前缀访问这些taglibs。 JSTL的官方文档位于[Java™ EE 5教程 — JavaServer Pages标准标记库](https://docs.oracle.com/javaee/5/tutorial/doc/bnakc.html)。
