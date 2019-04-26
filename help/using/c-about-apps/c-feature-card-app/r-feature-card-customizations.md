---
description: 更改地图应用程序的大小、宽度和交互选项。
seo-description: 更改地图应用程序的大小、宽度和交互选项。
seo-title: 功能卡自定义
solution: Experience Manager
title: 功能卡自定义
uuid: dd43c076-027f-42c8-be2 e-7d863 d4 e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# 功能卡自定义{#feature-card-customizations}

更改地图应用程序的大小、宽度和交互选项。

<!-- 
r_feature_card_customization.dita
 -->

功能卡应用程序只包括标准自定义：** [!UICONTROL Theme]**、品牌颜色、字体系列和字体大小。

您可以使用以下方法自定义功能卡：

* **[!UICONTROL Style]** 以及所有应用程序 **[!UICONTROL Config]** 的选项 **[!UICONTROL App Designer]**。有关中所有应用程序的标准 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 选项的详细信息，请参阅自定义应用程序 **[!UICONTROL App Designer]**。

* 集成工具。有关如何使用集成工具自定义应用程序的更多信息，请参阅应用程序集成。
* **[!UICONTROL Call-to-action button]** 您可以使用包含产品目录的“行动动员”按钮将用户定向到产品或您的站点进行进一步操作。

   * **[!UICONTROL Call-to-action button]** 切换切换以显示行动动员按钮。
   * **[!UICONTROL Require rights to display products]** 切换切换以要求内容所有者在为内容显示“行动动员”按钮之前为内容授予权限。

      >[!NOTE]
      >
      >即使未为内容授予权限，内容也会显示，但除非授予内容权限，否则“行动动员”按钮将不会显示内容。

   * **[!UICONTROL Call-to-action header text]** 要显示在内容模态中的行动动员按钮上方的标题中的词。默认措辞是：“购买这些产品：.
   * **[!UICONTROL Call-to-action button text]** 自定义“行动动员”按钮上的文本。默认文本为“立即购买”。
   * **[!UICONTROL Product display options]** 选择是否要显示和 **[!UICONTROL Photo]****[!UICONTROL Product name]** 使用行动动员按钮。
   * **[!UICONTROL Product URL referral tracking]** 切换切换以跟踪从此应用程序到关联产品页面的引用。
   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从应用程序内容到关联产品页面的引用跟踪。

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. 选择此选项可为多个产品页面创建一个应用程序。将特定于产品的UGC用于每个产品页面的应用程序。您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select Product folders]**. 选择用于筛选UGC的顶级产品文件夹。用于 `CTRL/Command + click` 选择多个文件夹。Livefyre使用该文件夹确定该文件夹中要显示在各种页面上的应用程序中的产品。
   * **[!UICONTROL Show related content]**. 切换此操作以显示发布到应用程序的内容，但标记为其他产品ID。在用于应用程序显示的产品特定内容之后，Livefyre会显示其他产品和未与产品关联的内容的内容。Livefyre首先优先使用相同产品ID，然后使用其他产品ID发布到应用程序的内容，然后使用没有产品ID的应用程序发布到应用程序。

