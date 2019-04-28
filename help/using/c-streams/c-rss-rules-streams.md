---
description: 您可以创建从RSS源提取内容的流规则。
seo-description: 您可以创建从RSS源提取内容的流规则。
seo-title: RSS规则
solution: Experience Manager
title: RSS规则
uuid: 3c9e2069-bb85-41dc-8b35-6237642a538 a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# RSS规则{#rss-rules}

您可以创建从RSS源提取内容的流规则。

RSS流每分钟更新一次，在Livefyre中的前50个项目中查找的内容会在源中的前50个项目中查找。Livefyre忽略了源中前50个项目中的所有内容。

要创建RSS规则以将内容从RSS源提取到App或Folder，您可以通过以下方式过滤：

* **[!UICONTROL URL]** RSS Feed。
* **[!UICONTROL Include recent items.]** 如果设置为：

   * **[!UICONTROL Enabled]** Livefyre将您的源中的前50个内容项目添加到流中，无论发布日期如何。
   * **[!UICONTROL Disabled]** Livefyre将您的源中的前50个内容项目添加到流中，发布日期与流规则创建日期或更高版本相同。

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** 从项目链接或XML中提取信息。

**RSS规则**

Livefyre根据以下RSS规范解析RSS源：

* [RSS2.0](https://en.wikipedia.org/wiki/RSS)
* [媒体RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [Atom feed](https://validator.w3.org/feed/docs/atom.html)

Livefyre不读取不符合这些规范的源，他们的内容将不会被引入您的流中。使用WC Feed验证服务检查RSS源的语法，并确保它有效。

有关所有流规则的其他流规则选项，请参阅 [所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
