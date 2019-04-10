---
description: 您可以创建从Facebook页面提取内容的流规则。
seo-description: 您可以创建从Facebook页面提取内容的流规则。
seo-title: Facebook页面规则
solution: Experience Manager
title: Facebook页面规则
uuid: 2be6346-1a92-409d-a22 f-e1 ec66 b6 dcc8
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# Facebook页面规则{#facebook-page-rules}

您可以创建从Facebook页面提取内容的流规则。

您可以使用Facebook页面规则从Facebook页面流式发布发布的内容。内容将以与SocialSync相同的频率引入App或Folder，后者会根据Facebook页面和帖子流量模式进行更改。还支持Facebook页面内的链接，并将显示在流中。

要创建Facebook页面规则以将内容从Facebook页面提取到应用程序或文件夹，您可以通过以下方式过滤：

* **[!UICONTROL Facebook Page]**

   * 输入页面 **[!UICONTROL Name]** 的名称。仅输入URL的结尾文本。**例如：** 要添加内容，请 `https://facebook.com/KellysSuperFunFanPage`在字段中键入 *KellysSuperfontPanPage***[!UICONTROL Name]** 。

   * 如果 **[!UICONTROL Include Facebook Comments for each post]** 希望将用户评论包含到页面帖子，请开启此选项。
   * 如果 **[!UICONTROL Only Show Author Posts]** 希望排除其他用户的帖子，请开启。

有关所有流规则的其他流规则选项，请参阅 [所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

>[!NOTE]
>
>Livefyre仅限于从Facebook收到的内容，因此无法保证Facebook页面上的每个帖子都包含在您的流中。

>[!NOTE]
>
>如果Facebook Page Regulation和Facebook页面规则均为特定Facebook页面启用，并且Facebook页面规则启用用户评论，则流规则将覆盖DetailSync。内容将仅根据Facebook页面特选规则而不是使用SearchSync流式传输到应用程序中。

Facebook页面特选支持的内容类型包括：

* 页面所有者或管理员

   * 状态
   * 照片
   * 视频作为链接

* Standard Facebook用户

   * 状态
   * 照片
   * 视频作为链接

* 第三方

   * 状态

