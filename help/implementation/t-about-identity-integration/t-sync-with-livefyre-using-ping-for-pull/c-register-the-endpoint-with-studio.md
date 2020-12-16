---
description: 注册URL端点，以便Livefyre可以使用URL提取更新的用户档案信息。
seo-description: 注册URL端点，以便Livefyre可以使用URL提取更新的用户档案信息。
seo-title: 使用Studio注册端点
solution: Experience Manager
title: 使用Studio注册端点
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# 使用Studio{#register-the-endpoint-with-studio}注册端点

注册URL端点，以便Livefyre可以使用URL提取更新的用户档案信息。

每个网络只注册一次Ping for Pull URL。 设置后，此值不应更改，除非从用户管理系统获取用户用户档案数据的端点发生更改。

1. 使用Studio向Livefyre注册此URL端点。
1. 注册Livefyre将从中获取更新的用户用户档案信息的URL，转到&#x200B;**[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**&#x200B;并在&#x200B;**[!UICONTROL Ping for Pull URL]**&#x200B;字段中输入它。

   例如，URL可以如下所示：`https://example.yoursite.com/some_path/?id={id}`

