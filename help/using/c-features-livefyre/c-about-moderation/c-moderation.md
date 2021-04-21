---
description: Livefyre垃圾邮件和滥用过滤引擎(SAFE)是一个分析所有传入内容的后台过程，为所有Livefyre客户启用。
title: 安全规则
exl-id: 13cd8df0-c4b7-436e-ba07-64ec67321d6b
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# 安全规则{#safe-rules}

Livefyre垃圾邮件和滥用过滤引擎(SAFE)是一个分析所有传入内容的后台过程，为所有Livefyre客户启用。



SAFE使用模式规则和统计模型来检测垃圾邮件、滥用、亵渎和批量（重复）帖子。 您会在其他Livefyre产品（尤其是内容审核工具和ModQ）中看到它时时不时地引用。

>[!NOTE]
>
>SAFE仅英文，但批量邮件分类除外。 如果您需要其他语言的支持，请联系您的战略客户经理。

## 使用SAFE {#section_k34_4tx_vy}的Studio组件

SAFE应用的标志可用于以下Studio组件：

* 规则

   您可以定义SAFE规则，以自动标记内容并定义在&#x200B;**[!UICONTROL Network Settings]**&#x200B;中应如何处理已标记的内容。

   例如，站点可能为Profanity设置非常低的容差，并定义SAFE规则，将标记为Profane的所有内容设置为Bozo&#39;d。其他站点可能会定义规则，在进入流之前将Profane内容设置为预审核。

* ModQ

   您可以在ModQ中审核由SAFE规则和其他预审核规则（例如，SPAM、亵渎等）标出的内容。

* 库中的应用程序内容

   由SAFE标记的内容列在&#x200B;**[!UICONTROL Library]**&#x200B;选项卡的“App Content”（应用程序内容）中。 您可以按标记筛选内容以审核内容。

## 安全筛选器选项{#section_pg5_ttx_vy}

SAFE将以下标志应用于筛选的内容，并可用于从Livefyre Studio中创建规则和审核内容。

* **[!UICONTROL Profanity List]**:基于常见用法，由英文关键字列表定义的Profane内容。

   “亵渎过滤器”根据经测试的单词列表来查找亵渎语言。 如果检测到该内容，则将标记为Profane。

   >[!NOTE]
   >
   >Livefyre还提供了第二个“配置列表”过滤器，您可以在站点和网络级别对其进行自定义。 使用“亵渎”列表创建的规则将优先于使用“安全亵渎”过滤器生成的自动化规则。 有关详细信息，请参阅设置文档中的“亵渎列表”部分。

* **[!UICONTROL Mild Profanity]**:在礼貌的谈话中，通常不接受词语和短语，但在闲聊中通常可以接受。通常，网络电视上允许使用这些词语和短语。
* **[!UICONTROL Strong Profanity]**:非常强的语言，例如网络电视上不允许使用的词汇和短语，在R级电影和成熟的有线电视节目中很少使用。通常，这些词不会用在礼貌或随意的交谈中，而是在不礼貌的交谈中说出来，意在伤害听众。
* **[!UICONTROL SPAM]**:主动提供的，通常是商业内容。它使用一种统计模型，该模型依赖于各种功能（包括评论内容和URL）来将某条内容标记为SPAM。 您可以根据请求调整垃圾邮件阈值以自定义网络或站点的垃圾邮件标记率。
* **[!UICONTROL Mild Insult]**:侮辱性内容，由关键字和短语模式列表定义。
* **[!UICONTROL Strong Insult]**:侮辱性内容，由关键字和短语模式列表定义。
* **[!UICONTROL Hate Speech]**:基于种族或宗教的侮辱，特别是当目标组属于少数或受保护时。
* **[!UICONTROL ALL CAPS]**:以所有大写字母（读作喊叫）呈现的文本。
* **[!UICONTROL Mild Threat]**:一种威胁或侮辱，通常包括针对他人的轻度亵渎。此选项标记可能的威胁的频率更高，但误报率也高于&#x200B;**[!UICONTROL Strong Threat]**。

* **[!UICONTROL Strong Threat]**:一种严重的威胁或侮辱，它提到对一个或多个人具有可行的身体伤害，而且往往带有严重的亵渎。此选项标记可能的威胁的频率较低，但误报率也低于&#x200B;**[!UICONTROL Mild Threat]**。

* **[!UICONTROL Probable Nudity]**:可能包含裸体的图像。此选项标记裸体的频率较低，但假阳性率也低于&#x200B;**[!UICONTROL Possible Nudity]**。

* **[!UICONTROL Possible Nudity]**:可能包含裸体的图像。此选项会更频繁地标记裸体，但假阳性率也高于&#x200B;**[!UICONTROL Probable Nudity]**。

* **[!UICONTROL PII]** （个人识别信息）：可识别用户的信息。这可能包括电子邮件地址、实际地址、社会保险号（针对美国客户）、信用卡号、密码，或任何可用于欺诈或获取他人身份的信息。
* **[!UICONTROL Livefyre Recommends Trash]**。设置系统在自动审核推荐确定要拒绝的内容时执行的操作。 ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >要打开“审核Recommendations”，请与您的Adobe Livefyre支持专业人员联系。

## 处理SAFE {#section_pjy_5tx_vy}未捕获的内容

有几种方法可用于有效处理未被此过滤器捕获的内容。 以下选项按建议的处理顺序列出。

1. 作为审查方，从流中删除内容。
1. 创建一个标志规则，该规则规定如果某条内容被5个用户标记为“垃圾邮件”或“冒犯性”，则将其设置为Bozo。
1. 禁止发布不需要内容的用户，因此其所有内容将直接进入Bozo状态。
1. 添加应始终筛选到的特定词语，使其成为您的脏话列表。

>[!NOTE]
>
>如果审查方发布了被我们的垃圾邮件过滤器捕获的内容，则该内容仍被标记为垃圾邮件，但是自动被批准，并且不会设置为Bozo。

如果您注意到SAFE未捕获到的内容趋势或模式，请用评论ID和文本向您的客户经理发送电子邮件。



使用此功能的应用程序：

* [轮播](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地图](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [马赛克](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Siestr](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上传按钮](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)
