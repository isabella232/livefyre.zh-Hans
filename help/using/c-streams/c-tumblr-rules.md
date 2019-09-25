---
description: 您可以创建从Tumblr中提取内容的流规则。
seo-description: 您可以创建从Tumblr中提取内容的流规则。
seo-title: 《Tumblr规则》
solution: Experience Manager
title: 《Tumblr规则》
uuid: fe9601ab-aa5e-48c6-a5bf-5543c179cb90
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 《Tumblr规则》{#tumblr-rules}

您可以创建从Tumblr中提取内容的流规则。

根据Tumblr博客创建Tumblr规则并按标记过滤。 Tumblr流每5分钟更新一次，从源中的前20个项目中查找Livefyre中不存在的内容。 Livefyre忽略源中前20个项目之外的所有内容。

要创建Tumblr规则以将内容从Tumblr拉入您的应用程序或文件夹，可以按以下方式进行筛选：

* **[!UICONTROL Blog]**

   * 输入 **[!UICONTROL Blog Name]** Tumblr博客的。 输入URL(*staff.tumblr.com*)或博客名称(*staff*)。

   * 最多包含一个， **[!UICONTROL Tag]** 可按包含给定标记的帖子过滤结果。

* **[!UICONTROL Include recent items.]** 如果此设置为：

   * **[!UICONTROL Enabled]**, Livefyre将源中的前20个内容项添加到流中，而不管发布日期如何。
   * **[!UICONTROL Disabled]**, Livefyre将源中的前20个内容项添加到流中，发布日期与流规则创建日期或更高版本相同。

有关所有流规则的其他流规则选项，请参 [阅所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
