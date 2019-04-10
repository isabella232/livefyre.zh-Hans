---
description: Livefyre Studio的实施期望。
seo-description: Livefyre Studio的实施期望。
seo-title: 实施过程
solution: Experience Manager
title: 实施过程
uuid: 9f394e-3467-47d1-9816-45e2130db440
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 实施过程{#implementation-process}

实施Livefyre的时间长短取决于您的实施和工作范围。

## Livefyre网络体系结构概述 {#section_dgj_l32_rbb}

Livefyre在讨论网络架构方面使用以下条款：

* 网络。您计划使用Livefyre的顶级域。
* 站点。属于网络的子域或站点部分。
* 应用程序。在站点上呈现内容。内容以可视方式显示在应用程序中，使用可视化应用程序(Mosaic、传送、功能卡等)或使用“对话应用程序”(评论、评论、聊天等)的文本格式。您可以在网站上放置一个或多个应用程序。
* 流。流是指搜索社交媒体和其他站点以自动收集内容以便在应用程序中进行协调或直接发布的过滤器。
* 内容(例如UGC、评论)。应用程序中显示的内容。内容可以是可视的(例如，照片或视频)、纯音频或文本。

下图显示了网络、站点、应用程序和内容之间的关系。

![](assets/network_site_architecture.png)

您有自己的Livefyre实例，它是用于协调内容、管理用户等的中央仪表板。联系您的CSM以访问Livefyre实例。

## 集成步骤 {#section_s2j_d2x_tz}

集成Livefyre有三个主要步骤：

* 应用程序集成

   实施Livefyre时，实施的样式取决于您的用例。有关 [每个实施类型](/help/implementation/c-getting-started/c-implementation-process/c-app-integration-types.md#c_app_integration_types)的更多信息。

* 身份验证集成

   您必须将现有用户管理系统与Livefyre集成，用于对话应用程序以及需要在您的站点上进行最终用户身份验证的任何其他应用程序。如果当前没有使用用户管理工具，则可以使用Livefyre Identity。[有关Livefyre Identity、它是什么以及如何设置它的更多信息](/help/implementation/c-livefyre-identity-comp/c-livefyre-identity-comp.md#c_livefyre_identity)，请访问。

* 自定义

   自定义是可选的，但大多数客户自定义App以适合其品牌。

