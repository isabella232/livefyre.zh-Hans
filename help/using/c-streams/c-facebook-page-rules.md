---
description: 您可以创建从Facebook页面提取内容的流规则。
seo-description: 您可以创建从Facebook页面提取内容的流规则。
seo-title: Facebook页面规则
solution: Experience Manager
title: Facebook页面规则
uuid: 2be63476-1a92-409d-a22f-e1ec66b6dcc8
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# Facebook页面规则{#facebook-page-rules}

您可以创建从Facebook页面提取内容的流规则。

您可以使用Facebook页面规则从Facebook页面流式传送公开发布的内容。 内容将以与SocialSync相同的频率被拉入应用程序或文件夹，SocialSync会根据Facebook页面和帖子流量模式进行更改。 还支持Facebook页面内的链接，并将显示在流中。

要创建Facebook页面规则以将内容从Facebook页面拉入您的应用程序或文件夹，您可以按以下方式进行筛选：

* **[!UICONTROL Facebook Page]**

   * 输入页 **[!UICONTROL Name]** 面对应的。 仅输入URL的尾随文本。 **** 例如：要从添加内 `https://facebook.com/KellysSuperFunFanPage`容，请在字 *段中键入KellysSuperFunFan* Page **[!UICONTROL Name]** 。

   * 如果 **[!UICONTROL Include Facebook Comments for each post]** 您希望将用户评论包含到页面帖子，请打开。
   * 如果 **[!UICONTROL Only Show Author Posts]** 您希望从其他用户中排除帖子，请打开。

有关所有流规则的其他流规则选项，请参 [阅所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

>[!NOTE]
>
>Livefyre仅限于从Facebook收到的内容，因此无法保证Facebook页面上的每个帖子都包含在您的流中。

>[!NOTE]
>
>如果为特定Facebook页面启用了Facebook SocialSync和Facebook页面规则，并且为Facebook页面规则启用了用户评论，则流规则将覆盖SocialSync。 内容将仅根据Facebook页面特定规则（而不是使用SocialSync）流式传输到应用程序中。

Facebook页面特选支持的内容类型包括：

* 页面所有者或管理员

   * 状态
   * 照片
   * 视频作为链接

* 标准Facebook用户

   * 状态
   * 照片
   * 视频作为链接

* 第三方

   * 状态

