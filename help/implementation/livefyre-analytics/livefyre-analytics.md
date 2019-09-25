---
description: 分析网站的用户、内容和审查方活动。
seo-description: 分析网站的用户、内容和审查方活动。
seo-title: Analytics
solution: Experience Manager
title: Analytics
uuid: b022aa77-59b9-422a-8d9f-fb9d8a1b0478
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Analytics{#analytics}

分析网站的用户、内容和审查方活动。

## Analytics {#topic_22D8FAE581CD440EA02B1595520F60C2}

分析网站的用户、内容和审查方活动。

Livefyre Analytics提供对网络数据的访问，该数据可以在易于阅读的仪表板中访问对话、协调和用户数据。 使用这些仪表板监视活动并在您的站点上运行快速分析。

仪表板可按站点、日期和活动进行筛选。 使用窗口左上角的“网络”下拉菜单选择要显示的站点。 生成列标题后，单击列标题进行排序，或将鼠标悬停在图形上以了解有关任何数据点的更多特定信息。

本页介绍：

* 为功能 [板选择日期](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#DateRange) 范围
* [显示／隐藏可用活动](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ShowHideActivities)
* [导出功能板数据](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ExportDashboardData)
* [收藏集功能板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#CollectionsDashboard)
* [审核功能板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#ModerationDashboard)
* [用户控制板](https://answers.livefyre.com/livefyre-studio-version-1/studio/analytics/#UsersDashboard)

>[!NOTE]
>
>Analytics当前支持源自Livefyre核心应用程序和协调的活动。 这些仪表板中包含的大多数活动也可通过 [Livefyre javaScript Events](https://answers.livefyre.com/developers/reference/app-customizations/javascript-events/)，它可用于支持您自己的自定义或第三方分析工具。

## 日期范围 {#concept_798C438120E643B6BE262C9997DC87C4}

单击日期下拉列表以选择要显示的范围。 使用快速日期，或从提供的日历中选择开始和结束日期。

![](assets/analytics-date-range.png)

快速日期：

* **** 今天：显示从当天午夜至此时刻前最后一个完整小时的数据。
* **** 昨天：显示24小时前的数据。
* **** 7天：显示前7天的数据，不包括今天。
* **** 30天：显示前30天的数据，不包括今天。
* **** 本周：显示从上周日午夜至此时刻前最后一个完整小时的数据。
* **** 本月：显示从当月第一天的午夜至此时刻前最后一个完整小时的数据。
* **** 上周：显示上周的数据。
* **** 上个月：显示上个月的数据。

## 显示／隐藏活动 {#concept_022D9851CBCE4A2FB80D0AE52A23744D}

活动是指用户在您的网站上执行的注释、标记、共享和调节等操作。 使用显 **示／隐藏活动下拉框** ，选择您希望包含在功能板中的活动。

>[!NOTE]
>
>为过滤器选择新事件将重新呈现页面，而不更改URL。

![](assets/analytics-show-hide-activities.png)

可用活动因仪表板类型和导出而异，可能包括：

* **** 帖子：显示从当天午夜至此时刻前最后一个完整小时的数据。
* **** 回复：显示24小时前的数据。
* **** 喜欢：显示前7天的数据，不包括今天。
* **** 取消赞：显示前30天的数据，不包括今天。
* **** 包含媒体：显示从上周日午夜至此时刻前最后一个完整小时的数据。
* **** 帖子已上传照片：显示从当月第一天的午夜至此时刻前最后一个完整小时的数据。
* **** 帖子包含链接：显示上周的数据。
* **** 帖子包含@mentions:显示上个月的数据。
* **** 批准：显示上个月的数据。
* **** 博佐德：显示上个月的数据。
* **** 废弃：显示上个月的数据。
* **** 审核总数：显示上个月的数据。

## 导出功能板数据 {#concept_730DB61A9F894BE6BFB34E0E2A421ED3}

使用“ **导出** ”下拉菜单将功能板数据导出为CSV文件。

* 每日摘要（仅限集合）:导出每个集合的上一完整周的每日计数。
* 表数据：导出所有汇总的集合数据（当前报告中的所有列和所有行）。
* 原始数据：导出用于创建当前汇总报表的所有单个事件。

>[!NOTE]
>
>这些报告可能需要几分钟才能导出。 所有时间戳都是Unix时间。

## 收藏集 {#concept_228D8E5553784DB8BABF3819A5FF0345}

“收藏集”控制板按收藏集列出用户活动，允许您确定最吸引人（也是最不吸引人）的内容。 列出的每个集合都包含一个指向可在其上找到该集合的页面的链接。

![](assets/analytics-collections.png)

## 审核 {#concept_98689B1E804B43CEA21E3F456107CCD9}

“审核”控制板按审查方列出事件，允许您评估其活动。 使用此报告可查找最活跃的版主及其最常见的审核操作。

>[!NOTE]
>
>将为主持人名称Livefyre system列出自动化的Livefyre协调活动。

![](assets/analytics-moderation.png)

## 用户 {#concept_D1A83E31C7B5467F9C844CBF9A740E12}

“用户”控制板按用户显示站点活动，允许您分析各个用户与站点的交互方式。 使用此功能板查找整个网站中最活跃的用户，并评估最受欢迎的网站活动。

![](assets/analytics-users.png)

