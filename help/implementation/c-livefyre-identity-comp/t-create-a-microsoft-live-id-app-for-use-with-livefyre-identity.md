---
description: 您可以将Livefyre Identity与Microsoft Live Identity结合使用，允许用户使用Facebook登录来在您的网站上交互应用程序。
seo-description: 您可以将Livefyre Identity与Microsoft Live Identity结合使用，允许用户使用Facebook登录来在您的网站上交互应用程序。
seo-title: 创建用于Livefyre Identity的Microsoft Live Identity应用程序
solution: Experience Manager
title: 创建用于Livefyre Identity的Microsoft Live Identity应用程序
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建用于Livefyre Identity的Microsoft Live Identity应用程序{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Microsoft Live Identity结合使用，允许用户使用Facebook登录来在您的网站上交互应用程序。

为了允许用户使用Microsoft Live Identity凭据登录，Livefyre需要以下Microsoft Live标识信息：

* 客户端ID(私钥)
* 客户端机密(密码)

要创建用于Livefyre Identity的Microsoft Live Identity应用程序，请执行以下操作：

1. 在 [https://apps.dev.microsoft.com上创建或登录Microsoft Live帐户](https://apps.dev.microsoft.com/)
1. 创建新的或选择现有应用程序以与Livefyre Identity结合使用。
1. 单击 **[!UICONTROL Add Platform]**，然后选择Web作为平台类型。
1. 确保选中 **[!UICONTROL Allow Implicit Flow]** 此选项，并使用您的网络名称而不是{network-name}输入重定向URL： `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`。
1. 生成新密码/密钥对以获取私钥。
1. 在中 **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**，切换 **[!UICONTROL Enable Microsoft Live Login]** 切换到 **[!UICONTROL On]**。
1. 输入Microsoft Live Client ID和Microsoft Live Client机密。
1. 单击 **[!UICONTROL Save Settings]**。

完成后，Microsoft Live Identity的应用程序详细信息页面将列出应用程序的客户端ID(消费者密钥)和客户端机密(消费者机密)，以供在Studio的集成设置页面中使用。
