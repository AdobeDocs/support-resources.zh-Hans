---
title: 折叠部分错误
description: UGP-13446可折叠部分未呈现，可能由于嵌入的页面选项卡所致
hide: true
hidefromtoc: true
source-git-commit: f2d8eb9125df5f542c1ed075348586965f4adaad
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 7%

---

# 可折叠部分

<http://jira.corp.adobe.com/browse/UGP-13446> UGP-13446可折叠部分未呈现，可能由于嵌入的页面选项卡所致

## 示例

第一个带有页面选项卡；第二个没有

### 选项2：使用页面选项卡

+++ 手动安装6.5.18.0 - 6.5.22.0的修补程序

**步骤1：下载并解压缩修补程序包**

- 从Adobe软件分发门户下载适用于[ - 6.5.226.5.18.0的](https://www.adobe.com/cn)修补程序
- 本地提取

**步骤2：导航到正确的版本文件夹**

- 根据环境中安装的Service Pack版本，转到匹配的文件夹。

  对于Service Pack 20，文件夹为：

  ```
  <extracted-hotfix>/SP20/
  ```

**步骤3：找到部署目录**

- 在JEE服务器上的AEM Forms上，转到：

  ```
  [AEM installation directory]/deploy
  ```

  示例：`adobe/adobe-experience-manager-forms/deploy`



**步骤4：更新和替换EAR文件**

>[!BEGINTABS]

>[!TAB JBoss]

1. 打开`adobe-core-jboss.ear`并将`adminui.war`替换为

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adminui.war
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/jboss/adminui.war`

1. 在`adobe-core-jboss.ear`内，转到`lib/`文件夹并将`adobe-uisupport.jar`替换为：

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 保存耳朵。 确保正确保存了更改。


1. 将`adobe-edcserver-jboss.ear`替换为

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-edcserver-jboss.ear
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/jboss/adobe-edcserver-jboss.ear`

1. 将`adobe-forms-jboss.ear`替换为

   ```
   adobe-xxe-configuration-hotfix/SP[version]/jboss/adobe-forms-jboss.ear
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/jboss/adobe-forms-jboss.ear`



>[!TAB WebLogic]

1. 打开`adobe-core-weblogic.ear`并将`adminui.war`替换为

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adminui.war
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/weblogic/adminui.war`

1. 在`adobe-core-weblogic.ear`内，将`adobe-uisupport.jar`替换为：

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 保存耳朵。 确保正确保存了更改。


1. 将`adobe-edcserver-weblogic.ear`替换为

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-edcserver-weblogic.ear
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-edcserver-weblogic.ear`

1. 将`adobe-forms-weblogic.ear`替换为

   ```
   adobe-xxe-configuration-hotfix/SP[version]/weblogic/adobe-forms-weblogic.ear
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/weblogic/adobe-forms-weblogic.ear`

>[!TAB WebSphere]

1. 打开`adobe-core-websphere.ear`并将`adminui.war`替换为

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adminui.war
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/websphere/adminui.war`

1. 在`adobe-core-websphere.ear`内，将`adobe-uisupport.jar`替换为：

   ```
   adobe-xxe-configuration-hotfix/SP[version]/adobe-uisupport.jar
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/adobe-uisupport.jar`

1. 保存耳朵。 确保正确保存了更改。


1. 将`adobe-edcserver-websphere.ear`替换为

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-edcserver-websphere.ear
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/websphere/adobe-edcserver-websphere.ear`

1. 将`adobe-forms-websphere.ear`替换为

   ```
   adobe-xxe-configuration-hotfix/SP[version]/websphere/adobe-forms-websphere.ear
   ```

   例如：`adobe-xxe-configuration-hotfix/SP20/websphere/adobe-forms-websphere.ear`

>[!ENDTABS]



**步骤5：使用`adobe-rightsmanagement-<appserver>-dsc.jar`更新**&#x200B;文件

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

例如：`adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**步骤6： WebSphere和WebLogic上的Document Security的其他配置**：

如果您使用的是Document Security(以前称为Rights Management)，请在启动AEM Forms服务器之前设置以下Java系统属性（JVM参数）：

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**步骤7：重新运行配置管理器**

- 启动配置管理器以重新部署更新的EAR并应用修补程序

+++

### 选项2：不带页面选项卡

+++ 手动安装6.5.18.0 - 6.5.22.0的修补程序

**步骤1：下载并解压缩修补程序包**

- 从Adobe软件分发门户下载适用于[ - 6.5.226.5.18.0的](https://www.adobe.com/cn)修补程序
- 本地提取

**步骤2：导航到正确的版本文件夹**

- 根据环境中安装的Service Pack版本，转到匹配的文件夹。

  对于Service Pack 20，文件夹为：

  ```
  <extracted-hotfix>/SP20/
  ```

**步骤3：找到部署目录**

- 在JEE服务器上的AEM Forms上，转到：

  ```
  [AEM installation directory]/deploy
  ```

  示例：`adobe/adobe-experience-manager-forms/deploy`



**步骤4：更新和替换EAR文件**

已删除页面选项卡

**步骤5：使用`adobe-rightsmanagement-<appserver>-dsc.jar`更新**&#x200B;文件

```
adobe-xxe-configuration-hotfix/SP[version]/<appserver>/adobe-rightsmanagement-<appserver>-dsc.jar
```

例如：`adobe-xxe-configuration-hotfix/SP20/jboss/adobe-rightsmanagement-jboss-dsc.jar`

**步骤6： WebSphere和WebLogic上的Document Security的其他配置**：

如果您使用的是Document Security(以前称为Rights Management)，请在启动AEM Forms服务器之前设置以下Java系统属性（JVM参数）：

```
-Dcom.adobe.forms.jee.services.allowDoctypeDeclaration=true
```


**步骤7：重新运行配置管理器**

- 启动配置管理器以重新部署更新的EAR并应用修补程序

+++

Fin
