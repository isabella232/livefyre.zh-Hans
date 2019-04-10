---
description: 分析网站的用户、内容和主持活动。
seo-description: 分析网站的用户、内容和主持活动。
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9 d8 a1 b0478
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Analytics{#analytics}

分析网站的用户、内容和主持活动。

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

分析网站的用户、内容和主持活动。

Livefyre Analytics可轻松访问网络数据，从而轻松阅读对话、协调和用户数据。使用这些仪表板监控活动并运行网站的快速分析。

仪表板可能会按站点、日期和活动进行过滤。使用窗口左上角的网络下拉列表选择要显示的站点。生成后，单击列标题可对其进行排序，或将鼠标悬停在图形上，以获取有关任何数据点的更多特定信息。

本页介绍：

* Selecting a [Date Range](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange) for your dashboard
* [显示/隐藏可用活动](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [导出仪表板数据](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [集合控制板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [协调控制板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [用户控制板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Analytics目前支持来自Livefyre核心应用程序和协调的活动。这些仪表板中包含的大多数活动也可通过 [Livefyre JavaScript事件获得，它](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/)可用于为您自己的自定义分析工具或第三方分析工具提供动力。

## 日期范围 {#concept_798C438120E643B6BE262C9997DC87C4}

单击日期向下拉出以选择要显示的范围。使用快速日期，或从提供的日历中选择开始日期和结束日期。

![](assets/analytics-date-range.png)

快速日期：

* **今天：** 显示从当日的午夜到当日的最后一个完整小时的数据。
* **昨天：** 显示前24小时的数据。
* **天：** 显示前天的数据，不包括今天的数据。
* **30天：** 显示前30天的数据，不包括今天的数据。
* **本周：** 显示数据从上一周日的午夜到最后一个完整小时的数据。
* **本月：** 显示数据从当月的第一天的午夜到当前的最后一个完整小时的数据。
* **上周：** 显示上周的数据。
* **上个月：** 显示上个月的数据。

## 显示/隐藏活动 {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

活动是用户在站点上执行的操作，包括注释、标记、共享和协调。使用 **显示/隐藏活动** 下拉列表选择要包含在功能板中的活动。

>[!NOTE]
>
>为过滤器选择新事件将重新渲染页面而不会更改URL。

![](assets/analytics-show-hide-activities.png)

可用的活动因仪表板类型和导出而异，可能包括：

* **帖子：** 显示从当日的午夜到当日的最后一个完整小时的数据。
* **回复：** 显示前24小时的数据。
* **喜欢：** 显示前天的数据，不包括今天的数据。
* **不喜欢：** 显示前30天的数据，不包括今天的数据。
* **包含媒体：** 显示数据从上一周日的午夜到最后一个完整小时的数据。
* **帖子上传了照片：** 显示数据从当月的第一天的午夜到当前的最后一个完整小时的数据。
* **帖子具有链接：** 显示上周的数据。
* **帖子包含@提及：** 显示上个月的数据。
* **批准：** 显示上个月的数据。
* **Bozo'd：** 显示上个月的数据。
* **已删除：** 显示上个月的数据。
* **协调总数：** 显示上个月的数据。

## 导出仪表板数据 {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

使用 **“导出** 下拉菜单”将您的仪表板数据导出为CSV文件。

* 每日摘要(仅限集合)：导出每个集合的最后一个完整周数。
* 表数据：导出所有已回滚集合数据(所有列和当前报表中的所有行)。
* 原始数据：导出用于创建当前汇总报告的所有单个活动。

>[!NOTE]
>
>这些报告可能需要几分钟才能导出。所有时间戳都是Unix时间。

## 集合 {#concept_228D8E5553784DB8BABF3819A5FF0345}

集合控制板列出了集合的用户活动，允许您确定最(和至少)具有吸引力的内容。每个列出的集合都包含指向可找到该页面的页面的链接。

![](assets/analytics-collections.png)

## 协调 {#concept_98689B1E804B43CEA21E3F456107CCD9}

审核控制板列出主持人的活动，允许您评估活动。使用此报告可找到最活跃的版主及其最常用的协调措施。

>[!NOTE]
>
>将为审核者名称Livefyre System列出自动化Livefyre审核活动。

![](assets/analytics-moderation.png)

## 用户 {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

“用户仪表板”按用户显示站点活动，允许您分析每个用户与您的站点交互的方式。使用此仪表板可找到您网站上最活跃的用户，并评估最受欢迎的站点活动。

![](assets/analytics-users.png)

