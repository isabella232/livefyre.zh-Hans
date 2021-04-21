---
description: 您可以将Livefyre Identity与LinkedIn结合使用，以允许用户使用其LinkedIn登录在您的站点上与应用程序交互。
title: 创建用于Livefyre Identity的LinkedIn应用程序
exl-id: e77eca6a-1698-414e-994e-1189f780ada1
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# 创建用于Livefyre Identity{#create-a-linkedin-app-for-use-with-livefyre-identity}的LinkedIn应用程序

您可以将Livefyre Identity与LinkedIn结合使用，以允许用户使用其LinkedIn登录在您的站点上与应用程序交互。

要启用LinkedIn登录，Livefyre需要以下LinkedIn应用程序信息：

* 消费方密钥（API密钥）
* 消费方密码（API机密）

要创建与Livefyre Identity一起使用的LinkedIn应用程序，请执行以下操作：

1. 转到https://www.linkedin.com/secure/developer，然后登录您的LinkedIn帐户以创建新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 单击 **[!UICONTROL Create Application]**.
1. 填写表单以创建应用程序。
1. 在&#x200B;**[!UICONTROL Default Application Permissions]**&#x200B;中，启用&#x200B;**[!UICONTROL r_basicprofile]**&#x200B;和&#x200B;**[!UICONTROL r_emailaddress]**&#x200B;应用程序权限。
1. 输入&#x200B;**[!UICONTROL OAuth 2.0 Authorized Redirect URL]**&#x200B;作为`https://identity.livefyre.com/{network-name}.fyre.co/api/v1.0/public/profile/social/complete/linkedin_fyre`。
1. 保存应用程序。
1. 在&#x200B;**[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > LinkedIn]**&#x200B;中，将&#x200B;**[!UICONTROL Enable LinkedIn Login]**&#x200B;切换到&#x200B;**[!UICONTROL On]**。
1. 输入LinkedIn Client ID和LinkedIn Client Secret。
1. 单击 **[!UICONTROL Save Settings]**.

完成后，LinkedIn的应用程序详细信息页面将列表该应用程序的API密钥(消费方密钥)和API密钥(消费方密码)，以在Studio的“集成设置”页中使用。
