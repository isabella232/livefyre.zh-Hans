---
description: 构建提取请求结构以接收和响应访问用户身份系统的请求。
seo-description: 构建提取请求结构以接收和响应访问用户身份系统的请求。
seo-title: 提取请求结构
solution: Experience Manager
title: 提取请求结构
uuid: bf6b9e45-d08 a-48e6-acc6-e4 fa56428 d25
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 提取请求结构{#pull-request-structure}

构建提取请求结构以接收和响应访问用户身份系统的请求。

Livefyre向您的端点URL发出一个提取请求。

例如，如果您的拖动端点URL为：

```
https://example.yoursite.com/some_path/?id={id}
```

对此端点的Livefyre提取请求将是：

```
https://example.yoursite.com/some_path/?id={id}&lftoken={UserAuthToken}
```

其中， `lftoken` JSON Web Token使用您的网络密钥进行签名， **[!UICONTROL {userAuthToken}]** 是Livefyre生成的用户身份验证令牌。

1. 用于 `lftoken` 验证对您的提取URL的ping请求是由Livefyre而非恶意代理发送的。
1. 对于所有传入的请求：

   * 确保请求中存在 `lftoken` 查询字符串。
   * 使用Livefyre库中的 `validateLivefyreToken` 方法确保已使用 `lftoken` 网络密钥进行签名。

   * 如果 `lftoken` 不存在或无法验证，则不允许您的端点使用配置文件信息做出响应。请改用403(禁止)状态代码，无需响应正文。

1. `userAuthToken` 由Livefyre `buildUserAuthToken` 方法为用户生成，用户id“system”。此用户是为每个新网络创建的第一个用户。
1. 要测试页面，请使用 [我们的Taking for Retting](https://livefyre-p4p-wizard.herokuapp.com/home) 测试人员确认一切均按预期工作。
