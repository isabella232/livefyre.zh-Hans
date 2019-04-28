---
description: 您可以使用Livefyre Identity with Twitter，允许用户使用Twitter登录来在您的网站上交互应用程序。
seo-description: 您可以使用Livefyre Identity with Twitter，允许用户使用Twitter登录来在您的网站上交互应用程序。
seo-title: 创建用于Livefyre Identity的Twitter应用程序
solution: Experience Manager
title: 创建用于Livefyre Identity的Twitter应用程序
uuid: 841cce7c-618d-4154-85a3-1de96d04bb69
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建用于Livefyre Identity的Twitter应用程序{#create-a-twitter-app-for-use-with-livefyre-identity}

您可以使用Livefyre Identity with Twitter，允许用户使用Twitter登录来在您的网站上交互应用程序。

要启用Twitter登录，Livefyre需要以下Twitter应用程序信息：

* 消费者密钥(API密钥)
* 消费者机密(API机密)

要创建用于Livefyre Identity的Twitter应用程序，请执行以下操作：

1. 转到 [https://apps.twitter.com/](https://apps.twitter.com/)，然后登录到您的Twitter帐户以创建新的应用程序，或选择现有的应用程序以用于Livefyre Identity。
1. 从应用程序的设置页面中：

   * 输入 **[!UICONTROL Callback URL:]**`https://identity.livefyre.com/{networkName}.fyre.co/api/v1.0/public/profile/social/complete/twitter_fyre` (其中 **{search名称}** 是您的Livefyre提供的网络名称)。例如：** [!UICONTROL labs]** in **[!UICONTROL `labs.fyre.co`]**)
   * 取消选择 **[!UICONTROL Enable Callback Locking]**。
   * 选择 **[!UICONTROL Allow this application to be used to Sign in with Twitter]**。

1. 从 **[!UICONTROL Permissions]** 选项卡中选择 **[!UICONTROL Access: Read only]**。

完成后，Twitter的“应用程序管理”&gt;“密钥和访问令牌”页面将列出应用程序的用户密钥(API密钥)和消费者机密(API机密)，以便在Studio的“集成设置”页中使用。
