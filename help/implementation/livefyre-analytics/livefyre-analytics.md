---
description: 分析网站的用户、内容和审查方活动。
title: Analytics
exl-id: dc0545ec-2294-44ab-87c4-67eb30c3f787
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 1%

---

# Analytics{#analytics}

分析网站的用户、内容和审查方活动。

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

分析网站的用户、内容和审查方活动。

Livefyre Analytics可让用户通过轻松阅读对话、审核和用户数据仪表板来访问网络数据。 使用这些仪表板可监控活动并在您的站点上运行快速分析。

仪表板可以按站点、日期和活动过滤。 使用窗口左上角的网络下拉列表选择要显示的站点。 生成后，单击列标题进行排序，或将鼠标悬停在图形上以了解有关任何数据点的更多特定信息。

本页介绍：

* 为您的仪表板选择[日期范围](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange)
* [显示/隐藏可用活动](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [导出仪表板数据](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [集合仪表板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [审核仪表板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [用户仪表板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Analytics目前支持源自Livefyre核心应用程序和审核的活动。 这些仪表板中包含的大多数活动也可通过[Livefyre JavaScript事件](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/)获得，这些应用程序可用于支持您自己的自定义或第三方分析工具。

## 日期范围 {#concept_798C438120E643B6BE262C9997DC87C4}

单击日期下拉列表以选择要显示的范围。 使用快速日期，或从提供的日历中选择开始和结束日期。

![](assets/analytics-date-range.png)

快速日期：

* **今天：** 显示从当天午夜到此时刻之前最后一个完整小时的数据。
* **昨天：** 显示之前24小时的数据。
* **7天：显** 示以前7天的数据，不包括今天。
* **30天：显** 示之前30天的数据，不包括今天。
* **本周：显** 示从上个星期日的午夜至此时刻之前最后一个完整小时的数据。
* **本月：** 显示从当月第一天午夜至此时刻前最后一个完整小时的数据。
* **Last Week:** 显示上周的数据。
* **上个月：** 显示上个月的数据。

## 显示/隐藏活动{#concept_022D9851CBCE4A2FB80D0AE52A23744D}

活动是用户在您的网站上执行的操作，包括注释、标记、共享和协调。 使用&#x200B;**显示/隐藏活动**&#x200B;下拉列表选择要包含在仪表板中的活动。

>[!NOTE]
>
>为筛选器选择新事件将在不更改URL的情况下重新呈现页面。

![](assets/analytics-show-hide-activities.png)

可用活动因仪表板类型和导出而异，可能包括：

* **帖子：** 显示从当天午夜至此时刻之前最后一个完整小时的数据。
* **回复：** 显示以前24小时的数据。
* **称赞：** 显示之前7天的数据，不包括今天。
* **取消** 称赞：显示前30天的数据，不包括今天。
* **包含媒体：** 显示从上个星期日的午夜到此时刻之前最后一个完整小时的数据。
* **帖子已上传照** 片：显示从当月第一天午夜至此前一整小时的数据。
* **帖子包含链接：** 显示上周的数据。
* **帖子有@mentions:** 显示上个月的数据。
* **已批准：** 显示上个月的数据。
* **Bozo&#39;d：显** 示上个月的数据。
* **Trashed:** 显示上个月的数据。
* **审核总** 数：显示上个月的数据。

## 导出仪表板数据{#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

使用&#x200B;**导出**&#x200B;下拉菜单将仪表板数据导出为CSV文件。

* 每日摘要（仅限集合）：导出每个集合上一周的每日统计。
* 表数据：导出所有汇总的集合数据（当前报表中的所有列和所有行）。
* 原始数据：导出用于创建当前汇总报表的所有单个事件。

>[!NOTE]
>
>这些报告可能需要几分钟才能导出。 所有时间戳都是Unix时间。

## 收藏集 {#concept_228D8E5553784DB8BABF3819A5FF0345}

“集合”仪表板按“集合”列表用户活动，从而允许您确定最具（和最不具有）吸引力的内容。 列出的每个集合都包含一个指向可在其中找到该集合的页面的链接。

![](assets/analytics-collections.png)

## 审核 {#concept_98689B1E804B43CEA21E3F456107CCD9}

审核仪表板列表事件由审核方进行，允许您评估其活动。 使用此报表可查找您最活跃的版主及其最常见的审核操作。

>[!NOTE]
>
>将自动的Livefyre审核活动将列在主持人名称Livefyre System中。

![](assets/analytics-moderation.png)

## 用户 {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

“用户”仪表板按用户显示网站活动，使您能够分析各个用户与网站交互的方式。 使用此仪表板查找整个网站中最活跃的用户，并评估最受欢迎的网站活动。

![](assets/analytics-users.png)
