---
description: 您可以将Livefyre Identity与GitHub Identity结合使用，以允许用户使用其GitHub登录名在您的站点上交互应用程序。
seo-description: 您可以将Livefyre Identity与GitHub Identity结合使用，以允许用户使用其GitHub登录名在您的站点上交互应用程序。
seo-title: 创建用于Livefyre Identity的GitHub Identity应用程序
title: 创建用于Livefyre Identity的GitHub Identity应用程序
uuid: cf56164c-1521-4a42-89cb-39483764807e
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# 创建用于Livefyre Identity的GitHub Identity应用程序{#create-a-github-identity-app-for-use-with-livefyre-identity}

您可以将Livefyre Identity与GitHub Identity结合使用，以允许用户使用其GitHub登录名在您的站点上交互应用程序。

要允许用户使用其GitHub身份凭据登录，Livefyre需要以下GitHub身份信息：

* 客户端ID（私钥）
* 客户端密码（密码）

要创建用于Livefyre Identity的GitHub Identity应用程序，请执行以下操作：

1. 创建或登录位于[](https://github.com/settings/developers)的GitHub帐户。
1. 注册新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 在表单上输入所有信息。 输入&#x200B;**[!UICONTROL Authorization callback URL]**，使用网络名称而不是`{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`。

1. 在&#x200B;**[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**&#x200B;中，将&#x200B;**[!UICONTROL Enable GitHub Login]**&#x200B;切换到&#x200B;**[!UICONTROL On]**。

1. 输入GitHub客户端ID和GitHub客户端机密。
1. 单击 **[!UICONTROL Save Settings]**.

完成后，GitHub Identity的应用程序详细信息页面将列表App的Client ID(消费方密钥)和Client Secret(消费方密码)，以便在Studio的“集成设置”页面中使用。
