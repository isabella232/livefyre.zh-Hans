---
description: 审阅优惠各种自定义设置，允许您创建符合您的需求和品牌的审阅应用程序。
seo-description: 审阅优惠各种自定义设置，允许您创建符合您的需求和品牌的审阅应用程序。
seo-title: 创建评论应用程序
solution: Experience Manager
title: 创建评论应用程序
uuid: 6caeafe7-c04e-484e-b02f-98dc6d9b3184
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---


# 创建评论应用程序{#creating-a-reviews-app}

审阅优惠各种自定义设置，允许您创建符合您的需求和品牌的审阅应用程序。

通过将“审阅应用程序”自定义嵌入到您的站点中作为JS应用程序使用。 无法在Livefyre Studio中创建评论应用程序。 要在您的站点上创建评论应用程序，请参阅[评论集成](/help/implementation/c-app-integrations/c-reviews-integration.md)。


## 评级{#section_hs5_c4h_21b}

评级是用户分配给评论的数值。 每个评论都必须包括评级，默认情况下显示为5星形系统。 (当评级在应用程序中显示为0.5 - 5时，Livefyre在后端存储X/100的比率，这样1星为20/100,2星为40/100。 此比率在Studio中查看审阅时显示。)

0.5到5的评级范围可配置为最高100的评级，也提供半个评级。

有关详细信息，请参阅“审阅”convConfig对象的maxRating字段。

## 等级图标样式{#section_cqn_c4h_21b}

可以自定义评级图标以适合您的品牌和风格。

有关详细信息，请参阅“审阅自定义”下的&#x200B;**[!UICONTROL Configure Star Ratings]**。

## 评级Dimension{#section_cnx_snh_21b}

评级维度是类别，您的审阅者对您的产品或服务进行评级。 评级维度的示例包括“性能”、“设计”、“成本”、“整体”或您选择的任何其他类别。

默认值是显示一个“整体”评级维，但您可以定义并实施多个评级维，如以下示例所示。

有关详细信息，请参阅审核集合元数据下的ratingDimensions字段。

## 查看文本字段{#section_xcm_4nh_21b}

您还可以在被审阅的产品或体验中加入其他文本字段。 （例如，文本字段可能包括“优势和缺点”或“不漏掉”。） 字段的数字、标题和默认文本可自定义。 用户必须填写所有文本字段以及审阅标题、正文和评级，才能发布其审阅。 无法包含可选文本字段。

有关详细信息，请参阅“审阅集合元数据”的ratingDimensions字段。

## 查看摘要{#section_ysz_lnh_21b}

默认情况下，审阅应用程序顶部会显示摘要部分。 此部分包含“Average User Rating”（平均用户评级）和“Reviews Collection”（评论集合）的“Rating Breakfon”（评级细分）的可视化，仅显示完整数字。 此部分是只读的，如果需要，可以隐藏。

有关详细信息，请参阅“审阅”convConfig对象的ratingSummaryEnabled字段。

## 垃圾邮件和不良信息过滤器{#section_hcm_jnh_21b}

审阅的标题和正文文本在发布审阅后立即通过垃圾邮件过滤器和亵渎过滤器进行传递。

## 文本自定义{#section_tjf_hnh_21b}

文本字符串（包括工具提示和标签）可能会根据语言进行自定义或适合您的品牌。

## 回复评论{#section_yng_fnh_21b}

用户可以在每个评论集合中回复他们自己或其他人的评论。 只有登录的用户才能发布评论回复。

Studio中启用了用户回复评论的选项。 所有者可以为网络、站点或集合级别切换此设置。 版主只能为其集合启用此设置。

## SocialSync和Curate {#section_llh_2nh_21b}

由于“审阅”设计为为每个提交的内容添加一个数值，因此“审阅”不支持SocialSync和Curate。

## 查看API {#section_xrh_wmh_21b}

利用审阅API，您可以在网站的其他部分显示平均用户评级和评级细分信息以及用户审阅活动。

[评级和评论](https://api.livefyre.com/docs/apis/by-category/ratings-and-reviews)

* **[!UICONTROL Bootstrap API Endpoint]** BootstrapAPI端点允许搜索引擎（如Google）读取您的审阅，以便内容和关键字能够改进搜索引擎优化。

* **[!UICONTROL Average User Ratings]** “平均用户评级”API检索一个或多个评论集合的平均用户评级，允许您在索引页面上创建此信息的可视化或添加到搜索索引页面。

* **[!UICONTROL Ratings Breakdown]** 评级细分API检索特定评论集合的所有评级的细分，并允许您创建一个可视化，显示与每个星级评级关联的评论数。

* **[!UICONTROL User Reviews]** 用户审阅API检索特定用户的最新审阅。此活动可用于在其公共用户档案页面上显示用户的评论。
