---
description: 您可以将Livefyre Identity与Yahoo！以允许用户使用其Yahoo！登录到您网站上的应用程序。
seo-description: 您可以将Livefyre Identity与Yahoo！以允许用户使用其Yahoo！登录到您网站上的应用程序。
seo-title: 创建Yahoo！用于Livefyre Identity的应用程序
solution: Experience Manager
title: 创建Yahoo！用于Livefyre Identity的应用程序
uuid: 6863cd2e-eb0 d-465b-b706-88ecacf41 bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建Yahoo！用于Livefyre Identity的应用程序{#create-a-yahoo-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Yahoo！以允许用户使用其Yahoo！登录到您网站上的应用程序。

为了允许用户使用其Yahoo凭据登录，Livefyre需要以下Yahoo应用程序信息：

* 客户端ID(消费者密钥)
* 客户端机密(消费者机密)

要创建Yahoo！应用程序用于Livefyre Identity：

1. 转到 [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)，然后登录Yahoo！account to create a new or select a现有app for use with Livefyre Identity.
1. 选择 **[!UICONTROL Application Type: Web Application]**。
1. Enter **[!UICONTROL Callback Domain:]**`https://identity.livefyre.com`
1. 选择 **[!UICONTROL API Permissions: Profiles (Social Directory)]****[!UICONTROL Read Public]**和.

   完成后，Yahoo的应用程序详细信息页面将列出应用程序的客户端ID(消费者密钥)和客户端机密(消费者机密)，以供在Studio的集成设置页面中使用。

   >[!NOTE]
   >
   >如果您启用Yahoo！登录而无需创建Yahoo！应用程序，如果您将Studio中的Client ID和Client Secret字段保留为空，Livefyre将使用openID将这些用户登录到您的Livefyre应用程序。在这种情况下，不提供OAuth和自定义品牌。