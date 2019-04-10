---
description: 您可以将Livefyre Identity与LinkedIn结合使用，允许用户使用他们的LinkedIn登录功能在您的站点上交互应用程序。
seo-description: 您可以将Livefyre Identity与LinkedIn结合使用，允许用户使用他们的LinkedIn登录功能在您的站点上交互应用程序。
seo-title: 创建LinkedIn应用程序以与Livefyre Identity结合使用
solution: Experience Manager
title: 创建LinkedIn应用程序以与Livefyre Identity结合使用
uuid: c5112f24-a4 e0-4526-afe8-b8 f27 a3 b2854
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 创建LinkedIn应用程序以与Livefyre Identity结合使用{#create-a-linkedin-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与LinkedIn结合使用，允许用户使用他们的LinkedIn登录功能在您的站点上交互应用程序。

要启用LinkedIn登录，Livefyre需要以下LinkedIn应用程序信息：

* 消费者密钥(API密钥)
* 消费者机密(API机密)

要创建LinkedIn应用程序以用于Livefyre Identity：

1. 转到https://www.linkedin.com/secure/developer，然后登录您的LinkedIn帐户以创建新的应用程序或选择现有应用程序以用于Livefyre Identity。
1. 单击 **[!UICONTROL Create Application]**。
1. 填写表单以创建应用程序。
1. 在 **[!UICONTROL Default Application Permissions]**中，启用 **[!UICONTROL r_basicprofile]** 和 **[!UICONTROL r_emailaddress]** 应用权限。
1. 输入 **[!UICONTROL OAuth 2.0 Authorized Redirect URL]**`https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`as。
1. 保存应用程序。
1. 在中 **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**，切换 **[!UICONTROL Enable LinkedIn Login]** 切换到 **[!UICONTROL On]**。
1. 输入LinkedIn客户端ID和LinkedIn客户端机密。
1. 单击 **[!UICONTROL Save Settings]**。

完成后，LinkedIn的应用程序详细信息页面将列出应用程序的API密钥(消费者密钥)和API机密(消费者机密)，以供在Studio的集成设置页面中使用。
