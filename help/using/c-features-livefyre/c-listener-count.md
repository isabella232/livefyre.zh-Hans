---
description: 监听器计数是一个计数器，用于跟踪页面上某个应用程序的站点访客数并显示此数。
seo-description: 监听器计数是一个计数器，用于跟踪页面上某个应用程序的站点访客数并显示此数。
seo-title: 监听器计数
solution: Experience Manager
title: 监听器计数
uuid: fdd7cfe4-ae69-4d31-baa2-8978368fc3e8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---


# 监听器计数{#listener-count}

监听器计数是一个计数器，用于跟踪页面上某个应用程序的站点访客数并显示此数。

监听器计数是指在实例化应用程序的页面上打开浏览器的站点访客数。 这样，您便可以了解页面上访客在任何给定时间的数量，以便在他们实时观看流或实时内容时跟踪他们。

Livefyre的监听器计数的工作方式如下：

1. 包含您的App的站点每60秒对Livefyre服务器执行一次ping操作。
1. Livefyre服务器会响应显示应用程序的页面上的站点访客数(定义为打开到该页面的浏览器的站点访客数)。
1. 页面上具有应用程序的站点访客数显示在应用程序上。

使用此功能的应用程序：

* [聊天](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [评论](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## 监听器Avatars {#section_wcn_kxp_vz}

监听器计数最多显示10个头像，并且只显示单击了对话&#x200B;**[!UICONTROL Follow]**&#x200B;的人的头像。

>[!NOTE]
>
>由于空间限制，移动界面仅显示监听器的数量和一个小的“人”图标。

Livefyre监听器计数显示页面上任意给定时间处于活动状态的人数，以及对话后的人数。 如果某人在页面上进行对话，则不会对该用户计数多次。 例如，如果用户在某页上并单击&#x200B;**[!UICONTROL Follow]**，则监听器计数不会增加；如果该用户随后单击&#x200B;**[!UICONTROL Unfollow]**，则计数不会减少。

使用此功能的应用程序：

* [聊天](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [评论](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)

