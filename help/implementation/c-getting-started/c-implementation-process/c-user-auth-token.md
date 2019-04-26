---
description: 本节介绍如何生成UserAuth JSON对象，该对象创建将用户日志记录到应用程序所需的用户身份验证令牌。
seo-description: 本节介绍如何生成UserAuth JSON对象，该对象创建将用户日志记录到应用程序所需的用户身份验证令牌。
seo-title: 用户身份验证令牌
solution: Experience Manager
title: 用户身份验证令牌
uuid: 6483debd-453c-4780-b19 c-1d8041693617
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 用户身份验证令牌{#user-auth-token}

本节介绍如何生成UserAuth JSON对象，该对象创建将用户日志记录到应用程序所需的用户身份验证令牌。

本节介绍如何生成UserAuth JSON对象，该对象创建将用户日志记录到应用程序所需的用户身份验证令牌。

要创建标记，请使用首选语言库传递以下参数：

| 参数 | Type | 描述 |
|---|---|---|
| noknName | String *required* | Livefyre网络的名称(由Livefyre提供)。 |
| NetworkKey | String *required* | 此特定网络的秘密密钥(Livefyre提供)。 |
| userID | String *required* | 用户在用户管理系统中登录的ID(仅限字母数字、短划线、下划线和点字符)： [a-ZA-Z0-9_-.]). **注意：** userID必须是唯一的。 |
| 过期 | *需要整数* | 当令牌立即过期时(以秒为单位)。**注意：** 此值也可作为浮点传递。生成的JSON Web令牌将在UNIX环境中存储此值。 |
| displayName | String *required* | 用于在UI中和注释中识别此用户的文本。(最多字符数：50.) |

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
>Livefyre演示站点帐户不会共享网络密钥。Livefyre为您提供了环境后，您将收到网络密钥。此键应保持私有。

