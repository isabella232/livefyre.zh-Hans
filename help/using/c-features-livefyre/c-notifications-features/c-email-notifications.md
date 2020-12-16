---
description: 允许用户选择其通知频率和内容。
seo-description: 允许用户选择其通知频率和内容。
seo-title: 电子邮件通知
solution: Experience Manager
title: 电子邮件通知
uuid: 27dad133-bd8d-4949-8146-1254c160d3af
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '951'
ht-degree: 1%

---


# 电子邮件通知{#email-notifications}

允许用户选择其通知频率和内容。

**为用户和版主启用电子邮件通知。**

Livefyre应用程序允许您根据特定操作为用户和版主启用电子邮件通知。 通知基于内容发布到流的时间，允许用户继续参与他们关心的对话，并在某人喜欢或回复其某个评论时获得通知。

用户和版主选择加入可以发送或发出电子邮件通知，并可以设置接收电子邮件的频率。 本节介绍如何配置和自定义这些电子邮件通知。

* 用户电子邮件选项：可用的用户通知选项。
* 审查方电子邮件选项：可用的版主通知选项。
* Livefyre标识电子邮件选项：作为Livefyre Identity的一部分发送的电子邮件。 这些电子邮件仅与Livefyre Identity客户相关。
* 与Livefyre同步数据：维护首选项与Livefyre同步。
* 自定义电子邮件：可用的电子邮件自定义。

使用&#x200B;**设置>集成设置>电子邮件通知设置**&#x200B;选项为网络自定义电子邮件通知。

>[!NOTE]
>
>为确保最终用户不会收到意外的邮件，不会从Livefyre UAT环境发送电子邮件通知。

**用户电子邮件选项**

Livefyre允许用户接收网站活动的电子邮件通知。 使用Livefyre提供的用户用户档案集成设置，允许用户选择其通知计划首选项。

>[!NOTE]
>
>电子邮件仅针对手动发布到流中的内容发送，而不针对从SocialSync提取的内容发送。

要允许用户设置其通知首选项，请在用户用户档案系统的“用户设置”中加入“电子邮件通知”部分。 将相应的字段添加到用户用户档案库模式，然后使用Ping for Pull管理用户设置。 (与Technical Integration Manager一起定义网络的默认频率。 如果您是企业用户档案客户，请将选定的默认值传递给Livefyre投放团队，以便在Livefyre库中进行配置。)

然后，您站点上的用户可以关注对话，并通过单击评论编辑器上的&#x200B;**[!UICONTROL +Follow]**&#x200B;按钮开始接收电子邮件通知。 通知首选项在Livefyre网络级别定义。 任何用户设置都将应用于整个网络中的所有站点和对话。

**建议的默认值**

* 我在对话中有人评论：**每小时摘要**
* 有人喜欢我的评论：**每小时摘要**
* 有人回复了我的一条评论：**立即**
* 在我留下评论时自动跟踪对话：**关闭**（未选中）

**注意**:电子邮件通知基于批准将内容包含在流中的时间。

Livefyre优惠了两个电子邮件频率选项：

* 立即
* 每小时摘要

**立即**

发送的电子邮件会立即显示帖子的文本、文章标题、作者的用户名以及将用户带到页面上的内容的&#x200B;**回复**&#x200B;链接。 这些电子邮件还在页脚中包含一个&#x200B;**取消订阅**&#x200B;链接，允许用户取消订阅该集合的电子邮件通知。 单击**取消订阅**将带他们进入确认页，以告知他们已取消订阅集合。

**每小时摘要**

以每小时的摘要发送的电子邮件按用户正在关注的每个应用程序显示最后一小时（或更近）内内容上的所有内容、对内容的回复和喜欢。 如果用户在您的网络中关注多个应用程序，则他们将收到每个应用程序的一封摘要电子邮件。

>[!NOTE]
>
>在没有新内容的会话中，启用每小时摘要的用户会在新内容发布后立即收到通知。

**审查方电子邮件选项**

版主可选择加入以接收他们正在关注的应用程序中发布的内容以及正在审核的应用程序中标记为“垃圾邮件”或“冒犯性”的评论的电子邮件。 **注意：** 当用户标记有“反对”或“非主题”评论时，不会发送任何电子邮件，因为这些类别对于审查方通知不重要。

还应将审查方用户用户档案设置页模式库添加审查方注释和审查方标志字段，以允许审查方更新其电子邮件通知的频率，如选择退出果他们愿意。 Livefyre建议您将这两个审查方电子邮件通知字段设置为&#x200B;**never**。 选项包括&#x200B;**never**（默认）、**immedialy**&#x200B;和&#x200B;**通常**。

**审查方电子邮件（标记内容）:**

当内容在审核的应用程序中标出时，发送给审查方的电子邮件将显示已标出的内容、标出内容的用户名以及返回内容页面的链接。

当用户在用户档案系统中更改您站点上的电子邮件通知首选项时，使用Livefyre的Ping for Pull将更新同步到Livefyre远程用户档案系统。

**与Livefyre同步数据**

## 自定义电子邮件{#section_jxb_c5k_yy}

电子邮件通知模板中的多个字段可能会更改以适合您的风格和品牌。

* **[!UICONTROL From Email Address]**

   所有电子邮件通知的“发件人电子邮件地址”可进行自定义，以与您的品牌保持一致。 Livefyre建议&#x200B;**noreply@customerdomain.com**，用您的域名替换&#x200B;**customerdomain**。 (默认值为&#x200B;**noreply@livefyre.com**。) 请将首选“从电子邮件地址”传递到Technical Integration Manager，以便在网络的Livefyre数据库中进行配置。

   >[!NOTE]
   >
   >此字段留空可禁用网络的电子邮件通知

* **[!UICONTROL Email Logo]**

   使用Studio的&#x200B;**“网络设置”**&#x200B;页面的“品牌”选项卡，可以自定义电子邮件通知中显示的标志，以显示您的公司标志，而不是默认的Livefyre标志。 此自定义仅在网络级别可用，而不在站点级别可用，并且仅对付费Livefyre客户可用。

* **[!UICONTROL Custom Templates]**

   您可以根据需要实施完全自定义的电子邮件模板。 但是，这需要一些开发工作，并可能产生专业服务成本。 有关详细信息，请联系您的客户经理。



使用此功能的应用程序：

* [轮播](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)

