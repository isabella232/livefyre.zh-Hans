---
description: 使用Livefyre API将Google AMP功能添加到您的Storify页面，以保持内容交互和SEO友好。
seo-description: 使用Livefyre API将Google AMP功能添加到您的Storify页面，以保持内容交互和SEO友好。
seo-title: 将Google AMP与Storify结合使用
solution: Experience Manager
title: 将Google AMP与Storify结合使用
uuid: 40c9f083-7284-43ba-ae27-53b1 ff9 e3954
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 将Google AMP与Storify结合使用{#use-google-amp-with-storify}

使用Livefyre API将Google AMP功能添加到您的Storify页面，以保持内容交互和SEO友好。

要将Google AMP与Storify结合使用，您必须使用Google AMP标记为您的Storifify App创建一个页面。

应用程序的AMP版本从原始页面请求更新(使用 ******amp-live-list** API中的pollInterval参数可设置更新请求的间隔)。为确保AMP页面上的访客快速获得最新内容，请在您的Storify AMP页面上保留低缓存TTL。

在Storify应用程序中作为帖子包含的非图像资源(例如视频)必须使用AMP规范指定的HTTPS。使用Google Cloud内容交付网络(CDN)的AMP URL使用HTTPS。

要将Google AMP与Storify结合使用，请执行以下操作：

1. 在站点上创建AMP验证的模板。
1. 使用以下一个或多个Google AMP API自定义Google AMP页面：
   1. [amp-iframe](https://www.ampproject.org/docs/reference/components/amp-iframe) 以自定义Storify显示屏
   1. [amp-live-list](https://www.ampproject.org/docs/reference/components/amp-live-list) 可自定义更新的时间间隔
   1. [amp-social-share](https://www.ampproject.org/docs/reference/components/amp-social-share) 以添加社交共享按钮
1. 将以下Storify AMP页面的内容包含在 <style amp-custom> 标签： [https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css](https://cdn.livefyre.com/libs/liveblog-v2-component/amp.min.css)
1. 将以下Storify AMP标记API的内容包含到您的Google AMP模板中： `https://api.livefyre.com/app-service/v4/bootstrap/{{APP_ID}}/amp` 其中{{App_ ID}}是Livefyre Studio中Storifify App的App ID。
   1. 唯一的查询参数是 **PollInterval**，这是应用程序将检查更新的时间间隔(以毫秒为单位)。
   1. URL包括来自最新帖子(包括帖子、视频等)的内容。
   1. publisher页面需要像您希望更新Google AMP页面一样经常从此URL获取内容。
