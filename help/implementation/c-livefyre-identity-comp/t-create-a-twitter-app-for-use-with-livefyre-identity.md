---
description: 您可以将Livefyre Identity与Twitter一起使用，以允许用户使用其Twitter登录名在您的站点上交互应用程序。
seo-description: 您可以将Livefyre Identity与Twitter一起使用，以允许用户使用其Twitter登录名在您的站点上交互应用程序。
seo-title: 创建用于Livefyre Identity的Twitter应用程序
solution: Experience Manager
title: 创建用于Livefyre Identity的Twitter应用程序
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 1%

---


# 创建用于Livefyre Identity的Twitter应用程序{#create-a-twitter-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Twitter一起使用，以允许用户使用其Twitter登录名在您的站点上交互应用程序。

要启用Twitter登录，Livefyre需要以下Twitter应用程序信息：

* 消费方密钥（API密钥）
* 消费方密码（API机密）

要创建用于Livefyre Identity的Twitter应用程序，请执行以下操作：

1. 转至[https://apps.twitter.com/](https://apps.twitter.com/)，然后登录您的Twitter帐户以创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 从应用程序的“设置”页面：

   * 输入&#x200B;**[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre`(其中&#x200B;**{networkName}**&#x200B;是您的Livefyre提供的网络名称。 例如：** [!UICONTROL labs]**在&#x200B;**[!UICONTROL `labs.fyre.co`]**&#x200B;中。)
   * 取消选择 **[!UICONTROL Enable Callback Locking]**.
   * 选择 **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. 从&#x200B;**[!UICONTROL Permissions]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Access: Read only]**。

完成后，Twitter的“应用程序管理”>“密钥和访问令牌”页将列表应用程序的消费方密钥（API密钥）和消费方密码（API密钥），以便在Studio的“集成设置”页中使用。
