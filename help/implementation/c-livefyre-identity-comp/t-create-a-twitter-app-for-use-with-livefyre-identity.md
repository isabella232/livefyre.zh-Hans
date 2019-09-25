---
description: 您可以将Livefyre Identity与Twitter结合使用，以允许用户使用其Twitter登录名在您的站点上交互应用程序。
seo-description: 您可以将Livefyre Identity与Twitter结合使用，以允许用户使用其Twitter登录名在您的站点上交互应用程序。
seo-title: 创建用于Livefyre identity的Twitter应用程序
solution: Experience Manager
title: 创建用于Livefyre identity的Twitter应用程序
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建用于Livefyre identity的Twitter应用程序{#create-a-twitter-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Twitter结合使用，以允许用户使用其Twitter登录名在您的站点上交互应用程序。

要启用Twitter登录，Livefyre需要以下Twitter应用程序信息：

* 消费者密钥（API密钥）
* 消费者机密（API机密）

要创建用于Livefyre Identity的Twitter应用程序，请执行以下操作：

1. 转到https://apps.twitter.com/ [](https://apps.twitter.com/)，然后登录您的Twitter帐户以创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 从应用程序的“设置”页面：

   * 输 **[!UICONTROL Callback URL:]** 入(其 `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` 中{networkName} **** 是您的Livefyre提供的网络名称。 For example:** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**.)
   * Deselect **[!UICONTROL Enable Callback Locking]**.
   * Select **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. 从选项卡 **[!UICONTROL Permissions]** 中，选择 **[!UICONTROL Access: Read only]**。

完成后，Twitter的“应用程序管理”&gt;“密钥和访问令牌”页将列出该应用程序的消费者密钥（API密钥）和消费者机密（API密钥），以便在Studio的“集成设置”页中使用。
