---
description: 构建拉入请求结构，以接收并响应访问您的用户身份系统的请求。
title: 拉式请求结构
exl-id: 70203b23-9d7c-4a22-94ba-2a763e200972
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---

# 拉出请求结构{#pull-request-structure}

构建拉入请求结构，以接收并响应访问您的用户身份系统的请求。

Livefyre向您的端点URL发出拉取请求。

例如，如果您的拉式端点URL为：

```
https://example.yoursite.com/some_path/?id={id}
```

对此端点的Livefyre Pull请求将为：

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

其中`lftoken`是使用您的网络密钥签名的JSON Web令牌，**[!UICONTROL {userAuthToken}]**&#x200B;是Livefyre生成的用户身份验证令牌。

1. 使用`lftoken`验证向Ping for Pull URL发出的请求是由Livefyre而不是恶意代理发送的。
1. 对于所有传入请求：

   * 确保请求中存在`lftoken`查询字符串。
   * 使用Livefyre库中的`validateLivefyreToken`方法确保`lftoken`已使用您的网络密钥进行签名。

   * 如果`lftoken`不存在或验证失败，请不要允许您的端点使用用户档案信息进行响应。 相反，应使用403（禁止）状态代码进行响应，而不使用响应主体。

1. `userAuthToken` 由用户的Livefyre方 `buildUserAuthToken` 法生成，用户id为“system”。此用户是为每个新网络创建的第一个用户。
