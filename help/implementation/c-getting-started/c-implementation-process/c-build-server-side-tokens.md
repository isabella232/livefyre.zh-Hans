---
description: 构建集合元和身份验证令牌的指南。
seo-description: 构建集合元和身份验证令牌的指南。
seo-title: 构建服务器端令牌
solution: Experience Manager
title: 构建服务器端令牌
uuid: 8313f26e-5ceb-414e-a61a-480bb7a8ba66
translation-type: tm+mt
source-git-commit: 5bf937c8cb1a9ca12216ee1884142b8787ff063e
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# 构建服务器端令牌{#build-server-side-tokens}

构建集合元和身份验证令牌的指南。

构建Livefyre用于验证请求的令牌可确保只有您才能对Livefyre网络进行更新。

## 集合元令牌

了解如何构建令牌以创建新对话和显示现有对话。

## 身份验证令牌

了解如何构建用于验证用户身份的令牌，这是集成过程中的一个必要步骤（如果您不使用Janrain Capture进行用户管理）。

## 用户身份验证令牌{#section_l5l_hwt_bbb}

本节介绍如何生成UserAuth JSON对象，该对象创建将用户登录到应用程序所需的用户身份验证令牌。

要创建令牌，请使用首选语言库传递以下参数：

| 参数 | 类型 | 描述 |
|---|---|---|
| networkName | 字符串&#x200B;*必填* | Livefyre网络的名称（由Livefyre提供）。 |
| networkKey | 字符串&#x200B;*必填* | 此特定网络的密钥（由Livefyre提供）。 |
| userId | 字符串&#x200B;*必填* | 登录时存储在用户管理系统中的用户的ID(只允许使用字母数字、短划线、下划线和点字符：`[a-zA-Z0-9_-.]`)。 **注意：** userId必须唯一。 |
| 过期 | 整数&#x200B;*必填* | 令牌应从现在开始过期的时间（以秒为单位）。 **注意：** 此值也可以作为浮点值传递。生成的JSON Web令牌将在UNIX纪元时间中存储此值。 |
| displayName | 字符串&#x200B;*必填* | 用于在UI和注释中标识此用户的文本。 (最大字符数：50.) |

