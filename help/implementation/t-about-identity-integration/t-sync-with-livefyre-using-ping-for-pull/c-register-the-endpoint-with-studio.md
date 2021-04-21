---
description: 注册URL端点，以便Livefyre可以使用URL提取更新的用户档案信息。
title: 使用Studio注册端点
exl-id: 2910a13a-ae88-41d7-ba7c-88d7a1dbe445
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# 使用Studio{#register-the-endpoint-with-studio}注册端点

注册URL端点，以便Livefyre可以使用URL提取更新的用户档案信息。

每个网络只注册一次Ping for Pull URL。 设置后，除非从用户管理系统获取用户用户档案数据的端点发生更改，否则不应更改此值。

1. 使用Studio向Livefyre注册此URL端点。
1. 注册Livefyre将从中获取更新的用户用户档案信息的URL，转到&#x200B;**[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**，然后在&#x200B;**[!UICONTROL Ping for Pull URL]**&#x200B;字段中输入它。

   例如，URL可以如下所示：`https://example.yoursite.com/some_path/?id={id}`
