---
description: 您可以将Livefyre Identity与GitHub Identity结合使用，允许用户使用其GitHub登录功能在您的站点上交互应用程序。
seo-description: 您可以将Livefyre Identity与GitHub Identity结合使用，允许用户使用其GitHub登录功能在您的站点上交互应用程序。
seo-title: 创建用于Livefyre Identity的GithHub标识应用程序
title: 创建用于Livefyre Identity的GithHub标识应用程序
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 创建用于Livefyre Identity的GithHub标识应用程序{#create-a-github-identity-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与GitHub Identity结合使用，允许用户使用其GitHub登录功能在您的站点上交互应用程序。

为了允许用户使用其GitHub标识凭据登录，Livefyre需要以下GitHub标识信息：

* 客户端ID(私钥)
* 客户端机密(密码)

要创建用于Livefyre Identity的GithHub标识应用程序，请执行以下操作：

1. 在上创建或登录到GitHub帐户 [](https://github.com/settings/developers)。
1. 注册新的或选择现有的应用程序以用于Livefyre Identity。
1. 在表单中输入所有信息。请使用 **[!UICONTROL Authorization callback URL]**您的网络名称(而不是 `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`)输入。

1. 在中 **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**，切换 **[!UICONTROL Enable GitHub Login]** 切换到 **[!UICONTROL On]**。

1. 输入GitHub Client ID和GitHub客户端机密。
1. 单击 **[!UICONTROL Save Settings]**。

完成后，GitHub Identity的应用程序详细信息页面将列出应用程序的客户端ID(消费者密钥)和客户端机密(消费者机密)，以供在Studio的集成设置页面中使用。
