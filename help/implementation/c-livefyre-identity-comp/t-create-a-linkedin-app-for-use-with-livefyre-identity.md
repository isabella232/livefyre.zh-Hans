---
description: 您可以将Livefyre Identity与LinkedIn结合使用，以允许用户使用其LinkedIn登录名在您的网站上交互应用程序。
seo-description: 您可以将Livefyre Identity与LinkedIn结合使用，以允许用户使用其LinkedIn登录名在您的网站上交互应用程序。
seo-title: 创建用于Livefyre Identity的LinkedIn应用程序
solution: Experience Manager
title: 创建用于Livefyre Identity的LinkedIn应用程序
uuid: c5112f24-a4e0-4526-afe8-b8f27a3b2854
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# 创建用于Livefyre Identity的LinkedIn应用程序{#create-a-linkedin-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与LinkedIn结合使用，以允许用户使用其LinkedIn登录名在您的网站上交互应用程序。

要启用LinkedIn登录，Livefyre需要以下LinkedIn应用程序信息：

* 消费方密钥（API密钥）
* 消费方密码（API机密）

要创建用于Livefyre Identity的LinkedIn应用程序，请执行以下操作：

1. 转到https://www.linkedin.com/secure/developer，然后登录您的LinkedIn帐户以创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 单击 **[!UICONTROL Create Application]**.
1. 填写表单以创建应用程序。
1. 在&#x200B;**[!UICONTROL Default Application Permissions]**&#x200B;中，启用&#x200B;**[!UICONTROL r_basicprofile]**&#x200B;和&#x200B;**[!UICONTROL r_emailaddress]**&#x200B;应用程序权限。
1. 输入&#x200B;**[!UICONTROL OAuth 2.0 Authorized Redirect URL]**&#x200B;作为`https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`。
1. 保存应用程序。
1. 在&#x200B;**[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**&#x200B;中，将&#x200B;**[!UICONTROL Enable LinkedIn Login]**&#x200B;切换到&#x200B;**[!UICONTROL On]**。
1. 输入LinkedIn客户端ID和LinkedIn客户端机密。
1. 单击 **[!UICONTROL Save Settings]**.

完成后，LinkedIn的应用程序详细信息页面将列表应用程序的API密钥(消费方密钥)和API密钥(消费方密码)，以便在Studio的“集成设置”页面中使用。
