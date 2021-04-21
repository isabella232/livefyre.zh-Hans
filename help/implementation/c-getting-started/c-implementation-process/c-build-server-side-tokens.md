---
description: 构建collectionMeta和身份验证令牌的指南。
title: 构建服务器端令牌
exl-id: f709b79e-9236-443e-b862-c7d281815d91
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 1%

---

# 生成服务器端令牌{#build-server-side-tokens}

构建collectionMeta和身份验证令牌的指南。

构建Livefyre用于验证请求的令牌可确保只有您才能对Livefyre网络进行更新。

## CollectionMeta令牌

了解如何构建令牌以创建新对话并显示现有对话。

## 身份验证令牌

了解如何构建用于验证用户身份的令牌，这是集成过程中的一个必要步骤（如果您不使用Janrain Capture进行用户管理）。

## 用户身份验证令牌{#section_l5l_hwt_bbb}

本节介绍如何生成UserAuth JSON对象，该对象创建将用户登录到应用程序所需的用户身份验证令牌。

要创建令牌，请使用首选语言库传入以下参数：

| 参数 | 类型 | 描述 |
|---|---|---|
| networkName | 字符串&#x200B;*必填* | Livefyre网络的名称（由Livefyre提供）。 |
| networkKey | 字符串&#x200B;*必填* | 此特定网络的密钥（由Livefyre提供）。 |
| userId | 字符串&#x200B;*必填* | 用户管理系统中存储的登录用户ID（仅允许使用字母数字、短划线、下划线和点字符）：`[a-zA-Z0-9_-.]`)。 **注意：** userId必须唯一。 |
| 过期 | 整数&#x200B;*必填* | 令牌应从现在开始过期（以秒为单位）。 **注意：** 此值也可以作为浮动值传递。生成的JSON Web令牌将在UNIX纪元时间中存储此值。 |
| displayName | 字符串&#x200B;*必填* | 用于在UI和注释中标识此用户的文本。 (最大字符数：50.) |
