---
description: 了解Livefyre惯例以及Livefyre如何组织内容。
title: 架构
exl-id: d4fe12d1-117a-4aae-90ff-e9ebdd6c5bac
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# 架构{#architecture}

了解Livefyre惯例以及Livefyre如何组织内容。

本节概述了Livefyre网络架构。

## 网络和站点概述

Livefyre按网络和站点组织用户和内容。 每个网络都可能有一个或多个用户帐户与其关联，并且每个网络可能包括一个或多个Livefyre站点。 Livefyre站点是集合的任意分组。 一个集合映射到CMS中的一个文章ID。

## 了解网络{#section_hqt_4m4_xz}

具有多个域的客户可以使用单个Livefyre网络在所有域中共享用户帐户。 希望为不同域保留单独用户帐户的客户需要单独的Livefyre网络。

配置设置可以应用于站点、网络和集合（在上图中称为对话）。

>[!NOTE]
>
>某些设置仅在网络级别可用（例如，电子邮件通知首选项、地址电子邮件和电子邮件自定义徽标）。 如果您希望这些设置对每个域都不同，则必须使用多个网络。

## 了解站点{#section_vjw_nm4_xz}

站点是文章的任意分组。 分组非常有用，因为它允许您将不同的主持人分配给不同的内容组。 审核者和所有者可以设置为审核内容并在网络或站点级别配置管理员设置。 如果您希望某些版主仅看到某些集合，则这些集合可能会设置为单独的Livefyre站点。

>[!NOTE]
>
>您在自定义网络下拥有的站点数量没有限制。

## 应用程序序列图{#section_mw2_lm4_xz}

无论您是希望使用Livefyre提供的端点实现自定义功能，还是只需调试问题，了解Livefyre应用程序请求/响应流的工作方式都会有所帮助。

![](assets/appsequencediagram.png)

1. 当客户端点击您的站点时，使用站点ID和文章ID实例化Livefyre应用程序。
1. 如果您希望验证用户身份（对流量评估以及站点保护都很有价值），请向Livefyre发送站点信息和用户用户档案令牌。
1. 发送Livefyre站点ID和文章ID以初始化应用程序。

   Livefyre返回初始内容。

   将此内容发送到页面并显示应用程序。

1. 要更新页面上显示的内容，请从您的页面向Livefyre发送最新的事件ID。 如果有任何新内容可用，则将返回该内容。

   使用新内容重新加载页面，并无限次重复此过程。

1. 如果您允许用户发布新内容，则在您的网站上发布新内容时触发事件，以将内容发布到Livefyre。 Livefyre将返回更新的流，您可以用它更新您的站点。
