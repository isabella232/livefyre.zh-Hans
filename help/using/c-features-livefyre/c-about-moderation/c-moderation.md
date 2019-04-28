---
description: Livefyre垃圾邮件和滥用过滤引擎(Safe)是一个后台流程，它分析所有传入的内容，并为所有Livefyre客户启用。
seo-description: Livefyre垃圾邮件和滥用过滤引擎(Safe)是一个后台流程，它分析所有传入的内容，并为所有Livefyre客户启用。
seo-title: 安全规则
title: 安全规则
uuid: 2f91d0d4-dffe-4651-88af-79bbb96 c1 b5 c
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962

---


# 安全规则{#safe-rules}

Livefyre垃圾邮件和滥用过滤引擎(Safe)是一个后台流程，它分析所有传入的内容，并为所有Livefyre客户启用。



SAFE使用模式规则以及统计模型检测垃圾邮件、滥用、亵渎和批量(重复)帖子。您会在其他Livefyre产品(尤其是内容协调工具和Modq)中经常看到它。

>[!NOTE]
>
>SAFE仅为英语，除批量邮寄分类外。如果您需要对其他语言的支持，请联系您的战略客户经理。

## 使用Safe的Studio组件 {#section_k34_4tx_vy}

SAFE应用的标记可与以下Studio组件一起使用：

* 规则

   您可以定义安全规则以自动标记内容并定义标记内容应如何处理 **[!UICONTROL Network Settings]**。

   例如，站点可能为亵渎设置非常低的容差，并定义安全规则，将所有标记为Proane的内容都设置为Bozo&#39;d。其他站点可能定义在进入流之前将Proane内容设置为预先审核的规则。

* Modq

   您可以在Modq中审核由SAFE规则标记的内容，以及其他预先审核规则(例如SPAM、亵渎等)。

* 库中的应用程序内容

   SAFE标记的内容会列在 **[!UICONTROL Library]** 选项卡中的应用程序内容中。您可以通过标记筛选内容以审核内容。

## 安全过滤器选项 {#section_pg5_ttx_vy}

SAFE将以下标记应用于筛选内容，可用于在Livefyre Studio中创建规则和审核内容。

* **[!UICONTROL Profanity List]**：Proane内容，由英语关键字列表根据共同使用而定。

   “亵渎过滤器”根据经过测试的单词列表查找亵渎语言。如果检测到内容，则内容标记为Proane。

   >[!NOTE]
   >
   >Livefyre还提供第二个“亵渎列表”过滤器，您可以在站点和网络级别进行自定义。使用“亵渎列表”创建的规则优先于来自SAFE亵渎过滤器的自动化规则。有关详细信息，请参阅设置文档中的“亵渎列表”部分。

* **[!UICONTROL Mild Profanity]**：通常不可接受的词语和短语，但通常以级联对话接受。通常，网络电视允许这些词语和短语。
* **[!UICONTROL Strong Profanity]**：非常强大的语言，如不允许在网络电视上使用的词汇和短语，并且在R分级电影和成熟的有线电视节目中很少使用。一般来说，这些词语不用在粗体或不经意对话中，而且被认为是有意伤害监听器的目的。
* **[!UICONTROL SPAM]**：主动提供的商业内容。它使用的统计模型依赖各种功能(包括注释内容和URL)将一条内容标记为SPAM。您可以根据请求调整垃圾信息阈值以自定义网络或站点的SPM标记费率。
* **[!UICONTROL Mild Insult]**：对内容进行隔离，由关键字和短语模式列表定义。
* **[!UICONTROL Strong Insult]**：对内容进行隔离，由关键字和短语模式列表定义。
* **[!UICONTROL Hate Speech]**：基于性或宗教的侮辱，尤其是当目标组从属关系是少数或受保护时。
* **[!UICONTROL ALL CAPS]**：以大写字母形式呈现的文本(朗读)。
* **[!UICONTROL Mild Threat]**：威胁或侮辱，通常包括面向他人的轻微亵渎。此选项会更频繁地标记可能的威胁，但速度高于 **[!UICONTROL Strong Threat]**时。

* **[!UICONTROL Strong Threat]**：严重威胁一人或多人的严重威胁或侮辱，通常具有强烈的亵渎性。此选项标记可能的威胁更少，但会比错误的正负速率更低 **[!UICONTROL Mild Threat]**。

* **[!UICONTROL Probable Nudity]**：其中可能蕴含ness的图像。此选项不太频繁地标记nounity **[!UICONTROL Possible Nudity]**，但速度较低。

* **[!UICONTROL Possible Nudity]**：其中可能蕴含ness的图像。此选项更频繁地标记nudity，但 **[!UICONTROL Probable Nudity]**速度高于false-正值。

* **[!UICONTROL PII]** (个人可识别信息)：可识别用户的信息。这可能包括电子邮件地址、实际地址、社会保险号(对于美国客户)、信用卡号码、密码或可用于欺诈或获取某人身份的任何内容。
* **[!UICONTROL Livefyre Recommends Trash]**. 设置当自动协调推荐识别内容以拒绝时系统执行的操作。 ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >要开启仲裁推荐，请与您的Adobe Livefyre支持专业人员联系。

## 处理未通过SAFE捕获的内容 {#section_pjy_5tx_vy}

有几种方法可有效处理此过滤器未捕获的内容。以下选项按建议的流程顺序列出。

1. 作为主持人，从流中删除内容。
1. 创建“旗标规则”，该规则表示如果一段内容被五个用户标记为垃圾信息或攻击，则将其设置为Bozo。
1. 禁止发布不需要内容的用户，使其所有内容直接进入Bozo状态。
1. 添加应始终过滤到您的亵渎列表的特定词语。

>[!NOTE]
>
>如果审核者发布的内容被我们的垃圾邮件过滤器捕获，它仍被标记为垃圾邮件，但会自动批准，不会被设置为Bozo。

如果您注意到SAFE未捕获的内容的趋势或模式，请通过注释ID和文本电子邮件发送您的CSMS。



使用此功能的应用程序：

* [Carousel](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [注释](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地图](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [Mosaic](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Siten表示](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上传按钮](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

