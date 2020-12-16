---
description: 这些选项适用于来自所有社交网络或发布方法的任何流规则。
seo-description: 这些选项适用于来自所有社交网络或发布方法的任何流规则。
seo-title: 所有流规则的流规则选项
solution: Experience Manager
title: 所有流规则的流规则选项
uuid: 4072ee83-31e7-4de6-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 8bdb537b38d78dba033d6671b710c2a61934d6b2
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 5%

---


# 所有流规则的流规则选项{#stream-rule-options-for-all-stream-rules}

这些选项适用于来自所有社交网络或发布方法的任何流规则。

文本和关键字字段的搜索功能：

* 输入关键字时，Livefyre在输入单个单词时会自动使用布尔运算符&#x200B;**OR**。 例如，要搜索包含单词&#x200B;*cake*&#x200B;或&#x200B;*recipe*&#x200B;的帖子，请输入&#x200B;*cake*，然后在&#x200B;**[!UICONTROL keyword]**&#x200B;字段中输入&#x200B;*recipe*。

* 您可以在引号中围绕精确的短语文本来搜索精确的短语。 例如，要搜索精确短语&#x200B;*蛋糕菜谱*，请在&#x200B;**[!UICONTROL keyword]**&#x200B;字段中输入&#x200B;*&quot;蛋糕菜谱&quot;*。

* 您可以将布尔词组搜索和精确词组搜索合并到一个流规则中。 例如，可通过一次输入每个短语来搜索&#x200B;*蛋糕*、*菜谱*&#x200B;和&#x200B;*&quot;蛋糕菜谱&quot;*。

**[!UICONTROL Additional Filters]**：

* **[!UICONTROL Media]**。选择下列选项之一：

   * **[!UICONTROL All Content.]** 允许任何内容。
   * **[!UICONTROL Media Required.]** 仅允许包含图像和视频的内容。（对于Instagram和Facebook内容，只能指定&#x200B;**[!UICONTROL Photos]**&#x200B;或&#x200B;**[!UICONTROL Videos]**）。

* **[!UICONTROL Language]**。选择要搜索的语言。 英语是默认语言。
* **[!UICONTROL Smart Tags]**。选择用于标识内容的标记。 Livefyre使用计算机视觉技术识别带有特定智能标签的照片和视频，使搜索更精确。 使用&#x200B;**[!UICONTROL ANY]**&#x200B;修饰符可使用任何标记将内容筛选到流中，或使用&#x200B;**[!UICONTROL ALL]**&#x200B;修饰符将内容筛选到使用所有标记的流中。 使用&#x200B;**[!UICONTROL Image contains none of these smart tags]**&#x200B;字段为包含您不希望在流中包含的内容的照片输入标记。 此选项不适用于文本内容。

* **[!UICONTROL Products]**。添加产品标记以将流规则与产品目录中的产品相匹配。
* **[!UICONTROL Premoderate]**。选择下列选项之一：

   * **[!UICONTROL On]**。预审所有传入规则内容。 您可以从ModQ的“流”部分视图预审核的内容。 **[!UICONTROL On]** 将覆盖“应用程序设置”中的设置。
   * **[!UICONTROL Off]**。请勿预审任何传入规则内容。 **[!UICONTROL Off]** 将覆盖“应用程序设置”中的设置。
   * **[!UICONTROL Inherited (Off)]**。使用站点（**[!UICONTROL Site Settings]**&#x200B;下）中的预审核设置。

* **[!UICONTROL SAFE Rules]**。选择下列选项之一：
   * **[!UICONTROL Apply SAFE Rules]**。将所有SAFE Rules应用于此流。
   * **[!UICONTROL Apply SAFE Rules for:]** 选择一个或多个选项，以对此流规则应用安全规则。
   * **[!UICONTROL Disable SAFE Rules]**。请勿对此流应用任何安全规则。

有关特定于社交网络或内容类型的流规则选项，请参阅相应社交网络或内容类型的以下文档：

* [Facebook 页面](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [电子邮件](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
