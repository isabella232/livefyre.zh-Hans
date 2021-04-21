---
description: 您可以将Livefyre Identity与GitHub Identity结合使用，以允许用户使用其GitHub登录名在您的站点上与应用程序交互。
title: 创建用于Livefyre Identity的GitHub标识应用程序
exl-id: f25ffd0e-ea4f-42ac-abfc-c02018421b85
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---

# 创建用于Livefyre Identity{#create-a-github-identity-app-for-use-with-livefyre-identity}的GitHub Identity应用程序

您可以将Livefyre Identity与GitHub Identity结合使用，以允许用户使用其GitHub登录名在您的站点上与应用程序交互。

要允许用户使用其GitHub身份凭证登录，Livefyre需要以下GitHub身份信息：

* 客户端ID（私钥）
* 客户端密码（密码）

要创建用于Livefyre Identity的GitHub Identity应用程序，请执行以下操作：

1. 在[](https://github.com/settings/developers)创建或登录到GitHub帐户。
1. 注册新应用程序或选择现有应用程序以与Livefyre Identity一起使用。
1. 在表单上输入所有信息。 输入&#x200B;**[!UICONTROL Authorization callback URL]**，使用网络名称代替`{network-name}: {network-name}: https://identy.livefyre.com/{network-name}.fyre.co/api/v.1.0/public/profile/social/complete/github_fyre`。

1. 在&#x200B;**[!UICONTROL Livefyre Integration Settings Livefyre Identity GitHub]**&#x200B;中，将&#x200B;**[!UICONTROL Enable GitHub Login]**&#x200B;切换到&#x200B;**[!UICONTROL On]**。

1. 输入GitHub客户端ID和GitHub客户端机密。
1. 单击 **[!UICONTROL Save Settings]**.

完成后，GitHub Identity的应用程序详细信息页面将列表App的Client ID(消费方密钥)和Client Secret(消费方密码)，以在Studio的“集成设置”页中使用。
