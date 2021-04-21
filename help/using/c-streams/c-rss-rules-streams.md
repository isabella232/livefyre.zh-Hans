---
description: 您可以创建从RSS源中提取内容的流规则。
title: RSS规则
exl-id: bfb3bbad-ab26-451e-b540-d6c41f54dc31
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# RSS规则{#rss-rules}

您可以创建从RSS源中提取内容的流规则。

RSS流每5分钟更新一次，从源中的前50个项目中查找Livefyre中不存在的内容。 Livefyre忽略了源中前50项之外的所有内容。

要创建RSS规则，将RSS源中的内容拉入您的应用程序或文件夹，您可以按以下方式进行筛选：

* **[!UICONTROL URL]** RSS源。
* **[!UICONTROL Include recent items.]** 如果此设置为：

   * **[!UICONTROL Enabled]**, Livefyre会将源中的前50个内容项添加到流中，而不管发布日期如何。
   * **[!UICONTROL Disabled]**, Livefyre将源中的前50个内容项添加到流中，发布日期与流规则创建日期或更高日期相同。

* **[!UICONTROL Extract post information from item link (when disabled, post information is extracted from XML).]** 从项目链接或XML中提取信息。

**RSS规则**

Livefyre基于以下RSS规范解析RSS服务：

* [RSS 2.0](https://en.wikipedia.org/wiki/RSS)
* [媒体RSS](https://en.wikipedia.org/wiki/Media_RSS)
* [原子馈送](https://validator.w3.org/feed/docs/atom.html)

Livefyre不会读取不符合这些规范的源，并且其内容不会被拉入您的流中。 使用WC3源验证服务检查RSS源的语法，并确保其有效。

有关所有流规则的其他流规则选项，请参阅[所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
