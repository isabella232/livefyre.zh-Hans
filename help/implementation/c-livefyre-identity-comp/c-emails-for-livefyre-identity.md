---
description: 'null'
seo-description: 'null'
seo-title: Livefyre Identity电子邮件
solution: Experience Manager
title: Livefyre Identity电子邮件
uuid: e807803-687e-4df0-94d1-b18 a48 d024 e8
translation-type: tm+mt
source-git-commit: 74a63daa264014af9a8afb6639fa1561a7b83241

---


# Livefyre Identity电子邮件{#emails-for-livefyre-identity}

Livefyre Identity发送下列电子邮件：

* [密码重置电子邮件](#c_emails_for_livefyre_identity/section_nd1_whs_p1b)
* [验证电子邮件](#c_emails_for_livefyre_identity/section_ak5_xhs_p1b)
   * [为用户发送电子邮件验证](#c_emails_for_livefyre_identity/section_vyv_yhs_p1b)

* [欢迎电子邮件](#c_emails_for_livefyre_identity/section_z2v_zhs_p1b)
   * [向用户发送欢迎电子邮件](#c_emails_for_livefyre_identity/section_kjp_c3s_p1b)

您可以自定义所有Livefyre身份电子邮件的外观 **[!UICONTROL Integration Settings > Email Notifications.]**

## 密码重置电子邮件 {#section_nd1_whs_p1b}

当用户尝试重置口令时，Livefyre会自动发送密码重置电子邮件。

密码重置电子邮件如下所示：

**主题：** 重置口令

**正文：**

嘿，&lt; *username&gt;*，

有一个请求在&lt;网络名称&gt;上 *更改配置文件的口令*。

如果您请求了此操作，请单击下面的链接以选择新密码： *&lt;密码重置URL&gt;*。

*&lt; Username&gt;*、 *&lt; network name&gt;*和 *&lt;密码重置URL&gt;* 均根据站点访问者和网络动态生成。

## 验证电子邮件 {#section_ak5_xhs_p1b}

您可以发送电子邮件，确认用户的电子邮件地址。要发送验证电子邮件，您必须在 **集成设置&gt; Livefyre Identity中打开该选项**。

验证电子邮件如下所示：

**主题：** 电子邮件验证

**正文：**

&lt; *username&gt;*，

请单击以下链接(或在浏览器中粘贴)以验证您的帐户： *&lt;验证URL&gt;*。

此链接将在24小时后过期。

谢谢，

*&lt;客户姓名&gt;* 团队

*&lt; Username&gt;*、 *&lt; network name&gt;*和 *&lt;验证URL&gt;* 均根据站点访问者和网络动态生成。

## 向用户发送电子邮件验证 {#section_vyv_yhs_p1b}

您可以向用户发送电子邮件，以验证他们用来注册帐户的电子邮件地址。发送验证电子邮件：

1. 在Studio中，单击齿轮图标以修改网络设置。
1. 单击 **“集成设置”&gt;“Livefyre Identity”。**

1. 导航到 **登录类型**。
1. 单击 **“要求电子邮件验证”** 以向用户发送电子邮件，验证他们用于注册帐户的电子邮件地址。
1. 导航 **到网络电子邮件** 以配置电子邮件 **的标志**、电子邮件地址用作地址(**电子邮件发件人**)和显示名称(用于电子邮件地址(**电子邮件显示名称**))。

## 欢迎电子邮件 {#section_z2v_zhs_p1b}

您可以向用户发送欢迎电子邮件。要发送欢迎电子邮件，您必须在 **“集成设置** ”&gt; **“Livefyre Identity**”中打开该选项。

欢迎电子邮件如下所示：

**主题：** 欢迎使用 *&lt;客户姓名&gt;*

**正文：**

&lt; *username&gt;*，

为您创建了一个帐户 *，&lt;客户名称&gt;*。

此帐户是在 *&lt;引用URL&gt;* 从IP地址 *&lt; IP地址&gt;创建*的。

如果您这样做，您可以安全地忽略此电子邮件。

如果您没有这样做，请联系 `support@livefyre.com`

感谢致谢

“ *客户姓名”* 团队

*“用户名”、“客户名称”、“引用URL”* 和“IP地址”均根据网站访问者和网络动态生成。

## 向用户发送欢迎电子邮件 {#section_kjp_c3s_p1b}

在注册帐户后，您可以向用户发送欢迎电子邮件。如果您设置验证电子邮件，Studio会在发送验证电子邮件后发送此电子邮件。发送欢迎电子邮件：

1. 在Studio中，单击齿轮图标以修改网络设置。
1. 单击 **[!UICONTROL Integration Settings > Livefyre Identity]**

1. 导航 **[!UICONTROL Email Settings]**到。

1. 单击 **[!UICONTROL Send Welcome Emails To New Users]** 以启用发送电子邮件。
1. 导航到 **[!UICONTROL Network Email]** 配置电子邮件 *的徽标*、电子邮件地址用作地址(**电子邮件发件人**)和显示名称(用于电子邮件地址(**电子邮件显示名称**))。
