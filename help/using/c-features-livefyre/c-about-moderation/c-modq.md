---
description: 通过单个智能界面审核内容。
seo-description: 通过单个智能界面审核内容。
seo-title: 使用ModQ审核内容
title: 使用ModQ审核内容
uuid: c630fb85-7bd0-4da0-ac7e-080e970fb4f9
translation-type: tm+mt
source-git-commit: 52f59cd15f315aa93be198f6eb586f008c18a384
workflow-type: tm+mt
source-wordcount: '1465'
ht-degree: 0%

---


# 使用ModQ审核内容{#moderate-content-using-modq}

通过单个智能界面审核内容。

ModQ会创建与您定义的预审核规则匹配的站点或网络中所有内容的实时队列，使版主只关注需要他们注意的内容。

定义ModQ设置后，进入流的新内容或用户标记的现有内容将添加到队列中。 更改规则不会从ModQ中删除内容，而是会根据新设置向队列添加新内容。

ModQ允许您：

* 在上下文中进行审核，视图整个线程，并单击“批准”、“删除”或“Bozo”(Approve)，单击即可处理单个内容或完成线程。
* 提高工作流程的速度和效率。
* 回复内容，增加您对社区的参与。
* 使多个版主可以处理内容，而无需重复彼此的工作。

Livefyre内容在ModQ中列出最多6周，而ModQ中列出了90天未解决的预审核流内容。

>[!NOTE]
>
>如果一个内容与要包含在ModQ中的多个规则匹配，则可多次列出该内容。 例如，如果某个内容触发Offensive的用户标志规则，稍后触发Profane的另一个规则，则它将在ModQ中列出两次。

ModQ中未显示的内容包括：

* 内容被丢弃。
* 审查方批准的内容。
* 被禁用用户发布的内容，或被禁用用户应用的用户标志。

## 导航ModQ {#section_uv4_db2_yy}

ModQ分为两个选项卡式面板：

* **[!UICONTROL Items]** 列表所有预定用于协调的Livefyre本机和SocialSync内容。 此选项卡包括审核后已标记或编辑的任何社交搜索或流内容。
* **[!UICONTROL Streams Premoderation]** 列表在启用预审的情况下从流进入您的应用程序的所有内容。 （有关详细信息，请参阅创建流。）

这两个选项卡优惠许多相同的过滤器和审核工具。

* **[!UICONTROL Item Count]** 队列中剩余的项目数显示在ModQ的左上角。
* **[!UICONTROL Filter]** 单 **[!UICONTROL Filter]** 击可定义窗格中列出内容的参数。
* **[!UICONTROL History]** 单击屏 **[!UICONTROL History]** 幕右上角的按钮，打开最近审核过的内容的列表，允许您查看您的作品或更改最近的审核操作。 再次单击该按钮可返回排队的内容。 将仅显示您的100个最新操作。 **历史记录** 不会列表其他审查方采取的操作。

* **[!UICONTROL User Pane]** 单击页面右上方的展开或折叠按钮以打开或关闭“用户”窗格。

## 了解ModQ内容 {#section_oxm_kgz_y1b}

每个列出的内容都显示预览信息，包括发布内容的站点及其作者。 选择项目将显示包括任何媒体在内的整个内容。

>[!NOTE]
>
>Livefyre本机内容将显示比通过流或其他社交媒体源添加到您的应用程序的内容更多的信息。

选择项目时，将显示以下信息：

* **[!UICONTROL Time in Queue:]** 列表一段内容添加到ModQ的时间。
* **[!UICONTROL App name:]** 显示内容的应用程序。 链接到包含应用程序的站点。
* **[!UICONTROL Content Body:]** 文本和媒体缩略图（如果可用）。
* **[!UICONTROL Status:]** 内容的当前状态（待定、已处理等）。
* **[!UICONTROL Author information:]** 作者的姓名和用户名。
* **[!UICONTROL Timestamp:]** 创建内容的相对时间戳。 预览Studio的“应用程序内容”页面中的内容。
* **[!UICONTROL Flag Type:]** 冒犯性、反对、垃圾邮件等。

   * 安全标志： 垃圾邮件和批量。
   * 网络和站点不良列表应用的标志： 亵渎。
   * SAFE应用的标志： 仇恨言论、PII（个人身份信息）、侮辱和亵渎。
   * 用户标志： 垃圾邮件、非主题、冒犯性和反对。

* **[!UICONTROL Flag origin:]** 列出标志的源。 可能是SAFE、用户名或Livefyre。
* **[!UICONTROL More info:]** 列表内容的详细信息，包括“喜欢”、“用户标志”、“回复”和应用于内容的任何标记数。 单击站点可打开内容所在站点的顶级页面。 单击时间戳可打开页面上下文中内容的线程视图。

## ModQ中的过滤器选项 {#section_r2c_qc2_yy}

单击 **[!UICONTROL Filter]** ModQ窗口左上角的以打开一个面板，其中包含列出内容的可用筛选器选项。 当您选择选项时，ModQ将自动更新以仅列表已过滤的内容。 单 **[!UICONTROL Clear filters]** 击以清除所有选定选项，然后重新加载项目的完整列表。

选项卡和选项卡有不 **[!UICONTROL Items]** 同的 **[!UICONTROL Streams Premoderation]** 筛选选项。

ModQ的以下选项在和下面均 **[!UICONTROL Items]** 可用 **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL App]**。使用“搜索应用程序”字段按应用程序筛选结果。 可以选择多个应用程序。
* **[!UICONTROL System Flags]**。按垃圾邮件、亵渎、安全和预审规则等规则过滤内容。

   * 选择 **[!UICONTROL Spam]** 后，将列表SAFE标记为垃圾邮件的所有内容。
   * 选择 **[!UICONTROL Profanity]** 后，将列表由您的网络或站点不良列表标记的所有内容。
   * 选择 **[!UICONTROL SAFE]** 将列表输入ModQ的所有内容，这是您的安全规则的结果。
   * 选择 **[!UICONTROL Premoderation]** 此选项将列表由您的“网络”、“流”或“应用程序设置”标记为预审核的所有内容。

* **[!UICONTROL User Flags]** 按用户标志筛选内容。 选项包括冒犯、垃圾邮件、非主题和反对。
* **[!UICONTROL Rights Requests.]** 通过单击复选框，仅显示具有所授予权限的内容。
* **[!UICONTROL Entered the queue.]** 按将内容发送到ModQ的时间范围过滤内容。 内容发送到ModQ的时间不一定是内容发布到其App的时间。

ModQ下提供以下选项 **[!UICONTROL Streams Premoderation]**:

* **[!UICONTROL Social Source]** 按内容来源的社交源筛选内容。 例如，社交来源选项包括Twitter、Instagram、Facebook和RSS。

ModQ下提供以下选项 **[!UICONTROL Items]**:

**[!UICONTROL Moderation Recommendations]**。根据自动协调推荐提供的推荐筛选内容。

以下图像显示ModQ中的审核推荐外观：  ![](assets/mod_reco1.png)

在和中设置内容时，会为其提供审核 **[!UICONTROL Network Settings > Moderation]** 建议 **[!UICONTROL Network Settings > ModQ]**。

## 可在ModQ中使用的操作 {#section_h4g_wrn_z1b}

您可以决定如何处理ModQ中的每段内容。

选择以下选项之一：

* 批 **[!UICONTROL Checkbox]** 准内容的图标
* 将内 **[!UICONTROL Trash can]** 容发送到垃圾桶的图标
* **[!UICONTROL Request Rights]** 向内容所有者请求对内容的权限。

   >[!NOTE]
   >
   >您无法在ModQ中请求Instagram内容的权限。 必须使用库或应用程序内容发送Instagram内容的权限请求。

* **[!UICONTROL Feature and Approve]** 以批准内容，同时还可以对内容进行特征处理。
* **[!UICONTROL Product Tag and Approve]** 要将产品从产品目录添加到内容，然后进行批准。
* **[!UICONTROL Mark as Pending]** 将内容标记为待处理。

>[!NOTE]
>
>在您删除某段内容后，该段内容以及对该段内容的所有回复将从ModQ中永久删除。 要在应用程序中放置已丢弃的内容，请参 [阅将已丢弃的项目添加回应用程序](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app)。

如果内容已处于所需状态，则选择“废纸篓”、“Bozo”或“批准”将确认该状态并从列表中删除该项目。 协调一段内容将立即从您的队列中删除，并将在其他管理者的队列中取消激活它。

>[!NOTE]
>
>流内容可能不是Bozo’d。 删除流内容将从流中永久删除它，并且无法撤消。

内容审核后，将从审查方的ModQ中删除，其作者无法再从流中编辑它。 如果审查方注销了某个项目，或者用户删除了其评论，则该项目将实时显示在其他审查方的队列中。 当内容灰显时，页面上会显 **[!UICONTROL Clear Moderated]** 示按钮，允许版主从其列表中删除该按钮，并且无论其他版主活动如何，都可以在页面中保留其位置。

## 在ModQ中使用废纸函数 {#section_tpx_qgz_y1b}

使用设置部分选择将内容标记为“已过滤”时可用的选项。

* ****[!UICONTROL Confirm Trash]**** 启用此选项，要求版主在将内容设置为废纸篓时确认其操作。 启用后，选 **[!UICONTROL Trash]** 择内容将显示一个对话框，要 **[!UICONTROL Reason for Moderation]**&#x200B;求输入内容，并优惠可 **[!UICONTROL Note]** 以在其中输入字段。

   (此设置在网 **[!UICONTROL only]** 络级别可用，并且适用于您网络下的所有站点。)

* ****[!UICONTROL Hide Replies]**** 启用此选项，可在删除父注释或Bozo’d时自动删除回复。

## 在ModQ中更改用户状态 {#section_tmw_lg1_z1b}

单击“用 **[!UICONTROL User actions]** 户摘要”面板中的按钮以将用户设为静音、禁止或允许列表。

* **[!UICONTROL Mute:]** 允许您将标记所列内容的用户的标记设为静音。 使用此选项可从预审核过滤器中排除用户的标志。 标志标记的内容不会因标志而进入ModQ，标志规则中不会包括其标志。
* **[!UICONTROL Ban:]** 允许您禁止列出的用户访问您的站点或网络。 （只有Studio管理员或用户管理者才能禁止用户进行网络访问。）
* **[!UICONTROL Whitelist:]** 允许您允许列表您的站点或网络中列出的用户。 (只有Studio管理员或用户管理者才能对用户进行网络列表。)



使用ModQ的应用程序：

* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidesk](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上传按钮](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

