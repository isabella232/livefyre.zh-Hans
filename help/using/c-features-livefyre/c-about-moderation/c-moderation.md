---
description: Livefyre垃圾邮件和滥用过滤引擎(SAFE)是一个后台流程，可分析所有传入内容，并为所有Livefyre客户启用。
seo-description: Livefyre垃圾邮件和滥用过滤引擎(SAFE)是一个后台流程，可分析所有传入内容，并为所有Livefyre客户启用。
seo-title: 安全规则
title: 安全规则
uuid: 2f91d0d4-dffe-4651-88af-79bbb96c1b5c
translation-type: tm+mt
source-git-commit: 09011bac06f4a1c39836455f9d16654952184962
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 0%

---


# 安全规则{#safe-rules}

Livefyre垃圾邮件和滥用过滤引擎(SAFE)是一个后台流程，可分析所有传入内容，并为所有Livefyre客户启用。



SAFE使用模式规则和统计模型来检测垃圾邮件、滥用、亵渎和批量（重复）帖子。 您将在其他Livefyre产品中不时看到引用的内容，特别是内容协调工具和ModQ。

>[!NOTE]
>
>SAFE仅英文，批量邮寄分类除外。 如果您需要支持其他语言，请联系您的战略客户经理。

## 使用SAFE {#section_k34_4tx_vy}的Studio组件

SAFE应用的标志可用于以下Studio组件：

* 规则

   您可以定义SAFE规则，以自动标记内容并定义在&#x200B;**[!UICONTROL Network Settings]**&#x200B;中应如何处理已标记内容。

   例如，站点可能为Profanity设置非常低的容差，并定义SAFE Rules，将标记为Profane的所有内容设置为Bozo’d。其他站点可以定义规则，在进入流之前将配置文件内容预先审核。

* ModQ

   您可以在ModQ中审核由SAFE规则和其他预审核规则（例如，SPAM、profity等）标出的内容。

* 库中的应用程序内容

   由SAFE标记的内容列在&#x200B;**[!UICONTROL Library]**&#x200B;选项卡的“应用程序内容”中。 您可以按标记过滤内容以审核内容。

## 安全筛选器选项{#section_pg5_ttx_vy}

SAFE将以下标志应用于已过滤的内容，可用于从Livefyre Studio中创建规则和审核内容。

* **[!UICONTROL Profanity List]**:Profane内容(由英文关键字列表定义)，基于常用。

   亵渎过滤器根据经测试的单词列表来查找普罗文语言。 如果检测到该内容，则标记为Profane。

   >[!NOTE]
   >
   >Livefyre还提供第二个Profity列表过滤器，您可以在站点和网络级别自定义该过滤器。 使用“亵渎”列表创建的规则将优先于通过“安全亵渎”过滤器生成的自动化规则。 有关详细信息，请参阅设置文档中的“亵渎列表”部分。

* **[!UICONTROL Mild Profanity]**:在礼貌的谈话中，词和短语通常不可接受，但在非正式的谈话中通常可以接受。通常，网络电视上允许使用这些词和短语。
* **[!UICONTROL Strong Profanity]**:非常强的语言，如网络电视上不允许使用的词语和短语，在R级电影和成熟的有线电视节目中也很少使用。通常，这些词不会用在礼貌或随意的谈话中，在不礼貌的谈话中被说出来，意在伤害听众。
* **[!UICONTROL SPAM]**:主动提供的、通常是商业内容。它使用一种统计模型，该模型依赖于各种功能（包括注释内容和URL）来将某个内容标记为SPAM。 您可以根据请求调整垃圾邮件阈值以自定义网络或站点的垃圾邮件标记率。
* **[!UICONTROL Mild Insult]**:侮辱性内容，由关键字和短语模式列表定义。
* **[!UICONTROL Strong Insult]**:侮辱性内容，由关键字和短语模式列表定义。
* **[!UICONTROL Hate Speech]**:基于种族或宗教的侮辱，特别是当目标组属于少数或受保护时。
* **[!UICONTROL ALL CAPS]**:以所有大写字母呈现的文本（如喊叫）。
* **[!UICONTROL Mild Threat]**:一种威胁或侮辱，通常包括针对他人的某种轻微的亵渎。此选项会更频繁地标记可能的威胁，但假阳性率也高于&#x200B;**[!UICONTROL Strong Threat]**。

* **[!UICONTROL Strong Threat]**:一种严重的威胁或侮辱，它提到对一个或多个人的可行人身伤害，而且通常带有强烈的亵渎。此选项标记可能的威胁的频率较低，但误报率也低于&#x200B;**[!UICONTROL Mild Threat]**。

* **[!UICONTROL Probable Nudity]**:可能有裸体的图像。此选项标记裸度的频率较低，但假阳性率也低于&#x200B;**[!UICONTROL Possible Nudity]**。

* **[!UICONTROL Possible Nudity]**:可能有裸体的图像。此选项更常标记裸度，但假阳性率也比&#x200B;**[!UICONTROL Probable Nudity]**&#x200B;高。

* **[!UICONTROL PII]** （个人身份信息）:可识别用户的信息。这可以包括电子邮件地址、实际地址、社会保险号码（针对美国客户）、信用卡号、密码，或任何可用于欺诈或获取某人身份的信息。
* **[!UICONTROL Livefyre Recommends Trash]**。设置系统在自动协调推荐识别要拒绝的内容时执行的操作。 ![](assets/mod_reco1.png)

   >[!NOTE]
   >
   >要打开“协调Recommendations”，请与AdobeLivefyre支持专业人员联系。

## 处理SAFE {#section_pjy_5tx_vy}未捕获的内容

有几种方法可以有效处理此过滤器未捕获的内容。 以下选项按建议的处理顺序列出。

1. 作为审查方，从流中删除内容。
1. 创建一个标志规则，如果5个用户将某条内容标记为“垃圾邮件”或“冒犯性”，则将其设置为Bozo。
1. 禁止发布不需要内容的用户，因此其所有内容将直接进入Bozo状态。
1. 添加应始终筛选到的特定单词，使其显示您的脏话列表。

>[!NOTE]
>
>如果审查方发布了被我们的垃圾邮件过滤器捕获的内容，该内容仍被标为垃圾邮件，但是自动被批准，并且不会设置为Bozo。

如果您注意到SAFE未捕获的内容趋势或模式，请用评论ID和文本向客户经理发送电子邮件。



使用此功能的应用程序：

* [轮播](/help/using/c-about-apps/c-carousel-app/c-carousel-app.md#c_carousel_app)
* [聊天](/help/using/c-about-apps/c-chat-app/c-chat-app.md#c_chat_app)
* [评论](/help/using/c-about-apps/c-comments/c-comments.md)
* [功能卡](/help/using/c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)
* [地图](/help/using/c-about-apps/c-map-app/c-map-app.md#c_map_app)
* [媒体墙](/help/using/c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)
* [马赛克](/help/using/c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)
* [评论](/help/using/c-about-apps/c-reviews-app/c-reviews-app.md#c_reviews_app)
* [Sidesk](/help/using/c-about-apps/c-sidenotes-app/c-sidenotes-app.md#c_sidenotes_app)
* [Storify 2](/help/using/c-about-apps/c-storify2/c-storify2.md#c_storify2)
* [上传按钮](/help/using/c-about-apps/c-upload-button-app/c-upload-button-app.md#c_upload_button_app)

