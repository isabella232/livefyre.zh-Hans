---
description: 'null'
seo-description: 'null'
seo-title: Livefyre Identity的电子邮件
solution: Experience Manager
title: Livefyre Identity的电子邮件
uuid: 4e807803-687e-4df0-94d1-b18a48d024e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 1%

---


# Livefyre Identity的电子邮件{#emails-for-livefyre-identity}

Livefyre Identity发送以下电子邮件：

* [密码重置电子邮件](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [验证电子邮件](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [为用户发送电子邮件验证](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [欢迎电子邮件](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [向用户发送欢迎电子邮件](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

您可以自定义&#x200B;**[!UICONTROL Integration Settings > Email Notifications.]**&#x200B;中所有Livefyre Identity电子邮件的外观

## 密码重置电子邮件{#section_nd1_whs_p1b}

当用户尝试重置其密码时，Livefyre会自动发送密码重置电子邮件。

密码重置电子邮件如下所示：

**主题：重** 置密码

**正文：**

嘿，*&lt;username>*,

*&lt;network name>*&#x200B;上有更改用户档案密码的请求。

如果您请求使用此密码，请单击以下链接以选择新密码：*&lt;password reset URL>*。

*&lt;username>*、和 *&lt;network name=&quot;&quot;>*&#x200B;均 *&lt;password reset=&quot;&quot; URL=&quot;&quot;>* 根据站点访客和您的网络动态生成。

## 验证电子邮件{#section_ak5_xhs_p1b}

您可以发送电子邮件验证用户的电子邮件地址。 要发送验证电子邮件，必须打开&#x200B;**集成设置> Livefyre Identity**&#x200B;中的选项。

验证电子邮件如下所示：

**主题：电子** 邮件验证

**正文：**

您好&#x200B;*&lt;username>*,

请单击以下链接（或在浏览器中粘贴）验证您的帐户：*&lt;验证URL>*。

此链接将在24小时后过期。

谢谢，

*&lt;customer name>*&#x200B;团队

*&lt;username>*、和 *&lt;network name=&quot;&quot;>*&#x200B;均 *&lt;verification URL=&quot;&quot;>* 根据站点访客和您的网络动态生成。

## 向用户{#section_vyv_yhs_p1b}发送电子邮件验证

您可以向用户发送电子邮件，以验证他们用于注册帐户的电子邮件地址。 要发送验证电子邮件：

1. 在Studio中，单击齿轮图标可修改网络设置。
1. 单击&#x200B;**集成设置> Livefyre标识。**

1. 导航到&#x200B;**登录类型**。
1. 单击&#x200B;**要求电子邮件验证**&#x200B;以向验证用户用于注册帐户的电子邮件地址的用户发送电子邮件。
1. 导航到&#x200B;**网络电子邮件**&#x200B;以配置电子邮件&#x200B;**的**&#x200B;标志、要用作发件人地址的电子邮件地址（**电子邮件发件人**）以及要用于发件人电子邮件地址的显示名称（**电子邮件显示名称**）。

## 欢迎电子邮件 {#section_z2v_zhs_p1b}

您可以向用户发送欢迎电子邮件。 要发送欢迎电子邮件，必须打开&#x200B;**集成设置** > **Livefyre Identity**&#x200B;中的选项。

欢迎电子邮件如下所示：

**主题：** 欢迎使用  *&lt;customer name=&quot;&quot;>*

**正文：**

您好&#x200B;*&lt;username>*,

已在&#x200B;*&lt;customer name>*&#x200B;上为您创建帐户。

此帐户是在&#x200B;*&lt;referral URL>*&#x200B;上从IP地址&#x200B;*&lt;IP地址>*&#x200B;创建的。

如果您这样做，您可以安全地忽略此电子邮件。

如果未执行此操作，请与`support@livefyre.com`联系

谢谢

*&quot;customer name&quot;*&#x200B;团队

*“用户名”、“客户名称”、“推荐URL”* 和“IP地址”均根据网站访客和您的网络动态生成。

## 向用户{#section_kjp_c3s_p1b}发送欢迎电子邮件

在用户注册帐户后，可以向用户发送欢迎电子邮件。 如果您设置了验证电子邮件，Studio会在发送验证电子邮件后发送此电子邮件。 发送欢迎电子邮件：

1. 在Studio中，单击齿轮图标可修改网络设置。
1. 单击 **[!UICONTROL Integration Settings > Livefyre Identity]**

1. 导航到&#x200B;**[!UICONTROL Email Settings]**。

1. 单击&#x200B;**[!UICONTROL Send Welcome Emails To New Users]**&#x200B;以启用发送电子邮件。
1. 导航到&#x200B;**[!UICONTROL Network Email]**&#x200B;以配置电子邮件&#x200B;*的*&#x200B;标志、要用作发件人地址的电子邮件地址（**电子邮件发件人**）以及要用于发件人电子邮件地址的显示名称（**电子邮件显示名称**）。
