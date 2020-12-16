---
description: 您可以创建从YouTube规则中提取内容的流规则。
seo-description: 您可以创建从YouTube规则中提取内容的流规则。
seo-title: YouTube规则
solution: Experience Manager
title: YouTube规则
uuid: ec6a3780-7119-45c3-8ab2-fb0f9803d161
translation-type: tm+mt
source-git-commit: 30aa5cce5e7567208362cc35caeb7b7260c42f3b
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# YouTube规则{#youtube-rules}

您可以创建从YouTube规则中提取内容的流规则。

根据“用户”、“渠道”或“播放列表”创建YouTube规则。

要创建YouTube规则以将内容从YouTube拉入您的应用程序或文件夹，可以按以下方式进行筛选：

* **[!UICONTROL User]**
   * 输入&#x200B;**[!UICONTROL User]**&#x200B;的虚字符串，以在流中包含来自用户的视频。
   * 例如，如果要输入的用户源的URL为`https://www.youtube.com/user/livefyresupport`，只需输入`livefyresupport`。

* **[!UICONTROL Channel]**
   * 输入&#x200B;**[!UICONTROL Channel]**&#x200B;的虚字符串以包含来自流中渠道的视频。
   * 例如，如果要输入的渠道源的URL为`https://www.youtube.com/channel/UCeNZlh03MyUkjRlLFpVQxsg`，只需输入`UCeNZlh03MyUkjRlLFpVQxsg`。

* **[!UICONTROL Playlist]**
   * 输入&#x200B;**[!UICONTROL Playlist]**&#x200B;的虚字符串，以在流中包含来自播放列表的视频。
   * 例如，如果要输入的播放列表源的URL为`https://www.youtube.com/playlist?list=PLFE5670C92BDAC201`，只需输入`PLFE5670C92BDAC201`

* **[!UICONTROL Include recent items.]** 如果此设置为：
   * **[!UICONTROL Enabled]**, Livefyre会将源中的前15个内容项添加到流中，而不管发布日期如何。
   * **[!UICONTROL Disabled]**, Livefyre将源中的前15个内容项添加到流中，发布日期与流规则创建日期或更高日期相同。

有关所有流规则的其他流规则选项，请参阅[所有流规则的流规则选项](../../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
