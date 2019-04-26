---
description: 定义请求Instagram和Twitter帖子权限的设置。
seo-description: 定义请求Instagram和Twitter帖子权限的设置。
seo-title: 设置Rights Management
solution: Experience Manager
title: 设置Rights Management
uuid: 3ffcbc95-484f-4eba-b817-658c1 d658 bf8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# 设置Rights Management{#set-up-rights-management}

定义请求Instagram和Twitter帖子权限的设置。

在定义Rights Request Settings之前，必须为Instagram或Twitter配置一个或多个社交帐户。有关如何配置社交帐户的详细信息，请参阅 [添加社交帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram)。

>[!NOTE]
>
>您只能在网络级别配置权限管理。您无法配置站点特定的权限管理。

1. 在Livefyre Studio中，导航到 **[!UICONTROL Network]****[!UICONTROL Settings > Rights Management]**。

   >[!NOTE]
   >
   >要设置Rights Management帐户，您需要审核者或管理员网络级别权限。

1. 选择 **[!UICONTROL +Add New Account]** 是否未设置任何Rights Management帐户。
1. 在 **[!UICONTROL Create New Setting]** 要用于Rights Management的社交网络下单击。

   >[!NOTE]
   >
   >对于Instagram帐户，您必须拥有Instagram业务帐户才能请求部分自动化。有关不同类型Instagram帐户以及如何使用这些帐户的详细信息，请参阅 [关于Instagram帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

1. 填写显示的字段。所有字段都是必填字段。

   * **[!UICONTROL Display name:]** 输入显示名称以标识用于Rights Request帐户的Twitter或Instagram帐户。此名称仅为内部名称。
   * ****[!UICONTROL Enabled:]默认设置为开启。为帐户启用权限管理。
   * **[!UICONTROL Approval hashtag:]** 内容所有者用来表示他们同意使用其内容的哈希标记。
   * **[!UICONTROL Terms and conditions:]** 网络条款和条件的链接，用于重复使用内容。此字段区分大小写。
   * **[!UICONTROL Network and sites:]** 此帐户可请求内容重用权限的网络或站点。要使此帐户在整个网络中可用，请选择列表中的第一个项目，或使用Command/CTRL键限制特定站点。
   * **[!UICONTROL Default message:]** 显示您的权限请求的消息。您可以在请求权限时重写此消息。

      * 当审核者向内容作者发出请求时，Livefyre将向审核者展示默认消息之一。审核者可以在发送之前生成其他默认消息或编辑消息。邮件必须包括作者的Twitter或Instagram句柄({handle})、您的批准标记({GrantTag})以及指向条款和条件的链接({termsLink})。

         **[!UICONTROL Note:]** {handle}、{GrantTag}和{termsLink}都区分大小写。

         **[!UICONTROL Note:]** 为了防止恶意使用，Twitter会用 [t. common](https://t.co/) 格式包裹任何包含的URL。为了防止您的默认消息超过140个字符，Livefyre建议不要在默认消息中包含URL。

      * 编写权限请求消息的最佳做法：

         * 创建多个默认消息，使您不像机器人一样。在创建下一个默认消息之前保存每个默认消息。
         * 鼓励审核者在发送前个性化本备注，以防止您的网络请求被标记为垃圾邮件。

1. 单击 **[!UICONTROL Save Settings]** 以添加您的Rights Request帐户。
从资产库发送权限请求。有关如何从资产库发送权限请求的更多信息，请参阅 [发送权限请求](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset) 。