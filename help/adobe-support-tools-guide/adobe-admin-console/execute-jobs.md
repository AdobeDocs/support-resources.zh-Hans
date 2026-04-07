---
title: 执行挂起的作业
description: 了解如何在Adobe Admin Console中执行待处理作业，以确保所有更改都应用于您的组织。
exl-id: 18549d19-7985-4a45-8894-e69836ddb23c
source-git-commit: 9085108231aaa46d8417d346686c211ea48f6b81
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# 执行挂起的作业

此功能适用于使用[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)的企业组织。

- [[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)中的更改分两个阶段完成：

   1. **编辑阶段**：对组织进行更改或分配产品。
   2. **执行阶段**：审阅并执行挂起的更改，以使它们生效。

- 若要确保在[[!DNL Global Admin Console]](https://helpx.adobe.com/enterprise/global-admin-console/adopt-global-administration.html)中所做的所有更改均已实施并生效，请选择&#x200B;**[!UICONTROL 作业执行]**&#x200B;选项卡，然后继续执行挂起的更改。

  登录到[[!DNL Global Admin Console]](https://global-admin-console.adobe.com/)。

## 更改的持久性和可见性

### 更改持久性

- 您可以注销并在以后返回，而不会丢失挂起的更改。
- 未执行的更改：
   - 将在30天后丢弃。
   - 会话结束时（例如关闭浏览器选项卡或窗口）会被清除。

> [!NOTE]
>
> 迅速执行重要更改以确保成功应用它们。

### 多个管理员和冲突

- 同一组织中的两名管理员：
   - 不要看到彼此未执行的更改。
   - 仅在以下时间后查看更改：
      - 执行，以及
      - 刷新显示或再次登录。
- 未执行的更改可能与已执行的更改冲突。

### 冲突处理

报告冲突：
- 在执行时，或者
- 数据刷新时（例如，注销并重新登录后）。

## 正在执行挂起的更改

作为全局管理员，您可以从&#x200B;**[!UICONTROL 作业执行]**&#x200B;选项卡查看和执行挂起的更改。

### 执行更改的步骤

1. 登录到[!DNL Global Admin Console]。
2. 从左侧导航面板中选择&#x200B;**[!UICONTROL 作业执行]**&#x200B;选项卡。
3. 查看挂起的更改。
4. 选择&#x200B;**[!UICONTROL 提交更改]**&#x200B;以执行这些更改。

提交作业后：

- 作业进入执行队列。
- 作业运行时，状态为&#x200B;**[!UICONTROL 挂起]**。
- Adobe建议一次只执行一个作业，以实现可预测性和更轻松的故障排除。

> [!IMPORTANT]
>
> 如果在执行过程中发生错误，则必须重新输入并重新提交任何未成功应用的更改。

### 长期运行的分配

如果产品分配需要超过12小时：
- 作业标记为&#x200B;**[!UICONTROL 失败]**。
- 该作业中的任何后续挂起任务都不会执行。

![个待处理作业](assets/pending-jobs.png)

## 取消正在运行的作业

您可以从&#x200B;**[!UICONTROL 作业执行]**&#x200B;选项卡取消当前正在执行的作业。

### 取消正在运行的作业的步骤

1. 登录到[!DNL Global Admin Console]。
2. 选择&#x200B;**[!UICONTROL 作业执行]**。
3. 选择&#x200B;**[!UICONTROL 取消正在运行的作业]**。

### 取消行为

1. 作业在当前步骤结束时停止。
2. 作业不会在步骤中间停止。
3. 某些步骤可能需要几分钟或几小时才能完成。
4. 在此期间，作业可能处于&#x200B;**[!UICONTROL 正在取消]**&#x200B;状态。

> [!NOTE]
>
> 计划取消，并了解当前步骤的完成可能会在作业停止时显着延迟。

## 查看作业历史记录

- 要查看过去30天内执行的作业，请执行以下操作：

   1. 登录到[!DNL Global Admin Console]。
   2. 选择&#x200B;**[!UICONTROL 作业执行]**。
   3. 滚动到页面底部。
   4. 选择&#x200B;**[!UICONTROL 最近的作业]**。

- 最近的作业显示：
   - 已提交&#x200B;**作业命令**。
   - 与执行关联的&#x200B;**错误**&#x200B;和&#x200B;**警告**。

> [!NOTE]
>
> 后续重命名或删除相关对象&#x200B;**不会影响**&#x200B;命令在作业历史记录中的显示方式。 历史记录反映提交时的状态。
