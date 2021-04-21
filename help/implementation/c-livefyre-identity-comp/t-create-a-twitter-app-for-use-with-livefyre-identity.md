---
description: 您可以将Livefyre Identity与Twitter结合使用，以允许用户使用其Twitter登录在您的站点上与应用程序交互。
title: 创建用于Livefyre Identity的Twitter应用程序
exl-id: 4f2b919f-fe5d-49a3-8432-04ffb3d68ce4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---

# 创建用于Livefyre Identity{#create-a-twitter-app-for-use-with-livefyre-identity}的Twitter应用程序

您可以将Livefyre Identity与Twitter结合使用，以允许用户使用其Twitter登录在您的站点上与应用程序交互。

要启用Twitter登录，Livefyre需要以下Twitter应用程序信息：

* 消费方密钥（API密钥）
* 消费方密码（API机密）

要创建与Livefyre Identity一起使用的Twitter应用程序，请执行以下操作：

1. 转至[https://apps.twitter.com/](https://apps.twitter.com/)，然后登录您的Twitter帐户以创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 从应用程序的“设置”页面：

   * 输入&#x200B;**[!UICONTROL Callback URL:]** `https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre`(其中&#x200B;**{networkName}**&#x200B;是您的Livefyre提供的网络名称。 例如：** [!UICONTROL labs]***（**[!UICONTROL `labs.fyre.co`]**&#x200B;中）。
   * 取消选择 **[!UICONTROL Enable Callback Locking]**.
   * 选择 **[!UICONTROL Allow this application to be used to Sign in with Twitter]**.

1. 从&#x200B;**[!UICONTROL Permissions]**&#x200B;选项卡中，选择&#x200B;**[!UICONTROL Access: Read only]**。

完成后，Twitter的“应用程序管理”>“密钥和访问令牌”页将列表应用程序的消费方密钥（API密钥）和消费方密码（API密钥），以在Studio的“集成设置”页中使用。
