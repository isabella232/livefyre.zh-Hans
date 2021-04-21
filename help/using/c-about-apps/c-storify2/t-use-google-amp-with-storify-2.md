---
description: 使用Livefyre API将Google AMP功能添加到Storify 2页面，以保持内容的交互性和SEO友好性。
title: 将Google AMP与Storify 2结合使用
exl-id: 2fee8655-ac9f-484e-a042-9b7ac7151fcc
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# 将Google AMP与Storify 2{#use-google-amp-with-storify}一起使用

使用Livefyre API将Google AMP功能添加到Storify 2页面，以保持内容的交互性和SEO友好性。

要将Google AMP与Storify 2一起使用，您必须为Storify 2应用程序创建一个包含Google AMP标记的页面。

App的AMP版本从原始页面请求更新(使用&#x200B;**amp-live-列表** API中的&#x200B;**pollInterval**&#x200B;参数设置更新请求的间隔)。 要确保AMP页面上的访客能快速获得最新内容，请在Storify 2 AMP页面上保留低缓存TTL。

作为帖子包含在Storify 2应用程序中的非图像资产（例如，视频）必须使用HTTPS（由AMP规范指定）。 使用Google Cloud Content投放网络(CDN)的AMP URL使用HTTPS。

将Google AMP与Storify 2结合使用：

1. 在您的站点上创建经过AMP验证的模板。
1. 使用以下一个或多个Google AMP API自定义您的Google AMP页面：
   1. [amp-](https://www.ampproject.org/docs/reference/components/amp-iframe) iframeto自定义Storify 2显示
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) 自定义更新的时间间隔
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) 添加社交共享按钮
1. 在`<style amp-custom>`标记中，将以下Storify 2 AMP页面的内容包含到Storify 2页面的CSS中：[https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. 将以下Storify 2 AMP标记API的内容包含到您的Google AMP模板中：`https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp`其中{{APP_ID}}是Livefyre Studio中Storify 2应用程序的应用程序ID。
   1. 唯一的查询参数是&#x200B;**pollInterval**，这是应用程序检查更新的间隔（以毫秒为单位设置）。
   1. 该URL包含来自最新帖子（包括帖子、视频等）的内容
   1. 发布者页面需要从此URL获取内容，所以需要更新Google AMP页面。
