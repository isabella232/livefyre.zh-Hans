---
description: 审阅优惠多种自定义设置，允许您创建符合您的需求和品牌的审阅应用程序。
title: 创建审阅应用程序
exl-id: 14f074d2-922c-4997-8d7d-f2c92f069e07
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 0%

---

# 创建评论应用程序{#creating-a-reviews-app}

审阅优惠多种自定义设置，允许您创建符合您的需求和品牌的审阅应用程序。

通过自定义将审阅应用程序作为JS应用程序嵌入您的站点，使用它。 无法在Livefyre Studio中创建评论应用程序。 要在您的站点上创建“审阅”应用程序，请参阅[“审阅集成”](/help/implementation/c-app-integrations/c-reviews-integration.md)。


## 评级{#section_hs5_c4h_21b}

评级是用户分配给评论的数值。 每个评论都必须包含一个评级，默认情况下显示为5星系系统。 (当评级在应用程序中显示为0.5 - 5时，Livefyre在后端存储X/100的比率，这样一来，1星为20/100,2星为40/100。 在Studio中查看审阅时，将显示此比率。)

0.5到5的评级范围可配置为最高100的评级，同时也提供半级评级。

有关详细信息，请参阅“审阅”convConfig对象的maxRating字段。

## 等级图标样式{#section_cqn_c4h_21b}

可以自定义评级图标以适合您的品牌和风格。

有关详细信息，请参阅“审阅自定义”下的&#x200B;**[!UICONTROL Configure Star Ratings]**。

## 评级Dimension{#section_cnx_snh_21b}

评级维度是类别，您的审阅者对您的产品或服务进行评级。 评级维度的示例包括“性能”、“设计”、“成本”、“整体”或您选择的任何其他类别。

默认为显示一个“整体”评级维度，但您可以定义并实施多个评级维度，如下例所示。

有关详细信息，请参阅“审阅集合元数据”下的ratingDimensions字段。

## 查看文本字段{#section_xcm_4nh_21b}

您还可以在正在审阅的产品或体验中包含其他文本字段。 （例如，文本字段可能包括“正面和反面”或“不要失败”。） 字段的数字、标题和默认文本均可自定义。 用户需要填写所有文本字段以及审阅标题、正文和评级，才能发布其审阅。 无法包含可选文本字段。

有关详细信息，请参阅“审阅集合元数据”的ratingDimensions字段。

## 查看摘要{#section_ysz_lnh_21b}

默认情况下，“审阅”应用程序顶部会显示摘要部分。 此部分包含“评论集合”的“平均用户评级”和“评级划分”的可视化，仅显示整个数字。 此部分是只读的，如果需要，可隐藏。

有关详细信息，请参阅“审阅”convConfig对象的ratingSummaryEnabled字段。

## 垃圾邮件和亵渎过滤器{#section_hcm_jnh_21b}

审阅的标题和正文文本在发布审阅后立即通过垃圾邮件过滤器和不当过滤器进行传递。

## 文本自定义{#section_tjf_hnh_21b}

可以根据语言自定义文本字符串，包括工具提示和标签。

## 回复评论{#section_yng_fnh_21b}

用户可以在每个审阅集合中回复自己或他人的审阅。 只有登录的用户才能发布评论回复。

Studio中启用了用户回复审阅的选项。 所有者可以为网络、站点或集合级别切换此设置。 版主只能为其集合启用此设置。

## SocialSync和Curate {#section_llh_2nh_21b}

由于“审阅”设计为为每个提交的内容添加一个数值，因此“审阅”不支持SocialSync和“策略”。

## 查看API {#section_xrh_wmh_21b}

利用审阅API，您可以在网站的其他部分显示平均用户评级和评级划分信息以及用户审阅活动。

[评级和评论](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** Bootstrap API端点允许搜索引擎（如Google）读取您的审阅，以便内容和关键字可以改进搜索引擎优化。

* **[!UICONTROL Average User Ratings]** “平均用户评级”API检索一个或多个评论集合的平均用户评级，允许您在索引页面上创建此信息的可视化或添加到搜索索引页面。

* **[!UICONTROL Ratings Breakdown]** 评级划分API可检索特定评论集合的所有评级的划分，并允许您创建一个可视化，显示与每个星级评级关联的评论数。

* **[!UICONTROL User Reviews]** “用户审阅”API检索特定用户的最新审阅。此活动可用于在用户的公共用户档案页面上显示用户的评论。
