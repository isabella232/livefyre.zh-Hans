---
description: 您可以将Livefyre Identity与Facebook结合使用，以允许用户使用其Facebook登录与您站点上的应用程序交互。
title: 创建用于Livefyre Identity的Facebook应用程序
exl-id: ec320865-6ea3-4f6f-a5f6-31f3d5cbdc93
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 1%

---

# 创建用于Livefyre Identity{#create-a-facebook-app-for-use-with-livefyre-identity}的Facebook应用程序

您可以将Livefyre Identity与Facebook结合使用，以允许用户使用其Facebook登录与您站点上的应用程序交互。

要允许您的用户使用其Facebook凭据登录，Livefyre需要以下Facebook应用程序信息：

* 应用程序 ID
* App Secret

要创建与Livefyre Identity一起使用的Facebook应用程序，请执行以下操作：

1. 转到[https://developers.facebook.com/apps](https://developers.facebook.com/apps)。
1. 登录您的Facebook开发人员帐户。
1. 单击&#x200B;**[!UICONTROL Add New App]**&#x200B;或选择一个现有应用程序以与Livefyre Identity一起使用。
1. 单击&#x200B;**[!UICONTROL Settings]**，然后单击&#x200B;**[!UICONTROL Basic]**。 输入&#x200B;**[!UICONTROL Contact Email]**&#x200B;地址、**[!UICONTROL Display Name]**、**[!UICONTROL Privacy Policy URL]**&#x200B;和&#x200B;**[!UICONTROL Terms of Service URL]**。
1. 单击&#x200B;**[!UICONTROL Products]**&#x200B;旁边的加号(**[!UICONTROL +]**)。
1. 单击&#x200B;**[!UICONTROL Facebook Login]**&#x200B;下的&#x200B;**[!UICONTROL Set Up]**。
1. 单击&#x200B;**[!UICONTROL Settings]**&#x200B;并设置以下内容：

   * 将&#x200B;**[!UICONTROL Client OAuth Login]**&#x200B;设置为&#x200B;**[!UICONTROL Yes]**。
   * 将&#x200B;**[!UICONTROL Web OAuth Login]**&#x200B;设置为&#x200B;**[!UICONTROL Yes]**。
   * 将&#x200B;**[!UICONTROL Use Strict Mode for Redirect URIs]**&#x200B;设置为&#x200B;**[!UICONTROL Yes]**。
   * 将&#x200B;**[!UICONTROL Enforce HTTPS for Web OAuth Login]**&#x200B;设置为&#x200B;**[!UICONTROL Yes]**。
   * 在&#x200B;**[!UICONTROL Valid OAuth redirect URLs]**&#x200B;下，添加URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre`（其中`{networkName}`是您提供的Livefyre网络名称）。

1. 在&#x200B;**[!UICONTROL App Review]**&#x200B;下：

   * 将应用程序公开。
   * 确保&#x200B;**[!UICONTROL Login Permissions]**&#x200B;的&#x200B;**[!UICONTROL Approved Items]**&#x200B;包括`email`、`public_profile`和`user_friends`。

完成后，Facebook开发人员的仪表板页将列表您的App ID和App Secret，以在Studio的“集成设置”中使用。
