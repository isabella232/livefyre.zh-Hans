---
description: 构建CollectionMeta和身份验证令牌的指南。
seo-description: 构建CollectionMeta和身份验证令牌的指南。
seo-title: 构建服务器端令牌
solution: Experience Manager
title: 构建服务器端令牌
uuid: 8313f26e-5ceb-414e-a61 a-480bb7 a8 ba66
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 构建服务器端令牌{#build-server-side-tokens}

构建CollectionMeta和身份验证令牌的指南。

构建Livefyre用来验证请求的令牌，确保只能对Livefyre网络进行更新。

## CollectionMeta令牌

了解如何创建用于创建新的和显示现有对话的令牌。

## Auth Token

了解如何构建用于验证用户身份的令牌，如果您没有使用Janrain Capture进行用户管理，则这是集成过程中的一个必要步骤。

## 用户身份验证令牌 {#section_l5l_hwt_bbb}

本节介绍如何生成UserAuth JSON对象，该对象创建将用户日志记录到应用程序所需的用户身份验证令牌。

要创建标记，请使用首选语言库传递以下参数：

| 参数 | Type | 描述 |
|---|---|---|
| noknName | String *required* | Livefyre网络的名称(由Livefyre提供)。 |
| NetworkKey | String *required* | 此特定网络的秘密密钥(Livefyre提供)。 |
| userID | String *required* | 用户在用户管理系统中登录的ID(仅限字母数字、短划线、下划线和点字符)： `[a-zA-Z0-9_-.]`)。**注意：** userID必须是唯一的。 |
| 过期 | *需要整数* | 当令牌立即过期时(以秒为单位)。**注意：** 此值也可作为浮点传递。生成的JSON Web令牌将在UNIX环境中存储此值。 |
| displayName | String *required* | 用于在UI中和注释中识别此用户的文本。(最多字符数：50.) |

