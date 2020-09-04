---
description: 使用Livefyre API将Google AMP功能添加到Storify 2页面，以保持内容的交互性和SEO友好性。
seo-description: 使用Livefyre API将Google AMP功能添加到Storify 2页面，以保持内容的交互性和SEO友好性。
seo-title: 将Google AMP与Storify 2结合使用
solution: Experience Manager
title: 将Google AMP与Storify 2结合使用
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 65d931e5bd04964db44f8e3a0e000ecec2652893
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# 将Google AMP与Storify 2结合使用{#use-google-amp-with-storify}

使用Livefyre API将Google AMP功能添加到Storify 2页面，以保持内容的交互性和SEO友好性。

要将Google AMP与Storify 2一起使用，您必须为Storify 2应用程序创建一个带有Google AMP标记的页面。

App的AMP版本从原始页面请求更新(使 **用amp** -live- **列表API中的pollInterval** 参数设置更新请求的时间间隔)。 要确保AMP页面上的访客能够快速获得最新内容，请在Storify 2 AMP页面上保持低缓存TTL。

作为帖子包含在Storify 2应用程序中的非图像资产（例如，视频）必须使用HTTPS（由AMP规范指定）。 使用Google Cloud内容投放网络(CDN)的AMP URL使用HTTPS。

要将Google AMP与Storify 2结合使用，请执行以下操作：

1. 在您的站点上创建经过AMP验证的模板。
1. 使用以下一个或多个Google AMP API自定义您的Google AMP页面：
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) ，用于自定义Storify 2显示
   1. [amp-live-列表](https://www.ampproject.org/docs/reference/components/amp-live-list) ，自定义更新的时间间隔
   1. [amp-social](https://www.ampproject.org/docs/reference/components/amp-social-share) -share添加社交共享按钮
1. 将以下Storify 2 AMP页面的内容包含在标记中Storify 2页面的CSS `<style amp-custom>` 中： [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. 将以下Storify 2 AMP标记API的内容包含到您的Google AMP模板中： `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` 其中{{APP_ID}}是Livefyre Studio中Storify 2应用程序的应用程序ID。
   1. 唯一的查询参 **数是pollInterval**，它是应用程序检查更新的时间间隔（以毫秒为单位）。
   1. 该URL包含来自最新帖子的内容（包括帖子、视频等）
   1. 发布者页面需要从此URL获取内容，所以需要更新Google AMP页面。
