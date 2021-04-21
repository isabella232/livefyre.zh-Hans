---
description: 允许用户自定义显示的图像及其内容。
title: 阿瓦塔
exl-id: cff7f6be-3660-4d71-949b-6ac04379d68d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---

# Avatars{#avatars}

允许用户自定义显示的图像及其内容。

用户头像会（默认情况下）显示在所有应用程序中的内容旁边，并从您的实施中使用的标识用户档案系统中提取。 根据显示这些化身的应用程序，这些化身的大小各不相同。

（如果您不希望在应用程序中显示Avatar，Livefyre允许您禁用它们。）

>[!NOTE]
>
>对于聊天，头像以25p x 25p显示，在大多数其他应用程序中，头像以50p x 50p显示。

## 头像存储{#section_zbh_x1f_wy}

Avatar在Livefyre中异步加载。 当用户首次登录到应用程序或更改其关联的头像图像文件时，其用户档案图像将添加到任务队列。 (当用户的头像上传到Livefyre头像存储位置时，默认头像会临时显示。)

## 格拉瓦塔{#section_mqh_p1f_wy}

Livefyre支持使用Gravatar。 如果用户没有自定义头像作为其用户用户档案的一部分，Livefyre将检查该用户的Gravatar。 如果不存在Gravatar，则将使用默认头像。


使用此功能的应用程序：

* [轮播](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地图](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [马赛克](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
