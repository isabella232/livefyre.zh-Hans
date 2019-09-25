---
description: 您可以将Livefyre Identity与Microsoft Live Identity结合使用，以允许用户使用其Facebook登录名在您的站点上交互应用程序。
seo-description: 您可以将Livefyre Identity与Microsoft Live Identity结合使用，以允许用户使用其Facebook登录名在您的站点上交互应用程序。
seo-title: 创建用于Livefyre identity的Microsoft Live Identity应用程序
solution: Experience Manager
title: 创建用于Livefyre identity的Microsoft Live Identity应用程序
uuid: 0c13e1bc-817f-43ed-85d5-09c9e95b6234
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建用于Livefyre identity的Microsoft Live Identity应用程序{#create-a-microsoft-live-identity-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Microsoft Live Identity结合使用，以允许用户使用其Facebook登录名在您的站点上交互应用程序。

要允许用户使用其Microsoft Live identity凭据登录，Livefyre需要以下Microsoft Live Identity信息：

* 客户端ID（私钥）
* 客户端密码（密码）

要创建用于Livefyre identity的Microsoft Live identity应用程序，请执行以下操作：

1. 在https://apps.dev.microsoft.com上创建或登录Microsoft live帐 [户](https://apps.dev.microsoft.com/)
1. 创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 单 **[!UICONTROL Add Platform]**&#x200B;击，然后选择Web作为平台类型。
1. 确保选中 **[!UICONTROL Allow Implicit Flow]** 此选项，并使用网络名称而不是{network-name}输入重定向URL: `https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/mslive_fyre`.
1. 生成新密码／密钥对以获取私钥。
1. 在中 **[!UICONTROL Livefyre Integration Settings Livefyre Identity Microsoft Live]**，将切换 **[!UICONTROL Enable Microsoft Live Login]** 切换到 **[!UICONTROL On]**。
1. 输入Microsoft Live Client ID和Microsoft Live Client Secret。
1. 单击 **[!UICONTROL Save Settings]**.

完成后，Microsoft Live identity的应用程序详细信息页面将列出该应用程序的Client ID(Consumer Key)和Client Secret(Consumer Secret)，以便在Studio的“集成设置”页面中使用。
