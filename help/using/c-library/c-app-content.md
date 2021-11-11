---
description: 在您的Livefyre网络中管理内容。
title: “应用程序内容”选项卡
exl-id: 8b3e5281-59ba-4321-8fee-4160ab7a5d5e
source-git-commit: 600c9712366f5de303de27cf39045beccd4145eb
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# “应用程序内容”选项卡{#app-content-tab}

在您的Livefyre网络中管理内容。

利用库中的应用程序内容选项卡，可搜索和审核在应用程序中发布的内容。 的 **[!UICONTROL App Content]** 选项卡启用多个带通配符搜索的搜索过滤器，以便您更快、更轻松地定义搜索参数。

使用“应用程序内容”选项卡可以：

* 搜索内容
* 查看内容历史记录
* 审核内容
* 添加标签
* 功能内容
* 将内容与产品目录中的产品关联

有关如何使用应用程序内容选项卡审核内容的更多信息，请参阅 [使用“应用程序内容”选项卡审核内容](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content).

## 通配符搜索 {#section_jvr_ntm_zz}

Livefyre搜索字段支持通配符，利用通配符，可向单词（或单词片段）添加星号(*)以捕获部分匹配项。

例如：

* 球只返回球
* 球*返回球和球
* *返回球和足球
* *ball*返回球和单球，滚雪球

## 搜索内容 {#section_fw1_mtm_zz}

“应用程序内容”面板允许您使用多个不同的内容过滤选项来缩小搜索范围。

![](assets/PublishedState-1024x367.png)

使用 **[!UICONTROL Quick Filters]** 下拉将返回的内容缩小到 **[!UICONTROL All Content]**, **[!UICONTROL All Sidenotes]**, **[!UICONTROL Approved]**, **[!UICONTROL Approved & Flagged]**, **[!UICONTROL Pending]**&#x200B;或 **[!UICONTROL Rights Requests]** 状态。 然后，选择 **[!UICONTROL Filter by]** 复选框或输入字段来缩小搜索范围。

使用下拉菜单按 **[!UICONTROL Newest]**, **[!UICONTROL Oldest]**, **[!UICONTROL Recently updated]**, **[!UICONTROL Most flags]** 或 **[!UICONTROL Most liked]**.

## 按选项过滤 {#section_aqn_xqm_zz}

使用 **[!UICONTROL Filter by]** 按以下选项进行筛选：

* **州** 用于按内容的当前审核状态进行过滤：** [!UICONTROL All Content]**, **[!UICONTROL Approved]**, **[!UICONTROL Pending]**&#x200B;或 **[!UICONTROL Bozo]**.

* **来源** 用于按内容的源进行过滤。 选择 **[!UICONTROL Livefyre]** 列出用户生成的内容，这些内容直接发布到流中。 选择 **[!UICONTROL Facebook]**, **[!UICONTROL Twitter]**&#x200B;或 **[!UICONTROL RSS]** 以包含从这些源提取到应用程序的内容。

* **标记** 选择标记允许您按 **[!UICONTROL User Flags]** （垃圾信息、非主题、冒犯或不同意）， **[!UICONTROL System Flags]** 由SAFE（亵渎、垃圾邮件或磁性审核）应用，或 **[!UICONTROL Moderation Recommendations]**. ![](assets/appcontentfilter.png)

* **日期/时间** 允许您按内容最初的时间过滤 **[!UICONTROL Created]** （或通过SocialSync或流提取到应用程序中），或最后 **[!UICONTROL Modified]** （已编辑、标记或状态已更改）。

* **作者** 用于按作者的 **[!UICONTROL IP]** 地址， **[!UICONTROL Display Name]** （可在“用户”面板中或作者发布内容的上方找到），或 **[!UICONTROL User ID]**（在“用户”面板上找到）。

* **包含** 允许您按 **[!UICONTROL Keyword]** 或 **[!UICONTROL Content Tag]**. 选择 **[!UICONTROL Media]** 复选框以仅返回包含媒体的内容。 (要搜索所有内容，请向下滚动浏览列表中的所有内容，然后单击 **[!UICONTROL Search full data]**.)

   **注意：** 不支持多关键字和内容标记搜索。 如果输入了多个关键词或标记，则将使用最后一个词进行搜索。

   按内容标记搜索时，当您在搜索字段中键入时，将自动填充建议的标记。 搜索结果将返回已分配标记的所有内容。 (使用此字段搜索特色内容，或单击 **[!UICONTROL Featured]** 标签。)

   **注意：** 在标记名称前使用减号(-)来搜索不包含该标记的内容。 例如：搜索“ — Miley”以搜索不包含“Miley”标记的所有内容。

* **应用程序** 允许您按 **[!UICONTROL Collection ID]**, **[!UICONTROL App Tag]**&#x200B;或 **父ID**. 按父ID过滤会返回对输入内容ID做出回复的所有内容。 （通过输入以逗号分隔的标记，按多个标记进行过滤。）

* **权限** 允许您按权限请求状态进行过滤：** [!UICONTROL Requested]**, **[!UICONTROL Granted]**, **[!UICONTROL Replied]**&#x200B;或 **[!UICONTROL Expired]**.

## 博佐内容 {#section_afl_vqm_zz}

在应用程序中， **[!UICONTROL Bozo]** 内容仅向内容作者显示。 这允许用户认为其内容已获得批准，同时将其隐藏在所有其他用户和审核者面前。

>[!NOTE]
>
>源自SocialSync或流的社交内容 **[!UICONTROL cannot]** 被设置为博佐。

您可以出于以下原因查看Bozo内容：

* 被SAFE标识为垃圾邮件的内容会自动设置为Bozo状态。
* “禁止的用户”中的所有内容都自动设置为Bozo。
* Studio中的内容可以标记为Bozo。
* 审核者可以直接在流中Bozo内容。

## 查看内容历史记录 {#section_ayz_tqm_zz}

内容面板允许您查看所有列出内容的历史记录，包括预审、垃圾邮件过滤、发布日期以及分配给该项目的任何用户标记或注释。

使用内容面板底部的选项卡查看其历史记录。

* **[!UICONTROL More Info:]** 列出此内容上的所有活动，包括提交、编辑、垃圾邮件检查、状态更改和注释。 Livefyre内容ID和用户的IP地址也会显示在此部分中。
* **[!UICONTROL Replies:]** 列出最多6个回复。 单击 **[!UICONTROL Show all replies]** 以显示对帖子的所有回复。

* **[!UICONTROL Flags & Reports:]** 列出所有用户标记，以及标记内容的用户头像和任何报表（用户在标记内容时添加的注释）。
* **[!UICONTROL Add a note:]** 用于添加注释，以供其他管理员或审核者查看。
* **[!UICONTROL Request Rights:]** 打开 **[!UICONTROL New Rights Request]** 对话框，可从中发出权限请求。

* **[!UICONTROL Save as Asset:]**打开 **[!UICONTROL Advanced Options]** 对话框，用于将选定的项目保存到资产库、将其发布到应用程序，或从其作者请求重用权限。

![](assets/PublishedMoreInfo-1024x462.png)

## 向内容添加标记 {#section_xb4_mxr_rdb}

标记内容允许您对内容进行分类和组织，以便轻松检索和进行样式自定义，或将内容标记为特色内容。

要添加标记，只需单击加号( **[!UICONTROL +]**)图标。 输入新标记，或从现有标记列表中进行选择。

![](assets/PublishedAddTag-1024x338.png)

## 在所有资产中搜索图像 {#section_zxf_hsf_wcb}

将内容添加到库后，即可按智能标记搜索内容。

在库中的所有资产下，您可以通过单击 **[!UICONTROL Show Filters]** 然后：

* 在搜索字段中输入要搜索的文本
* 按相关性排序
* 在 **[!UICONTROL Tags]** 字段进行搜索。 智能标记排名算法使用智能标记置信度得分过滤内容、内容的新增内容以及用户为内容提供的星级数。

## 特色内容 {#section_emb_kqm_zz}

选择默认 **[!UICONTROL Featured]** 标记来将内容标记为特有内容，并突出显示该内容对您的用户同样重要。 标记后，使用自定义样式选项来自定义应用程序中的特色内容。

## 功能或取消功能内容 {#section_ojx_3qm_zz}

* 在Studio中，单击 **[!UICONTROL +]** 在某段内容旁边签名，选择 **[!UICONTROL Featured]** 标记，然后单击 **[!UICONTROL Enter]** 功能内容。 标记将被保存并显示在内容旁边。

* 要取消功能，请单击 **[!UICONTROL x]** 在 **[!UICONTROL Featured]** 标记。

* 在“评论”、“实时博客”或“审阅”应用程序中，将鼠标悬停在要显示的内容上，然后单击 **[!UICONTROL Feature]**. 要取消功能，只需将鼠标悬停在内容上，然后单击 **[!UICONTROL Unfeature]**.

>[!NOTE]
>
>由于空间限制，聊天内容可能只能使用Studio进行特色显示或不能使用Studio进行特色显示，也可能不会从应用程序本身进行特色显示。

## 编辑特色内容 {#section_pyw_hqm_zz}

除以下内容外，大多数对内容的常规操作都可以对特色内容执行：

* 无法标记特色内容。
* 用户在内容“特色”后无法编辑其内容，不过如果他们愿意，仍可以删除该内容。 审核者可以编辑特色内容。
