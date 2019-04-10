---
description: 这些选项适用于所有社交网络或发布方法中的任何流规则。
seo-description: 这些选项适用于所有社交网络或发布方法中的任何流规则。
seo-title: 所有流规则的流规则选项
solution: Experience Manager
title: 所有流规则的流规则选项
uuid: 4072ee83-31e7-918c-134b8b8032e1
translation-type: tm+mt
source-git-commit: 566ea2587f101202045488e9f4edf73ece100293

---


# 所有流规则的流规则选项{#stream-rule-options-for-all-stream-rules}

这些选项适用于所有社交网络或发布方法中的任何流规则。

文本和关键字字段的搜索功能：

* 输入关键字时，Livefyre会自动使用Boolean运算符 **或** 单个单词时的值。例如，要用 *饼图* 或 *菜谱*搜索帖子，输入 *蛋糕*，然后在字段中输入 *菜谱***[!UICONTROL keyword]** 。

* 您可以通过引号准确地围绕词组搜索准确短语。例如，要搜索精确短语 *饼图，*请在字段中输入 *“蛋糕菜谱”***[!UICONTROL keyword]** 。

* 您可以在一个流规则中组合Boolean和准确短语搜索。例如，您可以逐个输入每个短语，搜索 *蛋糕*、 *食谱*和 *“蛋糕菜谱”* 。

**[!UICONTROL Additional Filters]**:

* **[!UICONTROL Media]**. 选择下列选项之一：

   * **[!UICONTROL All Content.]** 允许任何内容。
   * **[!UICONTROL Media Required.]** 只允许包含图像和视频的内容。(对于Instagram和Facebook内容，您可以指定 **[!UICONTROL Photos]** 或 **[!UICONTROL Videos]** 仅指定)。

* **[!UICONTROL Language]**. 选择要搜索的语言。英语是默认语言。
* **[!UICONTROL Smart Tags]**. 选择用于标识内容的标记。Livefyre使用计算机透视技术识别照片和视频，使用特定智能标签来更精确地搜索。使用 **[!UICONTROL ANY]** 修饰符将内容过滤到流中，使用任何标记或 **[!UICONTROL ALL]** 修饰符将内容过滤到使用所有标记的流中。使用该 **[!UICONTROL Image contains none of these smart tags]** 字段可为包含您不希望在流中的内容的照片输入标记。此选项不适用于文本内容。

* **[!UICONTROL Products]**. 添加产品标签，以使流规则与产品目录中的产品相匹配。
* **[!UICONTROL Premoderate]**. 选择下列选项之一：

   * **[!UICONTROL On]**. 审核所有传入的规则内容。您可以从ModQ的“流”部分查看预先审核的内容。**[!UICONTROL On]** 覆盖应用程序设置中的设置。
   * **[!UICONTROL Off]**. 请勿审核任何传入的规则内容。**[!UICONTROL Off]** 覆盖应用程序设置中的设置。
   * **[!UICONTROL Inherited (Off)]**. 使用站点(下 **[!UICONTROL Site Settings]**)中的中等设置。

* **[!UICONTROL SAFE Rules]**. 选择下列选项之一：
   * **[!UICONTROL Apply SAFE Rules]**. 将所有安全规则应用于此流。
   * **[!UICONTROL Apply SAFE Rules for:]** 选择一个或多个选项以应用此流规则的安全规则。
   * **[!UICONTROL Disable SAFE Rules]**. 请勿对此流应用任何安全规则。

有关特定于社交网络或内容类型的流规则选项，请参阅以下社交网络或内容类型的相关文档：

* [Facebook页面](../c-streams/c-facebook-page-rules.md#c_facebook_page_rules)
* [电子邮件](../c-streams/c-email-rules.md#c_email_rules)
* [Instagram](../c-streams/c-instagram-rules.md#c_instagram_rules)
* [Tumblr](../c-streams/c-tumblr-rules.md#c_tumblr_rules)
* [Twitter](../c-streams/c-twitter-rules.md#c_twitter_rules)
* [YouTube](../c-streams/c-youtube-rules/c-youtube-rules.md#c_youtube_rules)
* [RSS](../c-streams/c-rss-rules-streams.md#c_rss_rules_streams)
