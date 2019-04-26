---
description: 您可以创建从Twitter提取内容的流规则。
seo-description: 您可以创建从Twitter提取内容的流规则。
seo-title: Twitter规则
solution: Experience Manager
title: Twitter规则
uuid: a7fd2398-fd6 b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# Twitter规则{#twitter-rules}

您可以创建从Twitter提取内容的流规则。

根据主题标签、关键字、@提及或作者创建Twitter规则。

添加 **[!UICONTROL Words]** 和 **[!UICONTROL Username]** 用于规则将返回包含两个条目的内容。

>[!NOTE]
>
>Livefyre遵守Twitter显示准则，客户也负责遵守这些准则。有关更多信息，请参阅Twitter有关其 [“显示要求](https://dev.twitter.com/terms/display-requirements)”的文档。

要创建Twitter规则以将内容从Twitter源提取到应用程序或文件夹，可以通过以下方式过滤：

* **[!UICONTROL Keywords]**
   * 输入或 **[!UICONTROL Keywords]** 排除在Twitter流中。指定 **[!UICONTROL Contains any of these words]** 和 **[!UICONTROL Does not contain any of these words]** 字段的值将返回包含第一个值且不包含第二个值的帖子。可以输入单个字段的多个值，并将返回包含任何值的结果。要使用Boolean操作符，并在其中用两个或更多单词搜索帖子，请使用两个或多个*要*分隔两个词的字母。
   * 例如，输入 **[!UICONTROL Contains any of these words]** 关键字Gions、Posey和 **[!UICONTROL Does not contain any of these words]** Dodger将返回包含单词 *Giant* 或 *Posey* 的所有帖子，且不包含Dodger单词 **。
要搜索包含 *Ginants* 和 *Posey*字样的帖子，请输入“Giants&& Posey”。此功能仅对Twitter规则中 **[!UICONTROL Contains any of these words]** 的和 **[!UICONTROL Does not contain any of these words]** 字段受支持。

* **[!UICONTROL Hashtags]**.
   * 输入或 **[!UICONTROL Hashtags]** 排除在Twitter流中。指定 **[!UICONTROL Contains any of these words]** 和 **[!UICONTROL Does not contain any of these words]** 字段的值将返回在第一个字段中包含hashtags的帖子，并且不包含第二个字段中的哈希标记。可为单个字段输入多个值。流返回包含任何值的结果。

* **[!UICONTROL Usernames]**
   * 输入 **[!UICONTROL @mentions]** 或 **[!UICONTROL authors]** 拖入流或从流中排除。使用复选框定义 **[!UICONTROL Retweets]** 是否 **[!UICONTROL replies]** 还应包含选定作者。
   >[!NOTE]
   >
   >您可以包括或排除作者；您不能将这两个字段合并为一个Twitter规则。

* **[!UICONTROL Minimum number of followers.]** 选择用户必须从帖子中提取信息的最少关注者数量。
* **[!UICONTROL Location]**

   * 输入位置(城市、zipcode、address或geocode，采用通用纬度/longitude格式(+/-90，+/-180))。开始键入位置以显示带有建议的下拉菜单。从下拉菜单中选择一个位置。地图会显示该位置的固定位置。调整滑块，为每个位置选择一英里到25英里的半径。如果您不选择半径，Livefyre将自动选择默认的8英里。
   >[!NOTE]
   >
   >对于这两个字段，距离将从输入位置的中心计算距离。

   * 您可以添加多个位置和半径。您可以通过单击框中某个位置的名称旁边的X来删除位置。
   * 组合和 **[!UICONTROL Is near this location]****[!UICONTROL Is not near this location]** 字段可将内容提取到 **[!UICONTROL Is near this location]** 字段中的位置，但不在 **[!UICONTROL Is not near this location]** 字段中的位置附近提取内容。


* **[!UICONTROL Additional Filters]**
   * 使用其他过滤器进一步优化您的Twitter规则。定义您是否将：
      * 包括 **[!UICONTROL Replies]** 目标帖子(如果流变得高速，此功能将自动禁用)。
      * 包括来自 **[!UICONTROL Verified Twitter accounts only.]**
      * 包括 **[!UICONTROL All Content]**、 **[!UICONTROL Vines Only]**或 **[!UICONTROL Images Only.]**
      * 仅包含源自包含选定 **[!UICONTROL Minimum number of followers]** 帐户的帐户(任何、100、500、1000、10000或100,000)的帖子。

有关所有流规则的其他流规则选项，请参阅 [所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
