---
description: 本节介绍如何生成UserAuth JSON对象，该对象创建将用户登录到应用程序所需的用户身份验证令牌。
title: 用户身份验证令牌
exl-id: 564144dd-6db4-447b-80ac-b743ecac833d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 2%

---

# 用户身份验证令牌{#user-auth-token}

本节介绍如何生成UserAuth JSON对象，该对象创建将用户登录到应用程序所需的用户身份验证令牌。

本节介绍如何生成UserAuth JSON对象，该对象创建将用户登录到应用程序所需的用户身份验证令牌。

要创建令牌，请使用首选语言库传入以下参数：

| 参数 | 类型 | 描述 |
|---|---|---|
| networkName | 字符串&#x200B;*必填* | Livefyre网络的名称（由Livefyre提供）。 |
| networkKey | 字符串&#x200B;*必填* | 此特定网络的密钥（由Livefyre提供）。 |
| userId | 字符串&#x200B;*必填* | 用户管理系统中存储的登录用户ID（仅允许使用字母数字、短划线、下划线和点字符）：[a-zA-Z0-9_-。]）。**注意：** userId必须唯一。 |
| 过期 | 整数&#x200B;*必填* | 令牌应从现在开始过期（以秒为单位）。 **注意：** 此值也可以作为浮动值传递。生成的JSON Web令牌将在UNIX纪元时间中存储此值。 |
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

## 拼音{#section_f42_mjz_1cb}

```
network.build_user_auth_token(userId, displayName, expires) 
```

>[!NOTE]
>
>网络密钥不共享给Livefyre拆分帐户。 一旦Livefyre为您提供了环境，您将收到网络密钥。 这把钥匙应该保密。
