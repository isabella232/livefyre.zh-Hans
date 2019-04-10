---
description: 允许用户自定义显示其内容的图像。
seo-description: 允许用户自定义显示其内容的图像。
seo-title: Avatars
title: Avatars
uuid: bf20f3bc-3dcc-4e16-a629-380d1 a7 f3 f2
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Avatars{#avatars}

允许用户自定义显示其内容的图像。

用户头像会在所有应用程序中内容旁边显示(默认情况下)，并从实施中使用的标识配置文件系统中提取。这些avats根据显示的应用程序大小不同而异。

(如果您不希望在应用程序中显示Avatars，则Livefyre允许您禁用Avatars。)

>[!NOTE]
>
>Avatars在用于聊天的25p x25p中显示，在大多数其他应用程序中显示50p x50p。

## 头像存储 {#section_zbh_x1f_wy}

Avatars在Livefyre中异步加载。当用户首次登录应用程序或更改关联的头像图像文件时，他们的配置文件图像将添加到任务队列中。(在用户上传到Livefyre头像存储位置时，会临时显示一个默认的头像。)

## 墓座 {#section_mqh_p1f_wy}

Livefyre支持使用墓地。如果用户没有自定义头像作为其用户配置文件的一部分，Livefyre将会检查该用户的“墓地”。如果不存在任何术语，将使用默认的头像。

如果使用Livefyre WordPress插件来嵌入评论，则满足以下条件时将使用用户的术语表：

* 在WordPress管理员面板中已激活了术语，并且
* 用户有一个“蚱蜢”帐户，并且
* 不提供自定义头像。

有关详细信息，请参阅WordPress词汇文档。



使用此功能的应用程序：

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [注释](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地图](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)

