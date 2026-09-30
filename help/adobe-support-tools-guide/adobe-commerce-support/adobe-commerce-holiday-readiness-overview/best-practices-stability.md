---
title: 最佳实践和稳定性
description: 最佳实践和稳定性建议，以帮助Adobe Commerce商家准备环境以进行高流量事件，例如假日季节。
feature-set: Commerce
feature: Support
solution: Commerce
role: Developer, Admin, Leader
TQID: 'https://experienceleague.adobe.com/iA6ioGYYgQSotPrPqujDBdRcjBLUQXMGXfwlcSMGjkM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: cdfd3bc1-dc23-5cf0-b965-d3c0c55cde67
    internal-label: Best Practices
  - id: 5a951749-fac9-5bc7-9a98-ebe4ff066437
    internal-label: Cloud
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: 3c398179-d35a-51ba-b317-6c5b95feef5e
    internal-label: Logs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 71589dd124714805fbf844540fb2d272433631ee
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 4%
---

# 最佳实践和稳定性

此部分提供有关准备Adobe Commerce环境（包括云基础架构上的Commerce和内部部署）的技术建议，以便开展假期之类的高流量活动。

>[!NOTE]
>
>标记为&#x200B;**（仅限Cloud）**&#x200B;的步骤适用于云基础架构上的Commerce。 大多数其他建议也适用于内部部署。

## 升级到最新版本的Adobe Commerce {#upgrade-to-latest-version-of-adobe-commerce}

确保您的网站不是位于不受支持的Adobe Commerce版本上，这可能会影响网站的性能，并增加安全问题的漏洞。 请升级到最新版本的Adobe Commerce，以便安全应对假日季节。

Adobe Commerce的[最新版本](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/release/notes/overview)包含许多[关键安全修复](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/release/notes/security-patches/overview)，包括增强功能和已缓解的问题，当从以前的版本升级时，这些修复将使您的项目受益。

有关不支持的Adobe Commerce版本的详细信息，请查阅[Adobe Commerce生命周期策略](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/release/planning/lifecycle-policy)。

## 安装最新的ECE-Tools和Quality Patch Tool (QPT) {#install-latest-ece-tools-and-quality-patch-tool-qpt}

确保使用`--with-dependencies`开关安装了最新的`ece-tools`模块及其依赖模块，以便为Adobe Commerce版本正确安装所有必需的云修补程序。 有关步骤，请参阅[更新ECE-Tools包](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/dev-tools/ece-tools/update-package)。

查看Quality Patches Tool中提供的修补程序列表，并确保应用了与Adobe Commerce版本兼容的性能修补程序。 请参阅[Quality Patches Tool：搜索修补程序](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/tools/quality-patches-tool/patches-available-in-qpt/patches-available-in-qpt-tool-overview)。

>[!NOTE]
>
>QPT适用于Adobe Commerce on Cloud Infrastructure和内部部署。 安装和使用命令在这两者之间有所不同 — 对于Cloud，QPT包含在ECE-Tools软件包中。

## 查看和清除日志文件 {#review-and-clean-log-files}

查看云环境中的日志文件（例如，`~/var/log`下的应用程序日志文件），并识别写入默认或自定义日志文件的任何频繁记录的记录。 有关详细信息，请参阅[查看和管理日志](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/develop/test/log-locations)。

* 查看以下默认日志文件并修复重复出现的错误： `~/var/log`、`~/var/log/exception.log`、`~/var/log/support_report.log`、`~/var/log/system.log`、`~/var/report`。
* 删除之前为排除过去的问题而添加的调试日志。

这些日志也在[!DNL New Relic]中可用，请参阅[New Relic日志管理](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/monitor/new-relic/log-management)。

## 监控磁盘大小增长 {#monitor-disk-size-growth}

您在云基础架构上的Adobe Commerce有两个主磁盘卷。 监视这些卷，以确保它们在流量较大时具有足够的可用空间。 当任一卷的使用率超过70%时，Adobe Commerce会发出警告。

* `/mnt/shared` （共享文件，包括日志和媒体文件）
* `/data/mysql` （数据库卷）

有关详细信息，请参阅[管理磁盘空间](https://experienceleague.adobe.com/zh-hans/docs/commerce-on-cloud/user-guide/develop/storage/manage-disk-space)。

## 查看最慢的数据库请求 {#review-slowest-database-requests}

请务必定期监视和查看[!DNL New Relic]中最耗时的数据库事务。 调查明显缓慢的查询和组件。

* **检查最耗时的事务：**&#x200B;转到&#x200B;**[!UICONTROL New Relic]** > **[!UICONTROL APM和服务]** >选择环境> **[!UICONTROL 数据库]**，然后按最耗时的事务排序。

* **检查MySQL慢查询日志：**&#x200B;查看`mysql-slow.log`系统记录的慢查询。 这些日志也在[!DNL New Relic]中提供：转到&#x200B;**[!UICONTROL New Relic]** > **[!UICONTROL 日志]**，并按`filePath:"/var/log/mysql/mysql-slow.log"`进行筛选。

定期查看[!DNL MySQL]慢查询日志，以确认慢查询不是经常运行。 有关解决您标识为有问题的查询的步骤，请参阅[解决数据库性能问题](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/implementation-playbook/best-practices/maintenance/resolve-database-performance-issues)。

## 配置cron作业 {#configure-cron-jobs}

Commerce中的所有异步操作均使用Linux cron命令执行。

Commerce依赖正确的cron作业配置来实现重要的系统功能，包括索引和队列使用者操作。 如果未正确设置，则意味着Commerce将无法按预期工作。

使用Unix crontab文件中适当的Unix用户正确设置和配置Commerce cron至关重要。 每个Unix用户都有自己的crontab文件，该文件是用于为该用户运行cron作业的配置。 有关步骤，请参阅[配置和运行cron作业](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs)。

无法再执行脚本`dev/tools/cron.sh`，因为它已被删除。

## 优化客户端设置 {#optimize-client-side-settings}

要提高Commerce实例的店面响应速度，请在&#x200B;**[!UICONTROL 商店]** > **[!UICONTROL 配置]** > **[!UICONTROL 高级]** > **[!UICONTROL 开发人员]**&#x200B;下配置以下设置，该设置仅在开发人员模式下可用：

* **[!UICONTROL 网格设置]** > **[!UICONTROL 异步索引]**： *[!UICONTROL 启用]*
* **[!UICONTROL CSS设置]** — **[!UICONTROL 缩小CSS文件]**： *[!UICONTROL 是]*
* **[!UICONTROL JavaScript设置]** — **[!UICONTROL 缩小JavaScript文件]**： *[!UICONTROL 是]*
* **[!UICONTROL JavaScript设置]** — **[!UICONTROL 启用JavaScript捆绑]**： *[!UICONTROL 是]*（默认情况下未启用）
* **[!UICONTROL 模板设置]** — **[!UICONTROL 缩小HTML]**： *[!UICONTROL 是]*

由于Adobe Commerce on Cloud始终在生产模式下运行，请改为从命令行设置每个选项（例如`bin/magento config:set --lock-config dev/css/minify_files 1`），然后提交生成的`app/etc/config.php`更改并重新部署。 有关CLI路径的完整列表，请参阅[优化资源文件](https://experienceleague.adobe.com/zh-hans/docs/commerce-operations/implementation-playbook/best-practices/development/optimize-css-js-files)。
