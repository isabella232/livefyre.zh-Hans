---
description: 您可以将Livefyre Identity与Facebook结合使用，以允许用户使用其Facebook登录与您网站上的应用程序进行交互。
seo-description: 您可以将Livefyre Identity与Facebook结合使用，以允许用户使用其Facebook登录与您网站上的应用程序进行交互。
seo-title: 创建Facebook应用程序以与Livefyre Identity一起使用
solution: Experience Manager
title: 创建Facebook应用程序以与Livefyre Identity一起使用
uuid: a7f7be4e-8986-4e79-831a-0bb0ae55599
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建Facebook应用程序以与Livefyre Identity一起使用{#create-a-facebook-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Facebook结合使用，以允许用户使用其Facebook登录与您网站上的应用程序进行交互。

要允许用户使用其Facebook凭据登录，Livefyre需要以下Facebook应用程序信息：

* 应用程序 ID
* 应用程序机密

要创建用于Livefyre identity的Facebook应用程序，请执行以下操作：

1. 请访问 [https://developers.facebook.com/apps](https://developers.facebook.com/apps)。
1. 登录您的Facebook开发人员帐户。
1. 单击 **[!UICONTROL Add New App]** 或选择现有应用程序以与Livefyre Identity一起使用。
1. 单 **[!UICONTROL Settings]**&#x200B;击，然后 **[!UICONTROL Basic]**。 输入 **[!UICONTROL Contact Email]** 地址、 **[!UICONTROL Display Name]**、 **[!UICONTROL Privacy Policy URL]**&#x200B;和 **[!UICONTROL Terms of Service URL]**。
1. 单击旁边的加号( **[!UICONTROL +]**) **[!UICONTROL Products]**。
1. 单击下 **[!UICONTROL Set Up]** 面的 **[!UICONTROL Facebook Login]**。
1. 单 **[!UICONTROL Settings]** 击并设置以下内容：

   * Set **[!UICONTROL Client OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Web OAuth Login]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Use Strict Mode for Redirect URIs]** to **[!UICONTROL Yes]**.
   * Set **[!UICONTROL Enforce HTTPS for Web OAuth Login]** to **[!UICONTROL Yes]**.
   * 在下 **[!UICONTROL Valid OAuth redirect URLs]**&#x200B;面，添加URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (其中 `{networkName}` 是您提供的Livefyre网络名称)。

1. Under **[!UICONTROL App Review]**:

   * 将应用程序公开。
   * 确保 **[!UICONTROL Approved Items]** 包含、 **[!UICONTROL Login Permissions]** 和 `email``public_profile``user_friends`。

完成后，Facebook开发人员的“控制面板”页面将列出您的App ID和App Secret，以便在Studio的“集成设置”中使用。
