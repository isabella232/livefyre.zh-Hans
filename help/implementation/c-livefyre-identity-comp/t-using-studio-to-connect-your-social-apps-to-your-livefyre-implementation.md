---
description: 要启用社交登录，请使用Studio将您的社交应用程序凭据添加到Livefyre集成中，并自定义登录模式。
seo-description: 要启用社交登录，请使用Studio将您的社交应用程序凭据添加到Livefyre集成中，并自定义登录模式。
seo-title: 使用Studio将您的社交应用程序连接到Livefyre实施
title: 使用Studio将您的社交应用程序连接到Livefyre实施
uuid: be14869c-e0df-48cd-a1f3-99eb953dd9ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用Studio将您的社交应用程序连接到Livefyre实施{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

要启用社交登录，请使用Studio将您的社交应用程序凭据添加到Livefyre集成中，并自定义登录模式。

## 自定义登录模式 {#section_v4c_hv2_3z}

登录模式允许您自定义用户登录应用程序时将看到的信息。 您可以自定义模态窗口。

* **** 徽标：上传徽标以在登录模式下使用。
* **** 字体系列：选择与您的品牌匹配的字体。
* **** 品牌颜色：输入要用于模态中特定文本的十六进制颜色。
* **** 条款和条件URL:输入贵公司“条款和条件”页面的URL。 此字段是与Livefyre Identity一起使用的必需字段。

## 翻译Livefyre标识 {#section_xxt_z52_3z}

您可以在Livefyre Identity中创建和修改文本字符串的翻译集。

有关将翻译集与Livefyre Identity结合使用的更多信息，请参阅翻译集。

有关可为Livefyre Identity自定义的特定字符串的详细信息，请参阅Livefyre Identity。

## 启用电子邮件登录 {#section_dlv_wzt_bbb}

允许用户使用其电子邮件地址登录并与站点上的应用程序交互。

要使用Livefyre本机帐户启用登录，请执行以下操作：

1. 在Livefyre **[!UICONTROL Integration Settings]** Studio中导航到。
1. 将切换 **[!UICONTROL Enable Login with Email]** 切换到 **[!UICONTROL On]**。

## 使用Facebook帐户启用登录 {#section_ph3_515_bbb}

将您的Facebook帐户连接到Livefyre，以允许用户使用其Facebook登录名与您站点上的应用程序交互。

要使用Facebook帐户启用登录，请执行以下操作：

1. 将切换 **[!UICONTROL Enable Login with Facebook]** 切换到 **[!UICONTROL ON]**。

1. 添加您的Facebook应用程 **[!UICONTROL App ID]** 序和 **[!UICONTROL App Secret]**。

   这些值列在Facebook开发人员控制板中，该应用程序可从https://developers.facebook.com/apps/ [获取](https://developers.facebook.com/apps/675503539257343/dashboard/)。

## 启用Google登录 {#section_fq3_kb5_bbb}

将您的Google+帐户连接到Livefyre，以允许用户使用其Google+登录与您站点上的应用程序交互。

要使用Google+帐户启用登录，请执行以下操作：

1. 将切换 **[!UICONTROL Enable Login with Google]** 切换到 **[!UICONTROL ON]**。

1. 添加Google应用程序 **[!UICONTROL Client ID]** 和 **[!UICONTROL Client secret]**。

   这些值列在您的Google Cloud Platform项目界面中，可从https://console.cloud.google.com/ [获取](https://console.cloud.google.com/apis/library)。 要检索此信息，请转到， **[!UICONTROL API Manager > Credentials]**&#x200B;然后单击项目名称。

## 使用Twitter帐户启用登录 {#section_iyz_wb5_bbb}

将您的Twitter帐户连接到Livefyre，以允许用户使用其Twitter登录名与您站点上的应用程序交互。

要使用Twitter帐户启用登录，请执行以下操作：

1. 将切换 **[!UICONTROL Enable Login with Twitter]** 切换到 **[!UICONTROL ON]**。

1. 添加您的Twitter应用程 **[!UICONTROL Consumer Key (API Key)]** 序和 **[!UICONTROL Consumer Secret (API Secret)]**。

   这些值列在您的Twitter应用程序页面中， **[!UICONTROL Keys and Access Tokens]** 可从https://apps.twitter.com/ [获取](https://apps.twitter.com/)。

## 启用使用Yahoo! 帐户 {#section_s1q_3c5_bbb}

连接您的Yahoo! 帐户，以允许用户使用其Yahoo! 登录以与站点上的应用程序交互。

使用Yahoo! account:

1. 将切换 **[!UICONTROL Enable Login with Yahoo!]** 切换到 **[!UICONTROL ON]**。

1. 添加您的Yahoo! 和 **[!UICONTROL Client ID]** 应 **[!UICONTROL Client Secret]**&#x200B;用

   这些值列在Yahoo! 应用程序详细信息页面，可从developer.yahoo.com/apps [获取](https://developer.yahoo.com/apps)。

## 使用Microsoft Live帐户启用登录 {#section_z42_4c5_bbb}

将您的Microsoft Live ID帐户连接到Livefyre，以允许用户使用其Microsoft Live ID登录与您站点上的应用程序交互。

要使用Microsoft Live ID帐户启用登录，请执行以下操作：

1. 在中 **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**，将切换 **[!UICONTROL Enable Microsoft Live Login]** 切换到 **[!UICONTROL On]**。

1. 输入和 **[!UICONTROL Microsoft Live Client ID (Private Key)]** 。 **[!UICONTROL Microsoft Live Client Secret (Password)]**

1. 单击 **[!UICONTROL Save Settings]**.

   Microsoft **[!UICONTROL Microsoft Live Client ID (Private Key)]** Live ID应 **[!UICONTROL Microsoft Live Client Secret (Password)]** 用程序详细信息页面中列出了这些值和值。

## 将您的社交应用程序连接到Livefyre Identity {#section_on2_vc5_bbb}

使您的用户能够将Livefyre identity实施用于站点上的应用程序。

1. 创建应用程序.
1. 导航到 **[!UICONTROL Studio]** &gt; **[!UICONTROL Settings]** &gt; **[!UICONTROL Integration Settings]**&gt; **[!UICONTROL Livefyre Identity]**。

1. 为您创建的应用程序输入所需的应用程序凭据。