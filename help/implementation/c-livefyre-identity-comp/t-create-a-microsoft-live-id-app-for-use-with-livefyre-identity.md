---
description: 您可以将Livefyre Identity与Microsoft Live Identity一起使用，以允许用户使用其Facebook登录名在您的网站上与应用程序交互。
seo-description: 您可以将Livefyre Identity与Microsoft Live Identity一起使用，以允许用户使用其Facebook登录名在您的网站上与应用程序交互。
seo-title: 创建用于Livefyre Identity的Microsoft Live Identity应用程序
solution: Experience Manager
title: 创建用于Livefyre Identity的Microsoft Live Identity应用程序
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# 创建用于Livefyre Identity的Microsoft Live Identity应用程序{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Microsoft Live Identity一起使用，以允许用户使用其Facebook登录名在您的网站上与应用程序交互。

要允许用户使用其Microsoft Live Identity凭据登录，Livefyre需要以下Microsoft Live Identity信息：

* 客户端ID（私钥）
* 客户端密码（密码）

要创建用于Livefyre Identity的Microsoft Live Identity应用程序，请执行以下操作：

1. 创建或登录位于[https://apps.dev.microsoft.com](https://apps.dev.microsoft.com/)的Microsoft Live帐户
1. 创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 单击&#x200B;**[!UICONTROL Add Platform]**，然后选择Web作为平台类型。
1. 确保选中&#x200B;**[!UICONTROL Allow Implicit Flow]**&#x200B;选项，并使用网络名称输入重定向URL，而不是{network-name}:`https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`。
1. 生成新密码／密钥对以获取私钥。
1. 在&#x200B;**[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**&#x200B;中，将&#x200B;**[!UICONTROL Enable Microsoft Live Login]**&#x200B;切换到&#x200B;**[!UICONTROL On]**。
1. 输入Microsoft Live Client ID和Microsoft Live Client Secret。
1. 单击 **[!UICONTROL Save Settings]**.

完成后，Microsoft Live Identity的应用程序详细信息页面将列表该应用程序的Client ID(消费方密钥)和Client Secret(消费方密码)，以便在Studio的“集成设置”页中使用。
