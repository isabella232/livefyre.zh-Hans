---
description: 要启用社交登录，请使用Studio将您的社交应用程序凭据添加到Livefyre集成，并自定义登录模式。
seo-description: 要启用社交登录，请使用Studio将您的社交应用程序凭据添加到Livefyre集成，并自定义登录模式。
seo-title: 使用Studio将社交应用程序连接到Livefyre实施
title: 使用Studio将社交应用程序连接到Livefyre实施
uuid: be14869c-e0 df-48cd-a1 f3-99eb953 dd9 ce
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用Studio将社交应用程序连接到Livefyre实施{#using-studio-to-connect-your-social-apps-to-your-livefyre-implementation}

要启用社交登录，请使用Studio将您的社交应用程序凭据添加到Livefyre集成，并自定义登录模式。

## 自定义登录模式 {#section_v4c_hv2_3z}

登录模式允许您自定义用户登录应用程序时将看到的信息。您可以自定义模态窗口。

* **徽标：** 上传徽标以在登录模式中使用。
* **字体系列：** 选择一种字体以匹配您的品牌。
* **品牌颜色：** 输入要用于模态中特定文本的十六进制颜色。
* **条款和条件URL：** 输入公司的“条款和条件”页面的URL。此字段用于Livefyre Identity。

## 翻译Livefyre Identity {#section_xxt_z52_3z}

您可以在Livefyre Identity中创建和修改文本字符串的翻译集。

有关使用带有Livefyre Identity的翻译集的更多信息，请参阅翻译集。

有关可为Livefyre Identity自定义的特定字符串，请参阅Livefyre标识。

## 启用通过电子邮件登录 {#section_dlv_wzt_bbb}

允许用户使用其电子邮件地址登录您的网站上的App并与之交互。

使用Livefyre本机帐户启用登录功能：

1. 在Livefyre **[!UICONTROL Integration Settings]** Studio中导航到。
1. 切换 **[!UICONTROL Enable Login with Email]** 切换到 **[!UICONTROL On]**。

## 启用使用Facebook帐户登录 {#section_ph3_515_bbb}

将您的Facebook帐户连接到Livefyre，允许用户使用其Facebook登录功能与您网站上的App交互。

使用Facebook帐户启用登录功能：

1. 切换 **[!UICONTROL Enable Login with Facebook]** 切换到 **[!UICONTROL ON]**。

1. 添加您的Facebook应用程序 **[!UICONTROL App ID]** 和 **[!UICONTROL App Secret]**。

   这些值在Facebook开发人员的仪表板中列出，可从 [https://developers.facebook.com/apps/](https://developers.facebook.com/apps/675503539257343/dashboard/)获得。

## 启用Google登录 {#section_fq3_kb5_bbb}

将您的Google+帐户连接到Livefyre，允许用户使用Google+登录功能与您网站上的App交互。

要使用Google+帐户启用登录，请执行以下操作：

1. 切换 **[!UICONTROL Enable Login with Google]** 切换到 **[!UICONTROL ON]**。

1. 添加您的Google应用程序 **[!UICONTROL Client ID]** 和 **[!UICONTROL Client secret]**。

   这些值列在您的Google Cloud Platform项目界面中，可从 [https://console.cloud.google.com/获得](https://console.cloud.google.com/apis/library)。要检索此信息，请转到 **[!UICONTROL API Manager > Credentials]**并单击项目名称。

## 使用Twitter帐户启用登录 {#section_iyz_wb5_bbb}

将您的Twitter帐户连接到Livefyre，允许用户使用其Twitter登录名与您网站上的App交互。

要使用Twitter帐户启用登录，请执行以下操作：

1. 切换 **[!UICONTROL Enable Login with Twitter]** 切换到 **[!UICONTROL ON]**。

1. 添加您的Twitter应用程序 **[!UICONTROL Consumer Key (API Key)]** 和 **[!UICONTROL Consumer Secret (API Secret)]**。

   这些值列在您的Twitter应用 **[!UICONTROL Keys and Access Tokens]** 程序页面中，可从 [https://apps.twitter.com/获取](https://apps.twitter.com/)。

## 启用使用Yahoo！帐户 {#section_s1q_3c5_bbb}

连接Yahoo！帐户，以允许用户使用其Yahoo！登录到您网站上的应用程序。

要启用使用Yahoo！帐户：

1. 切换 **[!UICONTROL Enable Login with Yahoo!]** 切换到 **[!UICONTROL ON]**。

1. 添加Yahoo！app和 **[!UICONTROL Client ID]****[!UICONTROL Client Secret]**.

   这些值在Yahoo！应用程序详细信息页面，可从 [developer.yahoo.com/apps获取](https://developer.yahoo.com/apps)。

## 启用使用Microsoft Live Account登录 {#section_z42_4c5_bbb}

将您的Microsoft Live ID帐户连接到Livefyre，允许用户使用其Microsoft Live ID登录功能与您网站上的应用程序交互。

要使用Microsoft Live ID帐户启用登录，请执行以下操作：

1. 在中 **[!UICONTROL Livefyre > Integration Settings > Livefyre Identity > Microsoft Live]**，切换 **[!UICONTROL Enable Microsoft Live Login]** 切换到 **[!UICONTROL On]**。

1. 输入 **[!UICONTROL Microsoft Live Client ID (Private Key)]** 和 **[!UICONTROL Microsoft Live Client Secret (Password)]**。

1. 单击 **[!UICONTROL Save Settings]**。

   这些 **[!UICONTROL Microsoft Live Client ID (Private Key)]****[!UICONTROL Microsoft Live Client Secret (Password)]** 值列在Microsoft Live ID应用程序详细信息页面中。

## 将社交应用程序连接到Livefyre Identity {#section_on2_vc5_bbb}

使用户能够对网站上的应用程序使用Livefyre标识实施。

1. 创建应用程序。
1. 导航到 **[!UICONTROL Studio]** > **[!UICONTROL Settings]** > **[!UICONTROL Integration Settings]**> **[!UICONTROL Livefyre Identity]**。

1. 为所创建的应用程序输入所需的应用程序凭据。