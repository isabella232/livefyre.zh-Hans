---
description: 从头开始创建Livefyre应用程序，以创建自定义体验和数据可视化。
seo-description: 从头开始创建Livefyre应用程序，以创建自定义体验和数据可视化。
seo-title: 将Livefyre与第三方集成
solution: Experience Manager
title: 将Livefyre集成到CMS中
uuid: 5a3e18e8-8568-45bb-9070-d0fa43dd819b
translation-type: tm+mt
source-git-commit: 2436c389cbe14c7d64dd8c0392a3e0f031468836
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# 通过第三方集成实施Livefyre

从头开始创建Livefyre应用程序，以创建自定义体验和数据可视化。

您可以使用Bootstrap和流API使用Livefyre和社交数据，从头开始创建Livefyre应用程序。

有关需要身份验证的Livefyre应用程序，请参阅标识集成以了解有关支持的第三方身份验证平台的信息。

要实施对话应用程序（评论、聊天、实时博客、站点），请执行以下操作：

1. 执行应用程序集成。
a.使用CollectionMeta令牌创建集合。
b.使用Livefyre.js嵌入代码结构将Livefyre应用程序集成到站点。

   * 有关如何使用Livefyre.js嵌入代码结构的详细信息，请参阅[嵌入App](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。

   * 有关如何集成注释应用程序的信息，请参阅[注释](/help/using/c-about-apps/c-comments/c-comments.md)。

   * 有关如何集成聊天应用程序的信息，请参阅[聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md)。

   * 有关如何集成实时博客应用程序的信息，请参阅[实时博客](/help/using/c-about-apps/c-liveblog-app/c-liveblog-app.md)。

   * 有关如何集成Siestr应用程序的信息，请参阅[Siestrap](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md)。

1. 执行身份验证集成。
a.创建用户身份验证令牌以在Livefyre中传递和存储用户数据。
b.集成第三方用户和身份验证平台。 有关受支持平台的列表，请参阅[Identity Integration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)。

1. 执行应用程序自定义。 用于匹配您的品牌和风格并添加自定义功能的应用程序自定义选项。

要创建可视化应用程序（地图、媒体墙、趋势、传送、幻灯片、故事、功能卡、马赛克、投票）:

1. 执行应用程序集成。
a.使用CollectionMeta令牌创建集合。
b.使用Livefyre.js嵌入代码结构将Livefyre应用程序集成到站点。 有关如何使用Livefyre.js嵌入代码结构的详细信息，请参阅[嵌入App](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。

   * 有关如何集成映射应用程序的信息，请参阅[Map](/help/using/c-about-apps/c-map-app/c-map-app.md)。

   * 有关如何集成媒体墙应用程序的信息，请参阅[媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md)。

   * 有关如何集成趋势应用程序的信息，请参阅[趋势](/help/using/c-about-apps/c-trending-app/c-trending-app.md)。

1. 执行身份验证集成。
a.创建用户身份验证令牌，将用户数据传递并存储到Livefyre。
b.集成第三方用户和身份验证平台。 有关受支持平台的列表，请参阅[Identity Integration](/help/implementation/t-about-identity-integration/t-about-identity-integration.md)。

>[!NOTE]
>
>Livefyre不支持使用Livefyre.js的传送、幻灯片、故事、功能卡、马赛克和投票应用程序。

使用[创建App](/help/using/c-about-apps/c-create-an-app.md)进程集成这些应用程序。