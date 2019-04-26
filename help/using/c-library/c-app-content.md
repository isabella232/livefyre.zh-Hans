---
description: 跨Livefyre网络管理内容。
seo-description: 跨Livefyre网络管理内容。
seo-title: 应用程序内容选项卡
solution: Experience Manager
title: 应用程序内容选项卡
uuid: 65b23085-2b79-4a6f-96c9-44b421805312
translation-type: tm+mt
source-git-commit: 0c5420fcb3ba2e12375e92d4574d0a6dff310869

---


# 应用程序内容选项卡{#app-content-tab}

跨Livefyre网络管理内容。

通过库中的应用程序内容选项卡，您可以搜索并审核在应用程序中发布的内容。**[!UICONTROL App Content]** 该选项卡通过通配符搜索启用多个搜索过滤器，使您能够更快、更轻松地定义搜索参数。

使用应用程序内容选项卡可以：

* 搜索内容
* 查看内容历史记录
* 审核内容
* 添加标记
* 功能内容
* 将内容与产品目录中的产品关联

有关如何使用应用程序内容选项卡审核内容的更多信息 [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content)，请参阅。

## 通配符搜索 {#section_jvr_ntm_zz}

Livefyre搜索字段支持通配符，允许您将星号(*)添加到单词(或单词片段)以捕获部分匹配项。

例如：

* ball只返回ball
* ball*返回球和气球
* *球返回球和足球
* * ball*返回ball和uncall和s下雪

## 搜索内容 {#section_fw1_mtm_zz}

应用程序内容面板允许您使用多种不同的内容筛选选项缩小搜索范围。

![](assets/PublishedState-1024x367.png)

使用 **[!UICONTROL Quick Filters]** 下拉列表将返回的内容缩小为 **[!UICONTROL All Content]****[!UICONTROL All Sidenotes]****[!UICONTROL Approved]****[!UICONTROL Approved & Flagged]**、 **[!UICONTROL Pending]****[!UICONTROL Rights Requests]** 或状态。然后选择一个 **[!UICONTROL Filter by]** 选项，然后使用复选框或输入字段缩小搜索范围。

使用下拉菜单对列表中的内容排序 **[!UICONTROL Newest]**、 **[!UICONTROL Oldest]**排序或 **[!UICONTROL Recently updated]****[!UICONTROL Most flags]****[!UICONTROL Most liked]**排序。

## 按选项过滤 {#section_aqn_xqm_zz}

使用 **[!UICONTROL Filter by]** 此栏可按以下选项进行筛选：

* **状态** 允许您按内容的当前协调状态进行过滤：** [!UICONTROL All Content]** **[!UICONTROL Approved]**、 **[!UICONTROL Pending]****[!UICONTROL Bozo]**或。

* **源** 允许您按内容的源过滤。选择 **[!UICONTROL Livefyre]** 此选项可将用户生成的内容直接发布到流中。选择 **[!UICONTROL Facebook]**、 **[!UICONTROL Twitter]**或 **[!UICONTROL RSS]** 包含从这些来源拖入您的应用程序的内容。

* **标记** 选择标记允许您筛选( **[!UICONTROL User Flags]** 垃圾邮件、非主题、攻击性或反对)，由SAFE **[!UICONTROL System Flags]** (亵渎、垃圾邮件或智能仲裁)应用，或 **[!UICONTROL Moderation Recommendations]**以其他方式应用。 ![](assets/appcontentfilter.png)

* **日期/时间** 允许您在内容最初 **[!UICONTROL Created]** 是(或通过SocialSync或流拖入应用程序)或上次 **[!UICONTROL Modified]** (已编辑、标记或状态更改)时对其进行处理。

* **作者** 允许您按作者 **[!UICONTROL IP]** 的地址进行筛选( **[!UICONTROL Display Name]** 在“用户”面板上或从作者发布的内容上或在“用户 **[!UICONTROL User ID]**”面板中找到)。

* **包含允许** 您筛选内容的最近90天 **[!UICONTROL Keyword]****[!UICONTROL Content Tag]**。选中此 **[!UICONTROL Media]** 复选框可仅返回包含媒体的内容。(要搜索所有内容，请向下滚动列表中的所有内容，然后单击 **[!UICONTROL Search full data]**。)

   **注意：** 不支持多个关键字和内容标记搜索。如果输入了多个关键字或标记，则将使用最后一个词进行搜索。

   按内容标记搜索时，建议标记在您键入搜索字段时会自动填充。搜索结果将返回已分配标记的所有内容。(使用此字段搜索特色内容，或单击Studio中任何特色内容 **[!UICONTROL Featured]** 上的标签。)

   **注意：** 在标记名称之前使用减号(-)对不包含该标记的内容进行搜索。例如：搜索“-Miley”可搜索不包含“Milley”标记的所有内容。

* **应用程序** 允许您按 **[!UICONTROL Collection ID]**、 **[!UICONTROL App Tag]**或 **父ID筛选**。按父ID过滤可返回回复内容ID的所有内容。(通过以逗号分隔标记来筛选多个标记。)

* **权限** 允许您按权限请求状态过滤：** [!UICONTROL Requested]** **[!UICONTROL Granted]**、 **[!UICONTROL Replied]****[!UICONTROL Expired]**或。

## Bozo内容 {#section_afl_vqm_zz}

在应用程序中 **[!UICONTROL Bozo]** ，内容仅显示给内容作者。这允许用户相信他们的内容已获得批准，同时还将从所有其他用户和版主隐藏。

>[!NOTE]
>
>由Social同步或流 **[!UICONTROL cannot]** 生成的社交内容设置为Bozo。

由于以下原因，您可以使用Botzo内容：

* 被SAFE识别为垃圾邮件的内容会自动设置为Botzo状态。
* “已禁止用户”的所有内容将自动设置为Bozo。
* 内容可在Studio中标记为Bozo。
* 版主可以直接在流中嵌入内容。

## 查看内容历史记录 {#section_ayz_tqm_zz}

通过内容面板，您可以查看列出的所有内容的历史记录，包括预先审核、垃圾邮件过滤、发布日期以及分配给该项目的任何用户标记或备注。

使用内容面板底部的选项卡查看其历史记录。

* **[!UICONTROL More Info:]** 列出此内容的所有活动，包括提交、编辑、垃圾邮件检查、状态更改和备注。Livefyre内容ID和用户的IP地址也在此部分中显示。
* **[!UICONTROL Replies:]** 最多可列出个回复。单击 **[!UICONTROL Show all replies]** 以显示帖子的所有回复。

* **[!UICONTROL Flags & Reports:]** 列出所有用户标记、标记内容的用户的头像以及任何报告(标记内容时由用户添加的备注)。
* **[!UICONTROL Add a note:]** 允许您添加备注，对其他管理员或版主可见。
* **[!UICONTROL Request Rights:]** 打开 **[!UICONTROL New Rights Request]** 可从中发出权限请求的对话框。

* ****[!UICONTROL Save as Asset:]打开 **[!UICONTROL Advanced Options]** 对话框，允许您将选定项目保存到资产库、将其发布到应用程序或请求重复使用作者的权限。

![](assets/PublishedMoreInfo-1024x462.png)

## 向内容添加标记 {#section_xb4_mxr_rdb}

通过标记内容，您可以对内容进行分类和组织，以便轻松检索和样式自定义，或将内容标记为特色内容。

要添加标记，只需单击内容下的加号( **[!UICONTROL +]**)图标。输入新标记，或从现有标记列表中进行选择。

![](assets/PublishedAddTag-1024x338.png)

## 在所有资产中搜索图像 {#section_zxf_hsf_wcb}

将内容添加到库后，您可以按智能标签搜索内容。

在库中，在“所有资产”下，您可以通过单击 **[!UICONTROL Show Filters]** 然后单击以下图标来搜索现有图像：

* 输入要在搜索字段中搜索的文本
* 按相关性排序
* 在 **[!UICONTROL Tags]** 字段中输入文本以按智能标记进行搜索。Smart Tags排名算法使用智能标签置信分数、内容的新内容以及用户提供内容的星星数过滤内容。

## 特色内容 {#section_emb_kqm_zz}

选择默认 **[!UICONTROL Featured]** 标签以将内容标记为特色，并突出显示对用户的重要性。标记后，使用自定义样式选项自定义应用程序中的特色内容。

## 到功能或非功能内容 {#section_ojx_3qm_zz}

* 在Studio中，单击某个内容旁边 **[!UICONTROL +]** 的符号，在下拉列表中选择该 **[!UICONTROL Featured]** 标记，然后单击 **[!UICONTROL Enter]** “功能”内容。标记将保存并显示在内容的旁边。

* 要取消功能，请单击 **[!UICONTROL x]** 内容中显示的 **[!UICONTROL Featured]** 标记上的图标。

* 从评论、Live Blog或Reviews App中，将鼠标悬停在要功能的上方，然后单击 **[!UICONTROL Feature]**。要取消功能，只需将鼠标悬停在内容上方，然后单击 **[!UICONTROL Unfeature]**。

>[!NOTE]
>
>由于空间限制，聊天内容只能使用Studio进行特色或非特色处理，不能从应用程序本身中进行特色。

## 编辑特色内容 {#section_pyw_hqm_zz}

可以对特色内容执行大多数常规操作，但以下除外：

* 不能标记特色内容。
* 用户在“特色”后无法编辑其内容，但仍可根据需要删除其内容。版主可以编辑特色内容。

