---
description: 在客户旅程的特定点提供特定于产品的UGC，以使用UGC商务功能增加购买意图和转化率。
seo-description: 在客户旅程的特定点提供特定于产品的UGC，以使用UGC商务功能增加购买意图和转化率。
seo-title: UGC商务
solution: Experience Manager
title: UGC商务
uuid: 71e64901-a2b6-4957-ba88-058e4eaca537
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# UGC商务{#ugc-commerce}

在客户旅程的特定点提供特定于产品的UGC，以使用UGC商务功能增加购买意图和转化率。

使用UGC商务功能可影响UGC和产品详细信息页面上的购买意图和转换。 通过将UGC与产品库存无缝地关联，缩短上市时间。 通过使用UGC创建社区来突出真实的客户案例，建立品牌忠诚度。

AEM Livefyre提供了多种导入产品目录信息的方法，包括SKU、缩略图、价格和产品名称。 使用AEM Livefyre的权限请求、自动流规则标记和协调工作流轻松管理产品与UGC的关联。

除了影响购买，AEM Livefyre的UGC商务产品中的功能还可以通过以下方式促进转化率：

* B2B潜在客户生成：在UGC下放置行动动员按钮以捕获潜在客户
* B2C应用程序下载：提示用户下载应用程序
* 文章引用：将用户链接到与UGC部分相关的文章

将产品行动动员与UGC一起放置，以推动转化。 您可以：

* 将特定于产品的UGC大规模添加到数千个产品详细信息页面。
* 将AEM Livefyre的可视化应用程序嵌入到产品详细信息页面上，这些应用程序支持UGC商务功能，如Media Wall和Mosaic。
* 将可配置的引用跟踪代码与分析解决方案结合使用，以测量放置在UGC上的产品CTA和放置在产品详细信息页面上的UGC的转化率。

AEM Commerce用户可以将他们的现有产品目录无缝集成到Livefyre中，以推动用户参与Livefyre的可视化应用程序。 不使用AEM Commerce的Livefyre用户可以手动将其产品目录导入Livefyre。 有关 [更多信息，请参阅使用文件上传将产品上传到Livefyre](/help/using/c-features-livefyre/c-ugc-commerce.md)。

使用此功能的应用程序：

* [功能卡](../c-about-apps/c-feature-card-app/c-feature-card-app.md#c_feature_card_app)。 有关如何在功能卡中使用UGC商务的信息，请参阅功 [能卡自定义](../c-about-apps/c-feature-card-app/c-feature-card-app.md#section_uds_gzm_5y)。

* [](../c-about-apps/c-filmstrip-app/c-filmstrip-app.md#concept_jpc_n2j_jbb). 有关如何在幻灯片中使用UGC商务的信息，请参阅幻灯片自 [定义](../c-about-apps/c-filmstrip-app/c-filmstrip-customizations.md#c_filmstrip_customizations)。

* [媒体墙](../c-about-apps/c-media-wall-app/c-media-wall-app.md#c_media_wall_app)。 有关如何在媒体墙中使用UGC商务的信息，请参阅 [媒体墙自定义](../c-about-apps/c-media-wall-app/r-media-wall-customizations.md#r_media_wall_customizations)。

* [马赛克](../c-about-apps/c-mosaic-app/c-mosaic-app.md#c_mosaic_app)。 有关如何在马赛克中使用UGC商务的信息，请参阅马赛克 [自定义](../c-about-apps/c-mosaic-app/c-mosaic-customizations.md#c_mosaic_customizations)。

## 概述：如何使用UGC商务行动动员按钮 {#section_s2d_tln_n1b}

1. 使用行动动员按钮创建应用程序。 请参 [阅向应用程序添加行动动员按钮](/help/using/c-features-livefyre/c-call-to-action-button.md#task_36190DD1C8204C7793CB7EEA379C2155)。
1. 将您的产品目录添加到Livefyre。 可以通过以下两种方式之一导入内容：

   * [使用AEM Commerce将产品导入Livefyre](https://helpx.adobe.com/experience-manager/6-4/sites/administering/using/livefyre.html) 。
   * [如果不使用AEM Commerce](/help/using/c-features-livefyre/c-ugc-commerce.md) ，请将产品上传到Livefyre。

1. 将产品与内容关联。 您可以通过以下四种方式之一执行此操作：

   * 从库中。 请参 [阅使用库将产品与内容关联](../c-library/t-associate-products-with-content-using-the-library.md#t_associate_products_with_content_using_the_library)
   * 来自ModQ。 请参阅 [使用ModQ审核内容](/help/using/c-features-livefyre/c-about-moderation/c-modq.md)
   * 从应用程序内容。 请参 [阅向应用程序添加行动动员按钮](/help/using/c-features-livefyre/c-call-to-action-button.md)
   * 来自流。 请参 [阅所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。

## 使用文件上传将产品上传到Livefyre {#section_n1s_4hz_m1b}

上传产品以与“行动动员”按钮一起使用，以添加产品以与内容关联或编辑和删除现有文件。

>[!NOTE]
>
>将包含现有文件的文件上传到文件夹后，将删除该文件夹中的所有文件，并用新文件覆盖它们。

1. 导航到 **[!UICONTROL Network Settings > Products.]**
1. 创建或 **[!UICONTROL Product Folder]** 使用现有的 **[!UICONTROL Product Folder]**。

1. 单击以 **[!UICONTROL Product Folder]** 选择它。
1. Click the **[!UICONTROL Upload Products]** button.
1. 以下格式之一上传产品文件：

   * Google产品文件格式
   * Livefyre格式（见下文）
   上传标准格式的JSON文件。 您可以下载模板以查看标准格式的示例。 以下是模板中一个产品系列的示例。 它按顺序排列 `{"key": "value", "key": "value"}, {"key": "value", "key": "value"}`:

   ```
   {"id": "1", "title": "Flex RN 2017", "isFolder": false, "description": "Flex RN 2017", "price": "$85", "sku": "sku11111", "summary": "This brand is a member of the Sustainable Apparel Coalition", "features": "Cushioning: Lightweight, flexible response", "url": "www.shopping.com/shoes-flex-rn-2017/product/9", "attributes": [{"type": "color", "value": "blue"}
   ```

   下表说明了上传产品所需的键和值对：

## 产品目录上传标准格式的键／值对

| 键值 | 类型 | 描述 |
|--- |--- |--- |
| ID | 字符串 | 产品的唯一ID。 |
| 嵌入 | 对象 | Image attachment `0embed $ref: '../partials/schemas.yaml#/oEmbed'` |
| title | 字符串 | 产品标题。 |
| isFolder | 布尔值 | 如果为true，则产品会被视为文件夹（例如，mens、womens等）。 |
| parentId | 字符串 | 定义产品所在的文件夹。 |
| 描述 | 字符串 | 产品说明。 |
| 价格 | 字符串 | 产品的价值（以美元为单位）。 例如，'23.36'。 |
| sku | 字符串 | 产品的库存单位(SKU)。 |
| url | 字符串 | 链接到产品页面。 |
| enabled | 布尔值 | 值为True表示产品处于活动状态。 |
| 属性 | 数组 | 定义产品的类型和值（例如颜色、大小等）。 这是一组对象。</br>**** 属性：类 </br>型 </br>类型：</br>StringDescription:颜色，大小 </br>值 </br>类型：字符串 </br>描述：绿色、XS |
| 标记 | 数组 | 定义内容类别（例如汽车、鞋等）的标签。 这是字符串的数组。 |

## ModQ {#section_os1_v4t_n1b}

您可以根据您现有的仲裁工作流程，在ModQ中将产品目录中的内容与产品相关联。 有关如何将UGC Commerce与ModQ一起使用的信息，请参 [阅使用ModQ审核内容](/help/using/c-features-livefyre/c-about-moderation/c-moderate-content-using-app-content.md)。

## 流 {#section_qtj_v4t_n1b}

您可以使用流规则将产品自动关联到内容，然后将内容自动发布到应用程序，将其保存到库中，或使用ModQ审核它。 有关如何将UGC商务与流规则结合使用的详细信息，请参 [阅所有流规则的流规则选项](../c-streams/c-stream-rule-options-for-all-stream-rules.md#c_stream_rule_options_for_all_stream_rules)。
