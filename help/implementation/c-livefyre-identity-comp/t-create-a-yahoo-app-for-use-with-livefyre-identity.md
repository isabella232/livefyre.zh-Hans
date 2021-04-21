---
description: 您可以将Livefyre Identity与Yahoo! 允许用户使用他们的Yahoo! 登录以与您网站上的应用程序进行交互。
title: 创建Yahoo! 与Livefyre Identity一起使用的应用程序
exl-id: 6b4c6ea9-1cb0-4496-aabe-70811f464a3d
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---

# 创建Yahoo! 与Livefyre Identity一起使用的应用程序{#create-a-yahoo-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Yahoo! 允许用户使用他们的Yahoo! 登录以与您网站上的应用程序进行交互。

要允许您的用户使用其Yahoo凭据登录，Livefyre需要以下Yahoo应用程序信息：

* 客户端ID(消费方密钥)
* 客户机密码(消费方密码)

创建Yahoo! 与Livefyre Identity一起使用的应用程序：

1. 转到[https://developer.yahoo.com/apps/](https://developer.yahoo.com/apps/)并登录您的Yahoo! 帐户创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 选择 **[!UICONTROL Application Type: Web Application]**.
1. Enter **[!UICONTROL Callback Domain:]** `https://identity.livefyre.com`
1. 选择&#x200B;**[!UICONTROL API Permissions: Profiles (Social Directory)]**&#x200B;和&#x200B;**[!UICONTROL Read Public]**。

   完成后，Yahoo的应用程序详细信息页面将列表该应用程序的客户端ID(消费方密钥)和客户端机密(消费方密码)，以在Studio的“集成设置”页面中使用。

   >[!NOTE]
   >
   >如果启用Yahoo! 无需创建Yahoo! 应用程序，如果您将Studio中的“客户端ID”和“客户端机密”字段留空，则Livefyre将使用OpenID将这些用户登录到您的Livefyre应用程序。 在这种情况下，OAuth和自定义品牌将不可用。
