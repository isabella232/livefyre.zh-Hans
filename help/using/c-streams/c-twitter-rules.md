---
description: 您可以创建从Twitter中提取内容的流规则。
seo-description: 您可以创建从Twitter中提取内容的流规则。
seo-title: Twitter规则
solution: Experience Manager
title: Twitter规则
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Twitter规则{#twitter-rules}

您可以创建从Twitter中提取内容的流规则。

根据主题标记、关键字、@mentions或作者创建Twitter规则。

为规 **[!UICONTROL Words]** 则添 **[!UICONTROL Username]** 加和添加将返回包含两个条目的内容。

>[!NOTE]
>
>Livefyre遵循Twitter显示指南，客户也有责任遵守这些指南。 有关详细信息，请参阅Twitter的显示要求 [文档](https://dev.twitter.com/terms/display-requirements)。

要创建Twitter规则以将内容从Twitter源拉入您的应用程序或文件夹，您可以按以下方式进行筛选：

* **[!UICONTROL Keywords]**
   * 输入 **[!UICONTROL Keywords]** 要包含在Twitter流中或从Twitter流中排除的内容。 为和字段指定 **[!UICONTROL Contains any of these words]** 值 **[!UICONTROL Does not contain any of these words]** 将返回包含第一个且不包含第二个的帖子。 可以为单个字段输入多个值，并将返回包含任意值的结果。 要使用Boolean运算符AND搜索包含两个或多个单词的帖子，请使用两个和号(*&amp;*)分隔这两个单词。
   * 例如，输入 **[!UICONTROL Contains any of these words]** Giants、Posey和 **[!UICONTROL Does not contain any of these words]** keyword Dodger将返回所有Tweets(包括单词 *Giants* 或Posey *)，但不包括Dodger***关键字)。
要搜索同时包含“巨人”和“ *波西* ”字样的 **“帖子”，请输入“巨人和波西”。 此功能仅支持Twitter规则中 **[!UICONTROL Contains any of these words]** 的 **[!UICONTROL Does not contain any of these words]** 和字段。

* **[!UICONTROL Hashtags]**.
   * 输入 **[!UICONTROL Hashtags]** 要包含在Twitter流中或从Twitter流中排除的内容。 为和字段指定值 **[!UICONTROL Contains any of these words]** 将返 **[!UICONTROL Does not contain any of these words]** 回“帖子”，其中第一个字段包含主题标记，第二个字段不包含主题标记。 您可以为一个字段输入多个值。 流返回包含任意值的结果。

* **[!UICONTROL Usernames]**
   * 输 **[!UICONTROL @mentions]** 入 **[!UICONTROL authors]** 或拉入流，或从流中排除。 使用复选框定义是否 **[!UICONTROL Retweets]** 也应 **[!UICONTROL replies]** 包括选定作者或来自选定作者。
   >[!NOTE]
   >
   >您可以包括或排除作者；您不能将这两个字段合并为单个Twitter规则。

* **[!UICONTROL Minimum number of followers.]** 选择用户必须从帖子中提取信息的关注者最少数量。
* **[!UICONTROL Location]**

   * 输入位置(城市、zipcode、地址或地理代码，格式为公用经纬度(+/- 90, +/- 180))。 开始键入位置以显示包含建议的下拉菜单。 从下拉菜单中选择一个位置。 地图会显示该位置的针脚。 调整滑块，为每个位置选择半径1英里至25英里。 如果不选择radius,Livefyre会自动选择默认的8英里。
   >[!NOTE]
   >
   >对于这两个字段，将从输入位置的中心计算距离。

   * 您可以添加多个位置和半径。 可以通过单击框中位置名称旁边的X来删除位置。
   * 合并 **[!UICONTROL Is near this location]** 和字 **[!UICONTROL Is not near this location]** 段，将内容拉入字段中的位置，但 **[!UICONTROL Is near this location]** 不是靠近字段中的位置 **[!UICONTROL Is not near this location]** 。


* **[!UICONTROL Additional Filters]**
   * 使用其他过滤器进一步优化您的Twitter规则。 定义您是否将：
      * 包含 **[!UICONTROL Replies]** 到目标帖子（如果流变为高速，则此功能将自动禁用。）
      * 包括来自 **[!UICONTROL Verified Twitter accounts only.]**
      * 包 **[!UICONTROL All Content]**&#x200B;括、 **[!UICONTROL Vines Only]**&#x200B;或 **[!UICONTROL Images Only.]**
      * 仅包括源自选定帐户( **[!UICONTROL Minimum number of followers]** any、100、500、1000、10,000或100,000)的帖子。

有关所有流规则的其他流规则选项，请参 [阅所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
