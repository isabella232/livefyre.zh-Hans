---
description: 构建拉式请求结构，以接收并响应访问您的用户标识系统的请求。
seo-description: 构建拉式请求结构，以接收并响应访问您的用户标识系统的请求。
seo-title: 拉式请求结构
solution: Experience Manager
title: 拉式请求结构
uuid: bf6b9e45-d08a-48e6-acc6-e4fa56428d25
translation-type: tm+mt
source-git-commit: cf447db2cb3498fcb01b511848faeee4d1e48481

---


# 拉式请求结构{#pull-request-structure}

构建拉式请求结构，以接收并响应访问您的用户标识系统的请求。

Livefyre向您的端点URL发出拉取请求。

例如，如果您的拉端点URL是：

```
https://example.yoursite.com/some_path/?id={id}
```

对此端点的Livefyre Pull请求将为：

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

其中 `lftoken` 是使用网络密钥签名的JSON web令牌， **[!UICONTROL {userAuthToken}]** 是Livefyre生成的用户身份验证令牌。

1. 使用 `lftoken` 验证向Ping for Pull URL发出的请求是由Livefyre发送的，而不是恶意代理发送的。
1. 对于所有传入请求：

   * 确保查询 `lftoken` 字符串在请求中存在。
   * 使用Livefyre `validateLivefyreToken` 库中的方法确保已使用 `lftoken` 您的网络密钥进行签名。

   * 如果 `lftoken` 不存在或验证失败，请勿允许您的端点使用配置文件信息进行响应。 相反，请使用403（禁止）状态代码进行响应，而不要使用响应主体。

1. `userAuthToken` 由用户的Livefyre方 `buildUserAuthToken` 法生成，用户ID为“system”。 此用户是为每个新网络创建的第一个用户。
