---
description: 通过单一智能界面审核内容。
seo-description: 通过单一智能界面审核内容。
seo-title: 使用ModQ审核内容
title: 使用ModQ审核内容
uuid: c630fb85-7bd0-4da0-ac7 e-080e970 fb4 f9
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 使用ModQ审核内容{#moderate-content-using-modq}

通过单一智能界面审核内容。

ModQ创建跨站点或网络的所有内容的实时队列，它们匹配您定义的预审核规则，使审核者只能专注于需要他们注意的内容上。

一旦定义了Modq设置，输入流的新内容或由用户标记的现有内容将添加到队列中。对规则的更改不会从Modq删除内容，但是会根据新设置向队列中添加新内容。

ModQ允许您：

* 只需单击一下，即可在上下文中审核、查看整个线程、批准、废纸篓或Bozo，或单击即可完成线程。
* 提高工作流程的速度和效率。
* 回复内容，增加您与社区的参与。
* 使多个版主能够通过内容工作，而无需重复他人的工作。

Livefyre内容在ModQ中以最多周的时间列出，预先审核的流内容在Modq中列出90天。

>[!NOTE]
>
>如果一段内容与多个规则匹配，则可能多次列出单个内容。例如，如果某段内容触发了“攻击”的用户旗标规则，稍后又触发了“亵渎”规则，它将以两次模型形式列出。

未在ModQ中显示的内容包括：

* 已删除的内容。
* 审核者批准的内容。
* 被禁止用户发布的内容或被禁止用户应用的用户旗标。

## 导航模型 {#section_uv4_db2_yy}

Modq分为两个选项卡式面板：

* **[!UICONTROL Items]** 列出所有用于协调的Livefyre本机和SocialSync内容。此选项卡包括在协调后已被标记或编辑的任何社交搜索或流内容。
* **[!UICONTROL Streams Premoderation]** 列出在启用了Premieric功能的流中输入应用程序的所有内容。(有关详细信息，请参阅创建流。)

两个选项卡都提供许多相同的过滤器和协调工具。

* **[!UICONTROL Item Count]** 队列中剩余的项目数显示在ModQ左上角。
* **[!UICONTROL Filter]** 单击 **[!UICONTROL Filter]** 以定义内容将在窗格中列出的参数。
* **[!UICONTROL History]** 单击屏幕右上角的 **[!UICONTROL History]** 按钮以打开最近审核的内容列表，允许您查看工作或更改最近的审核操作。再次单击该按钮可返回到您排队的内容。只会显示100个最近的操作。**历史记录** 不会列出其他审核者采取的操作。

* **[!UICONTROL User Pane]** 单击页面右上角的展开或折叠按钮以打开或关闭用户窗格。

## 理解模型内容 {#section_oxm_kgz_y1b}

每个列出的内容都会显示预览信息，包括发布地点和作者的站点。选择项目将显示包括任何媒体在内的整个内容。

>[!NOTE]
>
>与通过流或其他社交媒体源添加到您的应用程序中的内容相比，Livefyre本机内容显示的信息会更多。

选择项目时会显示以下信息：

* **[!UICONTROL Time in Queue:]** 列出将内容片段添加到ModQ的时间。
* **[!UICONTROL App name:]** 显示内容的应用程序。使用应用程序指向网站的链接。
* **[!UICONTROL Content Body:]** 文本和媒体缩略图(如果可用)。
* **[!UICONTROL Status:]** 内容的当前状态(等待、已删除等)。
* **[!UICONTROL Author information:]** 作者姓名和用户名。
* **[!UICONTROL Timestamp:]** 创建内容时的相对时间戳。在Studio的“应用程序内容”页面中为内容提供权限。
* **[!UICONTROL Flag Type:]** 攻击、反对、垃圾邮件等。

   * 安全标志：垃圾邮件和批量。
   * 网络和站点亵渎列表应用的标志：亵渎。
   * SAFE应用的标记：仇恨言论、PII(个人识别信息)、侮辱和亵渎。
   * 用户标记：垃圾邮件、非主题、攻击性和反对。

* **[!UICONTROL Flag origin:]** 列出的标志的源。可为SAFE、用户名或Livefyre。
* **[!UICONTROL More info:]** 列出内容的详细信息，包括称赞次数、用户标记、回复以及应用于内容的任何标记。单击站点可打开内容所在站点的顶级页面。单击时间戳可打开页面上下文中内容的线程视图。

## Modq中的过滤器选项 {#section_r2c_qc2_yy}

单击 **[!UICONTROL Filter]** ModQ窗口左上角可打开一个面板，其中包含可供列出的内容的可用筛选器选项。当您选择选项时，ModQ将自动更新以仅列出筛选的内容。单击 **[!UICONTROL Clear filters]** 以清除所有选定的选项，并重新加载项目的完整列表。

不同的过滤器选项可用于 **[!UICONTROL Items]** 和 **[!UICONTROL Streams Premoderation]** 选项卡。

下面两 **[!UICONTROL Items]** 个选项可 **[!UICONTROL Streams Premoderation]**用于ModQ：

* **[!UICONTROL App]**. 使用“搜索应用程序”字段按App筛选结果。可能会选择多个应用程序。
* **[!UICONTROL System Flags]**. 按垃圾邮件、亵渎、安全和预先审核规则等规则过滤内容。

   * 选择 **[!UICONTROL Spam]** 将列出所有标记为垃圾邮件的内容。
   * 选择 **[!UICONTROL Profanity]** 将列出网络或站点亵渎列表中标记的所有内容标记。
   * 选择 **[!UICONTROL SAFE]** 将列出根据您的安全规则输入Modq的所有内容。
   * 选择 **[!UICONTROL Premoderation]** 将列出网络、流或应用程序设置为预审核标记的所有内容。

* **[!UICONTROL User Flags]** 按用户标记过滤内容。选项包括攻击性、垃圾邮件、非主题和反对。
* **[!UICONTROL Rights Requests.]** 只显示单击复选框授予权限的内容。
* **[!UICONTROL Entered the queue.]** 按内容发送到ModQ时的时间范围过滤内容。发送到ModQ的时间不一定是内容发布到其App的时间。

以下选项适用于下面的ModQ **[!UICONTROL Streams Premoderation]**：

* **[!UICONTROL Social Source]** 按内容来源筛选内容。例如，社交源选项包括Twitter、Instagram、Facebook和RSS。

以下选项适用于下面的ModQ **[!UICONTROL Items]**：

**[!UICONTROL Moderation Recommendations]**. 根据自动协调推荐提供的推荐过滤内容。

以下图像显示了“审核推荐”在ModQ中的外观： ![](assets/mod_reco1.png)

在设置和 **[!UICONTROL Network Settings > Moderation]** 设置内容时，为内容提供审核推荐 **[!UICONTROL Network Settings > ModQ]**。

## 可在ModQ中使用的操作 {#section_h4g_wrn_z1b}

您可以决定如何处理Modq中的每个内容。

选择以下选项之一：

* 批准内容的 **[!UICONTROL Checkbox]** 图标
* 向垃圾桶发送内容的 **[!UICONTROL Trash can]** 图标
* **[!UICONTROL Request Rights]** 向内容所有者请求内容的权限。

   >[!NOTE]
   >
   >您无法请求来自Instagram的内容的ModQ权限。您必须使用库或应用程序内容向Instagram发送内容的权限请求。

* **[!UICONTROL Feature and Approve]** 来批准内容，同时也是内容的特性。
* **[!UICONTROL Product Tag and Approve]** 将产品从您的产品目录添加到内容，然后批准。
* **[!UICONTROL Mark as Pending]** 将内容标记为待定。

>[!NOTE]
>
>垃圾桶一旦粉碎，内容的片段和所有回复都会永久从ModQ中删除。要将某个垃圾碎片放入应用程序中，请参阅 [将已将项目添加回应用程序](/help/using/c-features-livefyre/c-about-moderation/t-add-trashed-item-back-into-app.md#t_add_trashed_item_back_into_app)。

如果内容已处于所需状态，则选择垃圾桶、Botzo或批准将确认状态并从列表中删除项目。审核某一内容会立即将其从队列中删除，并会将其禁用到其他审核者的队列中。

>[!NOTE]
>
>流内容可能不是Bozo'd。垃圾流内容会永久删除流内容，无法撤消。

审核内容后，它将从审核者的ModQ中删除，并且其作者无法再从流中编辑它。如果审核者取消了某项，或者用户删除了他们的注释，则该审核者将实时在其他审核者的队列中灰显。当内容灰显时，页面上会显示该 **[!UICONTROL Clear Moderated]** 按钮，允许主持人从列表中删除它，并保持其在页面上的位置，而不考虑其他审核者活动。

## 在ModQ中使用垃圾桶功能 {#section_tpx_qgz_y1b}

使用设置部分可选择标记为“已删除”的选项。

* ****[!UICONTROL Confirm Trash]**** 启用此选项可要求审核者在将内容设置为垃圾桶时确认其操作。启用此功能后，选择 **[!UICONTROL Trash]** 内容将显示一个询问请求的 **[!UICONTROL Reason for Moderation]**对话框，并提供可输入的 **[!UICONTROL Note]** 字段。

   (此设置在 **[!UICONTROL only]** 网络级别可用，并且将适用于网络下的所有站点。)

* ****[!UICONTROL Hide Replies]**** 启用此选项可在删除父注释或Botzo“d”时自动垃圾桶回复。

## 在ModQ中更改用户状态 {#section_tmw_lg1_z1b}

单击“用户摘要”面板 **[!UICONTROL User actions]** 中的按钮以将用户设为静音、停止或白名单。

* **[!UICONTROL Mute:]** 允许您将标记为列出的内容的用户设为静音。使用此选项可从审核过滤器中排除用户标记。标记标记不会因标记而输入ModQ，而且标记不会包含在旗标规则中。
* **[!UICONTROL Ban:]** 允许您从站点或网络中禁止列出的用户。(只有Studio管理员或用户经理才能通过网络禁止用户。)
* **[!UICONTROL Whitelist:]** 允许您为站点或网络列入列出的用户。(只有Studio管理员或用户经理才能将白名单列入用户名单。)



使用Modq的应用程序：

* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [注释](/help/using/c-about-apps/c-comments/c-comments.md)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Siten表示](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上传按钮](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

