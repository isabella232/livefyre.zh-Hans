---
description: 您可以将Livefyre Identity与Facebook结合使用，以允许用户使用Facebook登录来与您网站上的App交互。
seo-description: 您可以将Livefyre Identity与Facebook结合使用，以允许用户使用Facebook登录来与您网站上的App交互。
seo-title: 创建用于Livefyre Identity的Facebook应用程序
solution: Experience Manager
title: 创建用于Livefyre Identity的Facebook应用程序
uuid: a7f be4e-8986-4e79-831a-0bb0ae555599
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 创建用于Livefyre Identity的Facebook应用程序{#create-a-facebook-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与Facebook结合使用，以允许用户使用Facebook登录来与您网站上的App交互。

为了允许用户使用其Facebook凭据登录，Livefyre需要以下Facebook应用程序信息：

* App ID
* 应用程序机密

要创建用于Livefyre Identity的Facebook应用程序，请执行以下操作：

1. 转到 [https://developers.facebook.com/apps](https://developers.facebook.com/apps)。
1. 登录您的Facebook开发人员帐户。
1. 单击 **[!UICONTROL Add New App]** 或选择现有应用程序以用于Livefyre Identity。
1. 然后单击 **[!UICONTROL Settings]****[!UICONTROL Basic]**。输入 **[!UICONTROL Contact Email]** 地址 **[!UICONTROL Display Name]**、 **[!UICONTROL Privacy Policy URL]****[!UICONTROL Terms of Service URL]**和。
1. 单击旁边的加号( **[!UICONTROL +]**) **[!UICONTROL Products]**。
1. 单击 **[!UICONTROL Set Up]****[!UICONTROL Facebook Login]**下一步。
1. 单击 **[!UICONTROL Settings]** 并设置以下各项：

   * 设置 **[!UICONTROL Client OAuth Login]****[!UICONTROL Yes]**为。
   * 设置 **[!UICONTROL Web OAuth Login]****[!UICONTROL Yes]**为。
   * 设置 **[!UICONTROL Use Strict Mode for Redirect URIs]****[!UICONTROL Yes]**为。
   * 设置 **[!UICONTROL Enforce HTTPS for Web OAuth Login]****[!UICONTROL Yes]**为。
   * 在下 **[!UICONTROL Valid OAuth redirect URLs]**，添加URL `https://identity.livefyre.com/{networkName}/api/v1.0/public/profile/social/complete/facebook_fyre` (即 `{networkName}` 您的Livefyre提供的网络名称)。

1. **[!UICONTROL App Review]**下面：

   * 使应用程序公开。
   * 确保 **[!UICONTROL Approved Items]****[!UICONTROL Login Permissions]** 包括 `email`、 `public_profile`和 `user_friends`。

完成后，Facebook开发人员的仪表板页面将列出您的App ID和App Secret，以便在Studio的集成设置中使用。
