---
description: 您可以将Livefyre Identity与GitHub Identity结合使用，以允许用户使用其GitHub登录在您的站点上与应用程序交互。
seo-description: 您可以将Livefyre Identity与GitHub Identity结合使用，以允许用户使用其GitHub登录在您的站点上与应用程序交互。
seo-title: 创建用于Livefyre identity的GitHub标识应用程序
title: 创建用于Livefyre identity的GitHub标识应用程序
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建用于Livefyre identity的GitHub标识应用程序{#create-a-github-identity-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与GitHub Identity结合使用，以允许用户使用其GitHub登录在您的站点上与应用程序交互。

要允许用户使用其GitHub身份凭证登录，Livefyre需要以下GitHub身份信息：

* 客户端ID（私钥）
* 客户端密码（密码）

要创建用于Livefyre identity的GitHub Identity应用程序，请执行以下操作：

1. 在上创建或登录GitHub帐户 [](https://github.com/settings/developers)。
1. 注册新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 在表单上输入所有信息。 请输 **[!UICONTROL Authorization callback URL]**&#x200B;入网络名称，而不是 `{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`。

1. 在中 **[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**，将切换 **[!UICONTROL Enable GitHub Login]** 切换到 **[!UICONTROL On]**。

1. 输入GitHub客户端ID和GitHub客户端机密。
1. 单击 **[!UICONTROL Save Settings]**.

完成后，GitHub Identity的应用程序详细信息页面将列出App的Client ID(Consumer Key)和Client Secret(Consumer Secret)，以便在Studio的“集成设置”页面中使用。
