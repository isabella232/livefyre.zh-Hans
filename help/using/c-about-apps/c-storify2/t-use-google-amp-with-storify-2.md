---
description: 使用Livefyre API将Google AMP功能添加到Storify 2页面，以保持内容的交互性和SEO友好性。
seo-description: Use Livefyre APIs to add Google AMP functionality to your Storify 2 page to keep the content interactive and SEO-friendly.
seo-title: 将Google AMP与Storify 2结合使用
solution: Experience Manager
title: 将Google AMP与Storify 2结合使用
uuid: 40c9f083-7284-43ba-ae27-53b1ff9e3954
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 将Google AMP与Storify 2结合使用{#use-google-amp-with-storify}

使用Livefyre API将Google AMP功能添加到Storify 2页面，以保持内容的交互性和SEO友好性。

要将Google AMP与Storify 2一起使用，您必须为Storify 2应用程序创建一个包含Google AMP标记的页面。

App的AMP版本从原始页面请求更新(使用 **amp-live-list** API中的pollInterval **** 参数设置更新请求的间隔)。 要确保AMP页面上的访客快速获得最新内容，请在Storify 2 AMP页面上保持低缓存TTL。

作为帖子包含在Storify 2应用程序中的非图像资产（例如，视频）必须按照AMP规范的指定使用HTTPS。 使用Google Cloud内容交付网络(CDN)的AMP URL使用HTTPS。

将Google AMP与Storify 2结合使用：

1. 在您的站点上创建经过AMP验证的模板。
1. 使用以下一个或多个Google AMP API自定义您的Google AMP页面：
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) ，用于自定义Storify 2显示屏
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) ，用于自定义更新的时间间隔
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) ，添加社交共享按钮
1. 将以下Storify 2 AMP页面的内容包含在Storify 2页面的CSS中 <style amp-custom> 标记： [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. 将以下Storify 2 AMP标记API的内容包含到您的Google AMP模板中：其 `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` 中{{APP_ID}}是Livefyre studio中Storify 2应用程序的应用程序ID。
   1. 唯一的查询参 **数是pollInterval**，这是应用程序检查更新的间隔（以毫秒为单位）。
   1. 该URL包含来自最近帖子（包括帖子、视频等）的内容
   1. 发布者页面需要像您希望更新Google AMP页面一样频繁地从此URL获取内容。
