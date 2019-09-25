---
description: 注册URL端点，以便Livefyre可以使用URL提取更新的配置文件信息。
seo-description: 注册URL端点，以便Livefyre可以使用URL提取更新的配置文件信息。
seo-title: 使用Studio注册端点
solution: Experience Manager
title: 使用Studio注册端点
uuid: 4eb816ee-d743-43bf-bfee-d9b9fd98b482
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用Studio注册端点{#register-the-endpoint-with-studio}

注册URL端点，以便Livefyre可以使用URL提取更新的配置文件信息。

每个网络只注册一次Ping for Pull URL。 设置后，除非从用户管理系统获取用户配置文件数据的端点发生更改，否则此值不应更改。

1. 使用Studio向Livefyre注册此URL端点。
1. 注册Livefyre将从中获取更新的用户配置文件信息的URL，转 **[!UICONTROL Studio > Settings > Integration Settings > Remote Profiles]**&#x200B;到并在字段中输入该 **[!UICONTROL Ping for Pull URL]** 信息。

   例如，URL可以如下： `https://example.yoursite.com/some_path/?id={id}`

