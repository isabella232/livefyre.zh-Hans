---
description: 通过单个智能界面审核内容。
title: 使用ModQ审核内容
exl-id: 694b1f45-2b24-4e80-99a1-788e2cecc8a4
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '1454'
ht-degree: 0%

---

# 使用ModQ{#moderate-content-using-modq}审核内容

通过单个智能界面审核内容。

ModQ会创建一个实时队列，其中包含您网站或网络中所有与您定义的预审核规则匹配的内容，使版主可以只关注需要他们关注的内容。

定义ModQ设置后，进入流的新内容或由用户标记的现有内容将添加到您的队列中。 对规则所做的更改不会从ModQ中删除内容，而是会根据新设置向队列中添加新内容。

ModQ允许您：

* 在上下文中进行审核，视图整个线程，单击即可批准、删除或禁止单个内容或完整线程。
* 提高工作流程的速度和效率。
* 回复内容，增加您对社区的参与。
* 使多个版主可以处理内容，而无需重复彼此的工作。

Livefyre内容在ModQ中列出最多6周，未解决的预审核流内容在ModQ中列出最多90天。

>[!NOTE]
>
>如果单个内容符合要包含在ModQ中的多个规则，则可多次列出该内容。 例如，如果某条内容触发了Offensive的用户标志规则，然后又触发了Profane的另一条规则，则它将在ModQ中列出两次。

ModQ中未显示的内容包括：

* 丢弃内容。
* 审查方批准的内容。
* 被禁用用户发布的内容，或被禁用用户应用的用户标志。

## 导航ModQ {#section_uv4_db2_yy}

ModQ分为两个选项卡式面板：

* **[!UICONTROL Items]** 列表所有Livefyre本机和SocialSync内容，它们都将进行协调。此选项卡包括审核后已标记或编辑的任何社交搜索或流内容。
* **[!UICONTROL Streams Premoderation]** 列表在启用预审的情况下从流中进入您的应用程序的所有内容。（有关详细信息，请参阅创建流。）

这两个选项卡都优惠了许多相同的过滤器和审核工具。

* **[!UICONTROL Item Count]** 队列中剩余的项目数显示在ModQ的左上角。
* **[!UICONTROL Filter]** 单 **[!UICONTROL Filter]** 击可定义将在窗格中列出内容的参数。
* **[!UICONTROL History]** 单击屏 **[!UICONTROL History]** 幕右上角的按钮，打开最近审核内容的列表，允许您查看您的作品或更改最近的审核操作。再次单击该按钮可返回到已排队的内容。 将仅显示您的100个最新操作。 **“历** 史记录”不会列表其他审查方采取的操作。

* **[!UICONTROL User Pane]** 单击页面右上方的展开或折叠按钮以打开或关闭“用户”窗格。

## 了解ModQ内容{#section_oxm_kgz_y1b}

每个列出的内容都显示预览信息，包括发布内容的站点及其作者。 选择项目将显示包括任何媒体在内的整个内容。

>[!NOTE]
>
>Livefyre本机内容将显示比通过流或其他社交媒体源添加到应用程序的内容更多的信息。

选择项目时，将显示以下信息：

* **[!UICONTROL Time in Queue:]** 列表内容添加到ModQ的时间。
* **[!UICONTROL App name:]** 显示内容的应用程序。包含应用程序的站点链接。
* **[!UICONTROL Content Body:]** 文本和媒体缩览图（如果可用）。
* **[!UICONTROL Status:]** 内容的当前状态（“待定”、“已处理”等）。
* **[!UICONTROL Author information:]** 作者的姓名和用户名。
* **[!UICONTROL Timestamp:]** 创建内容的相对时间戳。预览Studio的“应用程序内容”页面中的内容片段。
* **[!UICONTROL Flag Type:]** 冒犯、反对、垃圾信息等

   * 安全标志：垃圾邮件和批量邮件。
   * 由网络和站点不良列表应用的标志：亵渎。
   * SAFE应用的标志：仇恨言论、PII（个人身份信息）、侮辱和亵渎。
   * 用户标志：垃圾邮件、非主题、冒犯性和反对。

* **[!UICONTROL Flag origin:]** 列出标志的源。可以是SAFE、用户名或Livefyre。
* **[!UICONTROL More info:]** 列表内容的详细信息，包括“喜欢”、“用户标志”、“回复”和应用于内容的任何标记的数量。单击站点可打开内容所在站点的顶级页面。 单击时间戳将打开页面上上下文中内容的线程视图。

## ModQ {#section_r2c_qc2_yy}中的筛选器选项

单击“ModQ”窗口左上角的&#x200B;**[!UICONTROL Filter]**&#x200B;以打开一个面板，其中包含列出内容的可用筛选器选项。 当您选择选项时，ModQ将自动更新以仅列表已过滤的内容。 单击&#x200B;**[!UICONTROL Clear filters]**&#x200B;清除所有选定的选项，然后重新加载项目的完整列表。

**[!UICONTROL Items]**&#x200B;和&#x200B;**[!UICONTROL Streams Premoderation]**&#x200B;选项卡有不同的筛选器选项。

**[!UICONTROL Items]**&#x200B;和&#x200B;**[!UICONTROL Streams Premoderation]**&#x200B;下的ModQ有以下选项：

* **[!UICONTROL App]**。使用“搜索应用程序”字段按应用程序筛选结果。 可以选择多个应用程序。
* **[!UICONTROL System Flags]**。按垃圾邮件、亵渎、安全和预审规则等规则过滤内容。

   * 选择&#x200B;**[!UICONTROL Spam]**&#x200B;将列表SAFE标记为垃圾邮件的所有内容。
   * 选择&#x200B;**[!UICONTROL Profanity]**&#x200B;将列表由“网络”或“站点不良列表”标记的所有内容。
   * 选择&#x200B;**[!UICONTROL SAFE]**&#x200B;将列表因您的SAFE规则而进入ModQ的所有内容。
   * 选择&#x200B;**[!UICONTROL Premoderation]**&#x200B;将列表由“网络”、“流”或“应用程序设置”标记为“预审核”的所有内容。

* **[!UICONTROL User Flags]** 按用户标志筛选内容。选项包括“冒犯性”、“垃圾信息”、“非主题”和“反对”。
* **[!UICONTROL Rights Requests.]** 通过单击复选框，仅显示具有所授予权限的内容。
* **[!UICONTROL Entered the queue.]** 按将内容发送到ModQ的时间范围过滤内容。内容发送到ModQ的时间不一定是内容发布到其App的时间。

**[!UICONTROL Streams Premoderation]**&#x200B;下的ModQ提供以下选项：

* **[!UICONTROL Social Source]** 按内容来源的社交源筛选内容。例如，社交源的选项包括Twitter、Instagram、Facebook和RSS。

**[!UICONTROL Items]**&#x200B;下的ModQ提供以下选项：

**[!UICONTROL Moderation Recommendations]**。根据自动审核推荐提供的推荐筛选内容。

以下图像显示了ModQ中的Moderation Recommendations的外观： ![](assets/mod_reco1.png)

在&#x200B;**[!UICONTROL Network Settings > Moderation]**&#x200B;和&#x200B;**[!UICONTROL Network Settings > ModQ]**&#x200B;中设置内容时，会为内容提供审核建议。

## 可在ModQ {#section_h4g_wrn_z1b}中使用的操作

您可以决定如何处理ModQ中的每段内容。

选择以下选项之一：

* 用于批准内容的&#x200B;**[!UICONTROL Checkbox]**&#x200B;图标
* 要将内容发送到垃圾桶的&#x200B;**[!UICONTROL Trash can]**&#x200B;图标
* **[!UICONTROL Request Rights]** 向内容所有者请求对内容的权限。

   >[!NOTE]
   >
   >您不能从Instagram请求ModQ中对内容的权限。 必须使用库或应用程序内容发送来自Instagram的内容的权限请求。

* **[!UICONTROL Feature and Approve]** 以批准内容，并突出显示内容。
* **[!UICONTROL Product Tag and Approve]** 要将产品从您的产品目录添加到内容，然后进行批准。
* **[!UICONTROL Mark as Pending]** 将内容标记为待处理。

>[!NOTE]
>
>在您删除某段内容后，该段内容以及对该段内容的所有回复将从ModQ中永久删除。 要将被丢弃的内容放入应用程序中，请参阅[将被丢弃的项目重新添加到应用程序](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app)。

如果内容已处于所需状态，则选择“废纸篓”、“Bozo”或“批准”将确认该状态并从列表中删除该项目。 审核一段内容会立即从您的队列中删除它，并会在其他审核者的队列中将其停用。

>[!NOTE]
>
>流内容可能不是Bozo&#39;d。删除流内容将从流中永久删除它，并且无法撤消。

内容审核后，将从审查方的ModQ中删除，其作者无法再从流中编辑。 如果审查方取消了某个项目，或者用户删除了其评论，则该项目将在其他审查方的队列中实时显示为灰色。 当内容灰显时，页面上会显示&#x200B;**[!UICONTROL Clear Moderated]**&#x200B;按钮，允许版主将其从列表中删除，并保持其在页面上的位置，而不管其他版主活动。

## 使用ModQ {#section_tpx_qgz_y1b}中的垃圾桶函数

使用“设置”部分，选择当内容标记为“过滤”时可用的选项。

* ****[!UICONTROL Confirm Trash]**** 启用此选项，要求版主在将内容设置为“废纸篓”时确认其操作。启用后，选择&#x200B;**[!UICONTROL Trash]**&#x200B;作为内容将显示一个对话框，要求输入&#x200B;**[!UICONTROL Reason for Moderation]**，并优惠一个可输入&#x200B;**[!UICONTROL Note]**&#x200B;的字段。

   （此设置在网络级别&#x200B;**[!UICONTROL only]**&#x200B;可用，并且适用于网络下的所有站点。）

* ****[!UICONTROL Hide Replies]**** 启用此选项后，将在删除父注释或Bozo&#39;d时自动删除回复。

## 在ModQ {#section_tmw_lg1_z1b}中更改用户状态

单击“用户摘要”面板中的&#x200B;**[!UICONTROL User actions]**&#x200B;按钮以将用户设为静音、禁止或允许列表。

* **[!UICONTROL Mute:]** 允许您将标记列出内容的用户的“静音标志”。使用此选项可从预审核过滤器中排除用户的标志。 他们标记的内容不会因标记而进入ModQ，标记规则中不会包括他们的标记。
* **[!UICONTROL Ban:]** 允许您禁止在您的站点或网络中列出的用户。（只有Studio管理员或用户管理员才能禁止用户进行网络访问。）
* **[!UICONTROL Whitelist:]** 允许您允许列出您的站点或网络的列出用户。（只有Studio管理员或用户管理者才能对用户进行网络允许列表。）



使用ModQ的应用程序：

* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Siestr](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上传按钮](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
