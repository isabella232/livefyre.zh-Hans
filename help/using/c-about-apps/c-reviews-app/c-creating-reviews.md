---
description: 审阅提供了各种自定义功能，允许您创建符合需求和品牌的审阅应用程序。
seo-description: 审阅提供了各种自定义功能，允许您创建符合需求和品牌的审阅应用程序。
seo-title: 创建评论应用程序
solution: Experience Manager
title: 创建评论应用程序
uuid: 6Caeafe7-c04 e-484e-b02 f-98dc6 d9 b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 创建评论应用程序{#creating-a-reviews-app}

审阅提供了各种自定义功能，允许您创建符合需求和品牌的审阅应用程序。

通过将评论应用程序作为JS应用程序进行自定义嵌入，使用评论应用程序。无法在Livefyre Studio中创建评论应用程序。要在站点上创建评论应用程序，请参阅 [审阅集成](/help/implementation/c-app-integrations/c-reviews-integration.md)。


## 评级 {#section_hs5_c4h_21b}

评级是用户分配给审阅的数值。每个审阅都必须包含一个评级，默认情况下显示为个星形系统。(尽管评级在应用程序中显示为0.5-5，但Livefyre在后端存储X/100的比率，这样个星形就是20/100，星为40/100。在Studio中查看评论时，会显示此比率。)

0.5至5的评级范围最多可配置为100，也可使用一半评级。

有关详细信息，请参阅Reviews Overtionfig对象的MaxRating字段。

## 评级图标样式 {#section_cqn_c4h_21b}

可自定义评分图标以适合您的品牌和风格。

有关详细信息，请参阅 **[!UICONTROL Configure Star Ratings]** 评论自定义。

## 评级维度 {#section_cnx_snh_21b}

等级维度是评测者对产品或服务评级的类别。评级维度的示例包括“性能”、“设计”、“费用”、“整体”或您选择的任何其他类别。

默认值是显示一个“整体”评级维度，但是您可以定义并实施多个评级维度，如下面的示例所示。

有关详细信息，请参阅“审阅集合元数据”下的RatingDimensions字段。

## 审阅文本字段 {#section_xcm_4nh_21b}

您还可以在查看的产品或体验中包含其他文本字段。(例如，文本字段可能包括专业人员和Cons，或者不是小姐。)字段的编号、标题和默认文本可自定义。用户将需要填写所有文本字段，以及审核标题、正文和评级，以便发布审阅。不可能包含可选文本字段。

有关详细信息，请参阅“审核集合元数据”的RatingDimensions字段。

## 审阅摘要 {#section_ysz_lnh_21b}

默认情况下，摘要部分显示在评论应用程序的顶部。本节包含Reviews Collection的平均用户评级和评级划分可视化，仅显示整数。此部分是只读的，可以在需要时隐藏。

有关详细信息，请参阅Reviews OrdConfig对象的RatingSummaryEnabled字段。

## 垃圾信息和亵渎滤镜 {#section_hcm_jnh_21b}

评论张贴后，将通过我们的垃圾邮件过滤器和亵渎过滤器传递审阅标题和正文的文本。

## 文本自定义 {#section_tjf_hnh_21b}

文本字符串(包括工具提示和标签)可针对语言进行自定义或适合您的品牌。

## 回复评论 {#section_yng_fnh_21b}

用户可以在每个审阅集合中回复自己或其他人的审阅。只有登录的用户才能回复评论。

Studio中启用了用户回复评论的选项。所有者可以为网络、站点或集合级别切换此设置。审核者只能为其集合启用此设置。

## Search Sync和Curate {#section_llh_2nh_21b}

由于审阅旨在为每条提交内容添加一个数字值，因此审阅不支持“异步同步”和“特写”。

## 评论API {#section_xrh_wmh_21b}

评论API可用于显示平均用户评分和等级细分信息，并且用户可查看网站上其他部分的活动。

[评级和评论](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Bootstrap API端点可让您的审阅由Google等搜索引擎读取，这样内容和关键字就可以改进搜索引擎优化。

* **[!UICONTROL Average User Ratings]** 平均用户评级API检索一个或多个评论集合的平均用户等级，允许您在索引页面上创建此信息的可视化，或添加到搜索索引页面。

* **[!UICONTROL Ratings Breakdown]** 评级细分API检索特定Reviews Collection的所有评级的划分，并允许您创建一个可视化以显示与每个星级评级关联的审阅数。

* **[!UICONTROL User Reviews]** 用户评论API检索特定用户的最新评论。此活动可用于在其公共配置文件页面上显示用户的评论。
