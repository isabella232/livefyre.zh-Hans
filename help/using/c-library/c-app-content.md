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

通过库中的“应用程序内容”选项卡，您可以搜索和审核跨应用程序发布的内容。 该选 **[!UICONTROL App Content]** 项卡允许使用通配符搜索的多个搜索筛选器，以便更快、更轻松地定义搜索参数。

使用“应用程序内容”选项卡可以：

* 搜索内容
* 查看内容历史
* 审核内容
* 添加标签
* 功能内容
* 将产品目录中的内容与产品关联

有关如何使用“应用程序内容”选项卡审核内容的详细信息，请参阅 [](../c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md#c_moderate_content_using_app_content)。

## 通配符搜索 {#section_jvr_ntm_zz}

Livefyre搜索字段支持通配符，这允许您向单词（或单词片段）添加星号(*)以捕获部分匹配项。

例如：

* 球只返回球
* 球*返回球和球
* *返球球和足球
* *ball*返回球和球，单球和滚雪球

## 搜索内容 {#section_fw1_mtm_zz}

“应用程序内容”面板允许您使用多个不同的内容过滤选项缩小搜索范围。

![](assets/PublishedState-1024x367.png)

使用下拉 **[!UICONTROL Quick Filters]** 变换将返回的内容缩 **[!UICONTROL All Content]**&#x200B;小为 **[!UICONTROL All Sidenotes]**、、 **[!UICONTROL Approved]**、 **[!UICONTROL Approved & Flagged]**、 **[!UICONTROL Pending]**&#x200B;或 **[!UICONTROL Rights Requests]** 状态。 然后选择一 **[!UICONTROL Filter by]** 个选项，然后使用可用的复选框或输入字段缩小搜索范围。

使用下拉菜单按、、、或对列表中的内 **[!UICONTROL Newest]**&#x200B;容进 **[!UICONTROL Oldest]**&#x200B;行 **[!UICONTROL Recently updated]**&#x200B;排 **[!UICONTROL Most flags]** 序 **[!UICONTROL Most liked]**。

## 按选项筛选 {#section_aqn_xqm_zz}

使用该 **[!UICONTROL Filter by]** 栏按以下选项进行筛选：

* **状态** 允许您按内容的当前审核状态进行筛选：** [!UICONTROL All Content]**、 **[!UICONTROL Approved]**、 **[!UICONTROL Pending]**&#x200B;或 **[!UICONTROL Bozo]**。

* **源** -允许您按内容的源进行筛选。 选择 **[!UICONTROL Livefyre]** 以列出直接发布到流中的用户生成的内容。 选择 **[!UICONTROL Facebook]**、 **[!UICONTROL Twitter]**&#x200B;或 **[!UICONTROL RSS]** 以包括从这些源引入应用程序的内容。

* **旗标** “选择旗标”允许您按 **[!UICONTROL User Flags]** （垃圾邮件、非主题、冒犯性或反对）、SAFE( **[!UICONTROL System Flags]** Profity、Spam或Magically仲裁)应用或筛选 **[!UICONTROL Moderation Recommendations]**。 ![](assets/appcontentfilter.png)

* **日期／时间** -允许您根据内容最初的时间（或通过SocialSync或流拉入应用程序）或最后的时间 **[!UICONTROL Created]****[!UICONTROL Modified]** （编辑、标记或状态更改）进行筛选。

* **作者** ：允许您按作者的地址、 **[!UICONTROL IP]****[!UICONTROL Display Name]** （可在“用户”面板上或作者发布的内容的上方找到）或 **[!UICONTROL User ID]**（可在“用户”面板上找到）进行筛选。

* **包含** 允许您按或筛选最近90天的内 **[!UICONTROL Keyword]** 容 **[!UICONTROL Content Tag]**。 选中此复 **[!UICONTROL Media]** 选框可仅返回包含媒体的内容。 (要搜索所有内容，请向下滚动浏览列表中的所有内容，然后单击 **[!UICONTROL Search full data]**。)

   **** 注意：不支持多关键字和内容标记搜索。 如果输入了多个关键字或标记，则搜索将使用最后一个单词。

   按内容标记搜索时，当您在搜索字段中键入时，将自动填充建议的标记。 搜索结果将返回所有已分配标记的内容。 (使用此字段搜索特色内容，或在Studio中单 **[!UICONTROL Featured]** 击任何特色内容的标签。)

   **** 注意：在标记名称前使用减号(-)可搜索不包含该标记的内容。 例如：搜索“-Miley”以搜索不包含“Miley”标签的所有内容。

* **应用程序** 允许您按、 **[!UICONTROL Collection ID]**&#x200B;或父 **[!UICONTROL App Tag]** ID **进行筛选**。 按父级ID过滤将返回对输入内容ID的回复的所有内容。 （通过输入以逗号分隔的标记，按多个标记过滤。）

* **权限** 允许您按权限请求状态进行筛选：** [!UICONTROL Requested]**、 **[!UICONTROL Granted]**、 **[!UICONTROL Replied]**&#x200B;或 **[!UICONTROL Expired]**。

## Bozo Content {#section_afl_vqm_zz}

在应用程 **[!UICONTROL Bozo]** 序中，内容仅向内容作者显示。 这允许用户相信其内容已获得批准，同时隐藏其内容，使其不受所有其他用户和版主的影响。

>[!NOTE]
>
>使用SocialSync或Streams生成的社交内 **[!UICONTROL cannot]** 容设置为Bozo。

您可以Bozo内容，原因如下：

* SAFE标识为垃圾邮件的内容会自动设置为Bozo状态。
* “禁止的用户”中的所有内容将自动设置为Bozo。
* 内容可以标记为Studio中的Bozo。
* 版主可以直接在流中对内容进行Bozo处理。

## 查看内容历史 {#section_ayz_tqm_zz}

内容面板允许您查看所有列出内容的历史记录，包括预审、垃圾邮件过滤、发布日期以及分配给该项目的任何用户标记或备注。

使用内容面板底部的选项卡查看其历史记录。

* **[!UICONTROL More Info:]** 列出此内容上的所有活动，包括提交、编辑、垃圾邮件检查、状态更改和备注。 此部分还显示Livefyre内容ID和用户的IP地址。
* **[!UICONTROL Replies:]** 列出最多6个回复。 单击 **[!UICONTROL Show all replies]** 以显示对帖子的所有回复。

* **[!UICONTROL Flags & Reports:]** 列出所有用户标志、标记内容的用户的头像以及任何报告（标记内容时由用户添加的注释）。
* **[!UICONTROL Add a note:]** 允许您添加注释，其他管理员或版主可看到该注释。
* **[!UICONTROL Request Rights:]** 打开对 **[!UICONTROL New Rights Request]** 话框，从中可以发出权限请求。

* **[!UICONTROL Save as Asset:]**[!UICONTROL Advanced Options]** **打开对话框，该对话框允许您将选定项目保存到资产库，将其发布到应用程序，或向其作者请求重用权限。

![](assets/PublishedMoreInfo-1024x462.png)

## 向内容添加标记 {#section_xb4_mxr_rdb}

标记内容允许您对内容进行分类和组织，以便轻松进行检索和样式自定义，或将内容标记为特色内容。

要添加标记，只需单击内容下的加号( **[!UICONTROL +]**)图标。 输入新标记，或从现有标记列表中选择。

![](assets/PublishedAddTag-1024x338.png)

## 在所有资产中搜索图像 {#section_zxf_hsf_wcb}

在将内容添加到库后，可以按智能标记搜索内容。

在库中的所有资产下，您可以通过单击来搜索现有图像，然后 **[!UICONTROL Show Filters]** 执行以下操作：

* 在搜索字段中输入要搜索的文本
* 按相关度排序
* 在字段中输入要 **[!UICONTROL Tags]** 按智能标记搜索的文本。 “智能标签”排名算法使用智能标签置信度得分筛选内容，内容有多新，以及用户为内容提供的星级数。

## 特色内容 {#section_emb_kqm_zz}

选择默认标 **[!UICONTROL Featured]** 记将内容标记为特色，并突出显示它对您的用户同样重要。 标记后，使用自定义样式选项自定义应用程序中的特色内容。

## 要特征化或取消特征化内容 {#section_ojx_3qm_zz}

* 从Studio中，单击某 **[!UICONTROL +]** 段内容旁的符号，在下拉列表中选 **[!UICONTROL Featured]** 择标记，然后单击“功能 **[!UICONTROL Enter]** ”内容。 标记将保存并显示在内容的旁边。

* 要取消功能，请单 **[!UICONTROL x]** 击内 **[!UICONTROL Featured]** 容片段上显示的标记。

* 从评论、实时博客或评论应用程序中，将指针悬停在要显示的内容上并单击 **[!UICONTROL Feature]**。 要取消功能，只需将鼠标悬停在内容上并单击 **[!UICONTROL Unfeature]**。

>[!NOTE]
>
>由于空间限制，聊天内容可能只能使用Studio进行特色或非特色，并且可能不能从应用程序本身进行特色。

## 编辑特色内容 {#section_pyw_hqm_zz}

大多数针对内容的常规操作都可对特色内容执行，但以下情况除外：

* 无法标记特色内容。
* 用户在内容已经过“特色”后无法编辑其内容，但他们仍可以根据需要删除它。 版主可以编辑特色内容。

