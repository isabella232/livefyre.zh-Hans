---
description: 构建ping，以便用户更新其配置文件时，您的页面ping Livefyre。
seo-description: 构建ping，以便用户更新其配置文件时，您的页面ping Livefyre。
seo-title: 构建Ping
solution: Experience Manager
title: 构建Ping
uuid: cb8cc043-9ea5-407c-b70f-3f1e37accdae
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# 构建Ping{#build-the-ping}

构建ping，以便用户更新其配置文件时，您的页面ping Livefyre。

当Livefyre收到包含和的更新通 `networkName` 知时， `user_id`系统将向您的Ping for Pull URL发送拉取请求。

>[!NOTE]
>
>403/Not Authorized for your Ping（响应Ping）表示Ping请求附 `lftoken` 加的无效。 请确保此URL适 `lftoken` 用于具有网络 `user_id` 所有者权限的用户或系统用户。 如果您使用Livefyre库，请使用 `buildLivefyreToken` 该方法为请求生成有效的系统令牌。

1. 在您的页面中添加代码，在用户更新其配置文件时对Livefyre执行ping操作。 通过以下方式构建URL:

```
 POSThttps://{networkName}.quill.fyre.co/api/v3.0/user/{user_id}/refresh?lftoken={token}
```

* **[!UICONTROL networkName:]** 您的Livefyre提供的网络名称。
* **[!UICONTROL user_id:]** 您的用户ID。
* **[!UICONTROL token:]** 有效的系统令牌。

1. 拉取请求结构。
