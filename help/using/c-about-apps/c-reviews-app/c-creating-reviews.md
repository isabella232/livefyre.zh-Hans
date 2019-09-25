---
description: 审阅提供了各种自定义设置，允许您创建符合您的需求和品牌的审阅应用程序。
seo-description: 审阅提供了各种自定义设置，允许您创建符合您的需求和品牌的审阅应用程序。
seo-title: 创建审阅应用程序
solution: Experience Manager
title: 创建审阅应用程序
uuid: 6caefe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建审阅应用程序{#creating-a-reviews-app}

审阅提供了各种自定义设置，允许您创建符合您的需求和品牌的审阅应用程序。

通过将“审阅应用程序”自定义嵌入到您的站点中作为JS应用程序使用。 您无法在Livefyre studio中创建审阅应用程序。 要在站点上创建“审阅”应用程序，请参阅“审 [阅集成”](/help/implementation/c-app-integrations/c-reviews-integration.md)。


## 评级 {#section_hs5_c4h_21b}

评级是用户为审阅分配的数值。 每个评论都必须包括评级，默认情况下显示为5星形系统。 (当评级在应用程序中显示为0.5 - 5时，Livefyre在后端存储X/100的比率，这样一来，1星为20/100,2星为40/100。 此比率在Studio中查看审阅时显示。)

0.5到5的评级范围最高可配置为100，并且也提供了半个评级。

有关详细信息，请参阅“审阅”convConfig对象的maxRating字段。

## 评级图标样式 {#section_cqn_c4h_21b}

可以自定义评级图标以适合您的品牌和风格。

有关详细信息，请参阅“审阅自 **[!UICONTROL Configure Star Ratings]** 定义”下的内容。

## 评级维度 {#section_cnx_snh_21b}

评级维度是评级人员对产品或服务进行评级的类别。 等级维度的示例包括“性能”、“设计”、“成本”、“整体”或您选择的任何其他类别。

默认情况是显示一个“整体”评级维，但您可以定义并实现多个评级维，如下例所示。

有关详细信息，请参阅“审阅集合元数据”下的ratingDimensions字段。

## 审阅文本字段 {#section_xcm_4nh_21b}

您还可以在被审阅的产品或体验中加入其他文本字段。 （例如，文本字段可能包括“正反”或“不漏掉”。）字段的数字、标题和默认文本可自定义。 用户必须填写所有文本字段以及审阅标题、正文和评级，才能发布其审阅。 无法包含可选文本字段。

有关详细信息，请参阅“审阅集合元数据”的ratingDimensions字段。

## 审阅摘要 {#section_ysz_lnh_21b}

默认情况下，“审阅”应用程序顶部会显示摘要部分。 此部分包含“平均用户评级”和“评论集合”的“评级细分”的可视化，仅显示整数。 此部分为只读，如果需要，可隐藏。

有关详细信息，请参阅“审阅”convConfig对象的ratingSummaryEnabled字段。

## 垃圾邮件和不良信息过滤器 {#section_hcm_jnh_21b}

审阅标题和正文的文本在发布审阅后立即通过垃圾邮件过滤器和不良信息过滤器进行传递。

## 文本自定义 {#section_tjf_hnh_21b}

文本字符串（包括工具提示和标签）可能会根据语言或适合您的品牌进行自定义。

## 回复审阅 {#section_yng_fnh_21b}

用户可以在每个Reviews Collection中回复自己或其他人的Review。 只有登录的用户才能发布评论回复。

Studio中启用了用户回复审阅的选项。 所有者可以为网络、站点或集合级别切换此设置。 版主只能为其集合启用此设置。

## SocialSync和Curate {#section_llh_2nh_21b}

由于“审阅”设计为为每条已提交的内容添加一个数值，因此“审阅”不支持SocialSync和“特选”。

## 审阅API {#section_xrh_wmh_21b}

利用审阅API，您可以显示平均用户评级和评级细分信息，以及网站其他部分的用户审阅活动。

[评级和评论](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Bootstrap API端点允许Google等搜索引擎读取您的审阅，以便内容和关键字可以改进搜索引擎优化。

* **[!UICONTROL Average User Ratings]** “平均用户评级”API检索一个或多个“审阅集合”的平均用户评级，允许您在索引页面上创建此信息的可视化或添加到搜索索引页面。

* **[!UICONTROL Ratings Breakdown]** 评级细分API可检索特定评论集合的所有评级细分，并允许您创建一个可视化，显示与每个星级评级关联的评论数。

* **[!UICONTROL User Reviews]** 用户审阅API可检索特定用户的最新审阅。 此活动可用于在其公共配置文件页面上显示用户的评论。
