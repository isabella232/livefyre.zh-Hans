---
description: 您可以将Livefyre Identity与LinkedIn结合使用，以允许用户使用其LinkedIn登录在您的站点上与应用程序交互。
seo-description: 您可以将Livefyre Identity与LinkedIn结合使用，以允许用户使用其LinkedIn登录在您的站点上与应用程序交互。
seo-title: 创建LinkedIn应用程序以与Livefyre Identity一起使用
solution: Experience Manager
title: 创建LinkedIn应用程序以与Livefyre Identity一起使用
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建LinkedIn应用程序以与Livefyre Identity一起使用{#create-a-linkedin-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与LinkedIn结合使用，以允许用户使用其LinkedIn登录在您的站点上与应用程序交互。

要启用LinkedIn登录，Livefyre需要以下LinkedIn应用程序信息：

* 消费者密钥（API密钥）
* 消费者机密（API机密）

要创建用于Livefyre identity的LinkedIn应用程序，请执行以下操作：

1. 转到https://www.linkedin.com/secure/developer，然后登录您的LinkedIn帐户以创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 单击 **[!UICONTROL Create Application]**.
1. 填写表单以创建应用程序。
1. 在中，启 **[!UICONTROL Default Application Permissions]**&#x200B;用应用程序 **[!UICONTROL r_basicprofile]** 和应用 **[!UICONTROL r_emailaddress]** 程序权限。
1. 输入 **[!UICONTROL OAuth 2.0 Authorized Redirect URL]** 为 `https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`。
1. 保存应用程序。
1. 在中 **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**，将切换 **[!UICONTROL Enable LinkedIn Login]** 切换到 **[!UICONTROL On]**。
1. 输入LinkedIn客户端ID和LinkedIn客户端机密。
1. 单击 **[!UICONTROL Save Settings]**.

完成后，LinkedIn的应用程序详细信息页面将列出该应用程序的API密钥(Consumer Key)和API密钥(Consumer Secret)，以便在Studio的“集成设置”页中使用。
