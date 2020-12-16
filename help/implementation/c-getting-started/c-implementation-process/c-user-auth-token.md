---
description: 本节介绍如何生成UserAuth JSON对象，该对象创建将用户登录到应用程序所需的用户身份验证令牌。
seo-description: 本节介绍如何生成UserAuth JSON对象，该对象创建将用户登录到应用程序所需的用户身份验证令牌。
seo-title: 用户身份验证令牌
solution: Experience Manager
title: 用户身份验证令牌
uuid: 6483debd-453c-4780-b19c-1d8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---


# 用户身份验证令牌{#user-auth-token}

本节介绍如何生成UserAuth JSON对象，该对象创建将用户登录到应用程序所需的用户身份验证令牌。

本节介绍如何生成UserAuth JSON对象，该对象创建将用户登录到应用程序所需的用户身份验证令牌。

要创建令牌，请使用首选语言库传递以下参数：

| 参数 | 类型 | 描述 |
|---|---|---|
| networkName | 字符串&#x200B;*必填* | Livefyre网络的名称（由Livefyre提供）。 |
| networkKey | 字符串&#x200B;*必填* | 此特定网络的密钥（由Livefyre提供）。 |
| userId | 字符串&#x200B;*必填* | 登录时存储在用户管理系统中的用户的ID(只允许使用字母数字、短划线、下划线和点字符：[a-zA-Z0-9_-。]）。**注意：** userId必须唯一。 |
| 过期 | 整数&#x200B;*必填* | 令牌应从现在开始过期的时间（以秒为单位）。 **注意：** 此值也可以作为浮点值传递。生成的JSON Web令牌将在UNIX纪元时间中存储此值。 |
| displayName | 字符串&#x200B;*必填* | 用于在UI和注释中标识此用户的文本。 (最大字符数：50.) |

## Java {#section_b42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
 
```

## NodeJS {#section_c42_mjz_1cb}

```
network.buildUserAuthToken(userId, displayName, expires); 
```

## PHP {#section_d42_mjz_1cb}

```
$network->buildUserAuthToken(userId, displayName, expires); 
```

## Python {#section_e42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

## Ruby {#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>Livefyre演示帐户不共享网络密钥。 一旦Livefyre为您提供了环境，您将收到网络密钥。 这把钥匙应该保密。

