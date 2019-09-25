---
description: 您可以创建从YouTube规则中提取内容的流规则。
seo-description: 您可以创建从YouTube规则中提取内容的流规则。
seo-title: YouTube规则
solution: Experience Manager
title: YouTube规则
uuid: ec6a3780-7119-45c3-8ab2-fb0f9803d161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b

---


# YouTube规则 {#youtube-rules}

您可以创建从YouTube规则中提取内容的流规则。

根据用户、频道或播放列表创建YouTube规则。

要创建YouTube规则以将内容从YouTube拉入您的应用程序或文件夹，您可以按以下方式进行筛选：

* **[!UICONTROL User]**
   * 输入虚字符串，以 **[!UICONTROL User]** 便将来自用户的视频包含在流中。
   * 例如，如果要输入的用户源的URL是，只需 `https://www.youtube.com/user/livefyresupport`输入 `livefyresupport`。

* **[!UICONTROL Channel]**
   * 输入虚字符串，以 **[!UICONTROL Channel]** 便在流中包含来自渠道的视频。
   * 例如，如果您要输入的渠道源的URL是， `https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`只需输入 `UCeNZlh03MyUkjRlLFpVQxsg`。

* **[!UICONTROL Playlist]**
   * 输入虚字符串，以便 **[!UICONTROL Playlist]** 在流中包含来自播放列表的视频。
   * 例如，如果要输入的播放列表源的URL是， `https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`只需输入 `PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** 如果此设置为：
   * **[!UICONTROL Enabled]**, Livefyre将源中的前15个内容项添加到流中，而不管发布日期如何。
   * **[!UICONTROL Disabled]**, Livefyre将源中的前15个内容项添加到流中，发布日期与流规则创建日期或更高版本相同。

有关所有流规则的其他流规则选项，请参 [阅所有流规则的流规则选项](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
