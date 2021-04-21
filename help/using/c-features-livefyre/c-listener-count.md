---
description: 侦听器计数是一个计数器，用于跟踪页面上某个应用程序的站点访客数并显示此数。
title: 监听器计数
exl-id: a07e83c2-7465-42ec-9d24-821aac5ab74b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---

# 侦听器计数{#listener-count}

侦听器计数是一个计数器，用于跟踪页面上某个应用程序的站点访客数并显示此数。

监听器计数是指向实例化App的页面打开浏览器的站点访客数。 这样，您就可以了解页面上在任何给定时间有多少个站点访客，以便在他们实时观看流或实时内容时跟踪他们。

Livefyre的监听器计数的工作方式如下：

1. 包含您的App的站点每60秒对Livefyre服务器执行一次ping操作。
1. Livefyre服务器会响应显示应用程序的页面上的站点访客数(定义为打开到该页面的浏览器的站点访客数)。
1. 页面上具有应用程序的站点访客数显示在应用程序上。

使用此功能的应用程序：

* [聊天](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [评论](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

## 侦听器Avatar {#section_wcn_kxp_vz}

监听器计数最多显示10个头像，并且只显示那些单击了对话&#x200B;**[!UICONTROL Follow]**&#x200B;的人的头像。

>[!NOTE]
>
>由于空间限制，移动界面仅显示监听器的数量和一个小的“人物”图标。

Livefyre监听器计数显示页面上在任何给定时间处于活动状态的人数，以及对话后的人数。 如果某人在页面上并在对话后进行，则不会计入该用户的多次。 例如，如果用户在某页上单击&#x200B;**[!UICONTROL Follow]**，则侦听器计数不会增加；如果该用户随后单击&#x200B;**[!UICONTROL Unfollow]**，则计数不会减少。

使用此功能的应用程序：

* [聊天](../c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [评论](../c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Storify 2](../c-about-apps/c-storify2/c-storify2.md#c_storify2)
