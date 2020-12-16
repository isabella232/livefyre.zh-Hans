---
description: 您可以创建从Twitter中提取内容的流规则。
seo-description: 您可以创建从Twitter中提取内容的流规则。
seo-title: Twitter规则
solution: Experience Manager
title: Twitter规则
uuid: a7fd2398-fd6b-4c24-92b2-7471176d7648
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---


# Twitter规则{#twitter-rules}

您可以创建从Twitter中提取内容的流规则。

根据主题标记、关键字、@mentions或作者创建Twitter规则。

为规则添加&#x200B;**[!UICONTROL Words]**&#x200B;和&#x200B;**[!UICONTROL Username]**&#x200B;将返回包含这两个条目的内容。

>[!NOTE]
>
>Livefyre遵循Twitter显示指南，客户也有责任遵守这些指南。 有关详细信息，请参阅Twitter的[显示要求](https://dev.twitter.com/terms/display-requirements)文档。

要创建Twitter规则以将内容从Twitter源拉入您的应用程序或文件夹，您可以按以下方式进行筛选：

* **[!UICONTROL Keywords]**
   * 输入要包含在Twitter流中或从Twitter流中排除的&#x200B;**[!UICONTROL Keywords]**。 为&#x200B;**[!UICONTROL Contains any of these words]**&#x200B;和&#x200B;**[!UICONTROL Does not contain any of these words]**&#x200B;字段指定值将返回包含第一个字段且不包含第二个字段的帖子。 可以为单个字段输入多个值，并返回包含任意值的结果。 要使用布尔运算符AND搜索包含两个或多个单词的帖子，请使用两个和号(*&amp;&amp;*)分隔这两个单词。
   * 例如，输入&#x200B;**[!UICONTROL Contains any of these words]**&#x200B;关键字Giants、Posey和&#x200B;**[!UICONTROL Does not contain any of these words]**&#x200B;关键字Dodger将返回包含单词&#x200B;*Giants*&#x200B;或&#x200B;*Posey*&#x200B;的所有帖子，且不包含单词&#x200B;*Dodger*。
要搜索同时包含单词*Giants*&#x200B;和&#x200B;*Posey*&#x200B;的帖子，请输入“Giants &amp;&amp; Posey”。 此功能仅支持Twitter规则中的&#x200B;**[!UICONTROL Contains any of these words]**&#x200B;和&#x200B;**[!UICONTROL Does not contain any of these words]**&#x200B;字段。

* **[!UICONTROL Hashtags]**。
   * 输入要包含在Twitter流中或从Twitter流中排除的&#x200B;**[!UICONTROL Hashtags]**。 为&#x200B;**[!UICONTROL Contains any of these words]**&#x200B;和&#x200B;**[!UICONTROL Does not contain any of these words]**&#x200B;字段指定值将返回在第一个字段中包含哈希标记的帖子，在第二个字段中不包含哈希标记。 您可以为单个字段输入多个值。 流返回包含任意值的结果。

* **[!UICONTROL Usernames]**
   * 输入&#x200B;**[!UICONTROL @mentions]**&#x200B;或&#x200B;**[!UICONTROL authors]**&#x200B;以拉入流，或从流中排除。 使用复选框定义是否还应包括所选作者的&#x200B;**[!UICONTROL Retweets]**&#x200B;或&#x200B;**[!UICONTROL replies]**。

   >[!NOTE]
   >
   >您可以包括或排除作者；您不能将这两个字段合并为单个Twitter规则。

* **[!UICONTROL Minimum number of followers.]** 选择用户必须从其帖子中提取信息的最低关注者数量。
* **[!UICONTROL Location]**

   * 输入位置(城市、zipcode、地址或地理代码，格式为公用经纬度(+/- 90, +/- 180))。 开始键入位置以显示包含建议的下拉菜单。 从下拉列表中选择一个位置。 地图显示该位置的针脚。 调整滑块，为每个位置选择半径1英里至25英里。 如果您不选择半径，Livefyre会自动选择默认的8英里。
   >[!NOTE]
   >
   >对于这两个字段，将从输入位置的中心计算距离。

   * 您可以添加多个位置和半径。 可通过单击框中位置名称旁边的X来删除位置。
   * 合并&#x200B;**[!UICONTROL Is near this location]**&#x200B;和&#x200B;**[!UICONTROL Is not near this location]**&#x200B;字段，将内容拉入&#x200B;**[!UICONTROL Is near this location]**&#x200B;字段中的位置，但不拉入&#x200B;**[!UICONTROL Is not near this location]**&#x200B;字段中的位置。


* **[!UICONTROL Additional Filters]**
   * 使用其他过滤器进一步细化您的Twitter规则。 定义您是否将：
      * 将&#x200B;**[!UICONTROL Replies]**&#x200B;包含到目标帖子（如果流变为高速，将自动禁用此功能。）
      * 包含来自&#x200B;**[!UICONTROL Verified Twitter accounts only.]**&#x200B;的帖子
      * 包括&#x200B;**[!UICONTROL All Content]**、**[!UICONTROL Vines Only]**&#x200B;或&#x200B;**[!UICONTROL Images Only.]**
      * 仅包含源自所选&#x200B;**[!UICONTROL Minimum number of followers]**（any、100、500、1000、1000、10,000或100,000）帐户的帖子。

有关所有流规则的其他流规则选项，请参阅[所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
