---
description: 注册URL端点，Livefyre可使用URL提取更新的配置文件信息。
seo-description: 注册URL端点，Livefyre可使用URL提取更新的配置文件信息。
seo-title: 使用Studio注册端点
solution: Experience Manager
title: 使用Studio注册端点
uuid: eb816ee-d743-43bf-btense-d9 b9 fd98 b482
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 使用Studio注册端点{#register-the-endpoint-with-studio}

注册URL端点，Livefyre可使用URL提取更新的配置文件信息。

为每个网络注册“仅限提取URL”一次。设置后，此值不应更改，除非从用户管理系统更改获取用户配置文件数据的端点。

1. 使用Studio在Livefyre中注册此URL端点。
1. 注册Livefyre从中获取更新用户配置文件信息的URL，转到 **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**该URL，然后在 **[!UICONTROL Ping for Pull URL]** 字段中输入。

   例如，URL可以如下所示： `https://example.yoursite.com/some_path/?id={id}`

