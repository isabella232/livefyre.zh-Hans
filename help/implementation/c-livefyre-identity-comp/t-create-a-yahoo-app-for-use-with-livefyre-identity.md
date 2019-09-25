---
description: 您可以将Livefyre Identity与Yahoo! 允许用户使用其Yahoo! 登录以与站点上的应用程序交互。
seo-description: 您可以将Livefyre Identity与Yahoo! 允许用户使用其Yahoo! 登录以与站点上的应用程序交互。
seo-title: 创建Yahoo! 与Livefyre identity一起使用的应用程序
solution: Experience Manager
title: 创建Yahoo! 与Livefyre identity一起使用的应用程序
uuid: 6863cd2e-eb0d-465b-b706-88ecaccf41bc
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建Yahoo! 与Livefyre identity一起使用的应用程序{#create-a-yahoo-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Yahoo! 允许用户使用其Yahoo! 登录以与站点上的应用程序交互。

要允许用户使用其Yahoo凭据登录，Livefyre需要以下Yahoo应用程序信息：

* 客户端ID（用户密钥）
* 客户端机密（消费者机密）

创建Yahoo! 与Livefyre identity一起使用的应用程序：

1. 转到 [https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)，然后登录您的Yahoo! 帐户，以创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. Select **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. 选择 **[!UICONTROL API Permissions: Profiles (Social Directory)]** 和 **[!UICONTROL Read Public]**。

   完成后，Yahoo的应用程序详细信息页面将列出该应用程序的客户端ID（消费者密钥）和客户端机密（消费者机密），以便在Studio的“集成设置”页面中使用。

   >[!NOTE]
   >
   >如果启用Yahoo! 无需创建Yahoo! 应用程序时，如果您将Studio中的“客户端ID”和“客户端机密”字段留空，则Livefyre将使用OpenID将这些用户登录到Livefyre应用程序。 在这种情况下，OAuth和自定义品牌将不可用。