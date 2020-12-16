---
description: 定义Instagram和Twitter帖子的请求权限设置。
seo-description: 定义Instagram和Twitter帖子的请求权限设置。
seo-title: 设置Rights Management
solution: Experience Manager
title: 设置Rights Management
uuid: 3ffcbc95-484f-4eba-b817-658c1d658bf8
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---


# 设置Rights Management{#set-up-rights-management}

定义Instagram和Twitter帖子的请求权限设置。

在定义“权限请求设置”之前，必须为Instagram或Twitter配置一个或多个社交帐户。 有关如何配置社交帐户的详细信息，请参阅[添加社交帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/t-configure-social-accout-instagram.md#t_configure_social_accout_instagram)。

>[!NOTE]
>
>您只能在网络级别配置权限管理。 无法配置站点特定的权限管理。

1. 在Livefyre Studio中，导航到&#x200B;**[!UICONTROL Network]** **[!UICONTROL Settings > Rights Management]**。

   >[!NOTE]
   >
   >要设置Rights Management帐户，您需要审查方或管理员网络级别权限。

1. 如果未设置任何Rights Management帐户，请选择&#x200B;**[!UICONTROL +Add New Account]**。
1. 单击要用于Rights Management的社交网络下的&#x200B;**[!UICONTROL Create New Setting]**。

   >[!NOTE]
   >
   >对于Instagram帐户，您必须拥有Instagram商业帐户才能通过部分自动化申请权限。 有关不同类型的Instagram帐户以及如何使用它们的详细信息，请参阅[关于Instagram帐户](../c-users-creating-accounts-with-studio-access/t-configure-social-accout-instagram/c-about-instagram-accounts.md#c_about_instagram_accounts)。

1. 填写显示的字段。 所有字段均为必填。

   * **[!UICONTROL Display name:]** 输入显示名称以标识要用于您的权限请求帐户的Twitter或Instagram帐户。此名称仅限内部。
   * **[!UICONTROL Enabled:]**默认设置为on。 启用帐户的权限管理。
   * **[!UICONTROL Approval hashtag:]** 内容所有者将用来指示他们同意使用其内容的主题标签。
   * **[!UICONTROL Terms and conditions:]** 指向网络条款和条件以重复使用内容的链接。此字段区分大小写。
   * **[!UICONTROL Network and sites:]** 此帐户可请求其内容重用权限的网络或站点。要使此帐户在整个网络中可用，请选择列表中的第一个项目，或使用Command/CTRL键限制到特定站点。
   * **[!UICONTROL Default message:]** 随“权限请求”一起显示的消息。您可以在请求权限时覆盖此消息。

      * 当审查方向内容作者发出请求时，Livefyre会向审查方显示默认消息之一。 版主可以生成其他默认消息，或在发送前编辑该消息。 邮件必须包括作者的Twitter或Instagram句柄({handle})、您的批准主题标签({grantTag})以及指向条款和条件的链接({termsLink})。

         **[!UICONTROL Note:]** {handle}、{grantTag}和{termsLink}均区分大小写。

         **[!UICONTROL Note:]** 为防止恶意使用，Twitter会用t.coformatting包装所 [有包含](https://t.co/) 的URL。为防止默认消息超过140个字符，Livefyre建议不要在默认消息中包含URL。

      * 编写权限请求消息的最佳实践：

         * 创建多条默认消息，使您听起来不像机器人。 在创建下一个默认消息之前保存每个默认消息。
         * 鼓励版主在发送前个性化此备注，以防网络请求被标记为垃圾邮件。

1. 单击&#x200B;**[!UICONTROL Save Settings]**以添加您的Rights Request帐户。
从资产库发送权限请求。 有关如何从资产库发送权限请求的详细信息，请参阅[发送权限请求](../c-how-requesting-rights-works/t-send-a-rights-request-to-own-a-digital-asset.md#t_send_a_rights_request_to_own_a_digital_asset)。