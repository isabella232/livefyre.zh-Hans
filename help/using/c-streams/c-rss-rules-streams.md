---
description: 您可以创建从RSS源中提取内容的流规则。
seo-description: 您可以创建从RSS源中提取内容的流规则。
seo-title: RSS规则
solution: Experience Manager
title: RSS规则
uuid: 3c9e2069-bb85-41dc-8b35-6237642a538a
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# RSS规则{#rss-rules}

您可以创建从RSS源中提取内容的流规则。

RSS流每5分钟更新一次，从源中的前50个项目中查找Livefyre中不存在的内容。 Livefyre忽略源中前50个项目之外的所有内容。

要创建RSS规则以将内容从RSS源拉入您的应用程序或文件夹，您可以按以下方式进行筛选：

* **[!UICONTROL URL]** RSS源。
* **[!UICONTROL Include recent items.]** 如果此设置为：

   * **[!UICONTROL Enabled]**, Livefyre将源中的前50个内容项添加到流中，而不管发布日期如何。
   * **[!UICONTROL Disabled]**, Livefyre将源中的前50个内容项添加到流中，发布日期与流规则创建日期或更高版本相同。

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** 从项目链接或XML中提取信息。

**RSS规则**

Livefyre基于以下RSS规范解析RSS服务：

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [媒体RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [原子源](https://validator.w3.org/feed/docs/atom.html)

Livefyre不会读取不符合这些规范的源，并且它们的内容不会被拉入您的流中。 使用WC3 Feed Validation service检查RSS源的语法，并确保它有效。

有关所有流规则的其他流规则选项，请参 [阅所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
