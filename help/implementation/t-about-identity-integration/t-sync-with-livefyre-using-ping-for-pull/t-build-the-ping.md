---
description: 构建ping，以便在用户更新其配置文件时，页面ping Livefyre。
seo-description: 构建ping，以便在用户更新其配置文件时，页面ping Livefyre。
seo-title: 构建Bing
solution: Experience Manager
title: 构建Bing
uuid: cb8cc043-9ea5-407c-b70 f-3f1 e37 accoon
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 构建Bing{#build-the-ping}

构建ping，以便在用户更新其配置文件时，页面ping Livefyre。

当Livefyre收到包含 `networkName` 和和 `user_id`的更新通知时，系统会向您的“提取URL”发送一个请求请求。

>[!NOTE]
>
>403/未授权对您的ping做出响应表示在ping请求中 `lftoken` 附加了无效的附加内容。请确保属于 `lftoken` 网络 `user_id` 所有者权限或系统用户。如果您使用的是Livefyre库，则使用该 `buildLivefyreToken` 方法为请求生成有效系统令牌。

1. 在用户更新其配置文件时，将代码添加到对Livefyre进行ping的页面。以此方式构建URL：

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** 您的Livefyre提供了网络名称。
* **[!UICONTROL user_id:]** 用户的ID。
* **[!UICONTROL token:]** 有效的系统令牌。

1. 提取请求结构。
