---
description: 更改“映射”应用程序的大小、宽度和交互选项。
seo-description: 更改“映射”应用程序的大小、宽度和交互选项。
seo-title: 功能卡自定义
solution: Experience Manager
title: 功能卡自定义
uuid: dd43c076-027f-42c8-be2e-7d863d4e3976
translation-type: tm+mt
source-git-commit: a014b5cd618672934843f1adf20d6b2cc504e2d8

---


# 功能卡自定义{#feature-card-customizations}

更改“映射”应用程序的大小、宽度和交互选项。

<!-- 
r_feature_card_customization.dita
 -->

功能卡应用程序仅包含标准自定义：** [!UICONTROL Theme]**、品牌颜色、字体系列和字体大小。

您可以使用以下方式自定义功能卡：

* **[!UICONTROL Style]** 和中 **[!UICONTROL Config]** 所有应用程序的选项 **[!UICONTROL App Designer]**。 有关中所有应用程序的标准和选项的详细 **[!UICONTROL Style]** 信息， **[!UICONTROL Config]** 请参阅自定义应用程序 **[!UICONTROL App Designer]**。

* 集成工具。 有关如何使用集成工具自定义应用程序的更多信息，请参阅应用程序集成。
* **[!UICONTROL Call-to-action button]** 您可以将行动动员按钮与产品目录一起使用，以将用户定向到产品或您的站点以进一步执行操作。

   * **[!UICONTROL Call-to-action button]** 切换至开启以显示行动动员按钮。
   * **[!UICONTROL Require rights to display products]** 切换为打开，以要求内容所有者已授予内容权限，然后才会为内容显示行动动员按钮。

      >[!NOTE]
      >
      >即使未授予内容权限，内容也会显示，但除非授予内容权限，否则行动动员按钮将不显示内容。

   * **[!UICONTROL Call-to-action header text]** 内容模式中行动动员按钮上方标题中显示的词语。 默认措辞为“Shop these products:”。
   * **[!UICONTROL Call-to-action button text]** 自定义“行动动员”按钮上的文本。 默认文本为“立即购买”。
   * **[!UICONTROL Product display options]** 选择是否要显示 **[!UICONTROL Photo]** 和具 **[!UICONTROL Product name]** 有行动动员按钮的图标。
   * **[!UICONTROL Product URL referral tracking]** 切换至开启以跟踪从此应用程序到关联产品页面的引用。
   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从应用程序内容到关联产品页面的引用跟踪。

* **[!UICONTROL Product page filter]**

   * **[!UICONTROL Filter UGC by Product ID]**. 选择此选项可为多个产品页面创建一个应用程序。 将特定于产品的UGC过滤为每个产品页面的应用程序。 您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select Product folders]**. 选择要用于筛选UGC的顶级产品文件夹。 使用 `CTRL/Command + click` 可选择多个文件夹。 Livefyre使用该文件夹确定该文件夹中要在不同页面上的应用程序中显示的产品。
   * **[!UICONTROL Show related content]**. 切换此选项可显示已发布到应用程序但使用其他产品ID标记的内容。 显示应用程序的特定产品内容后，Livefyre将显示其他产品的内容以及与某个产品无关的内容。 Livefyre首先使用相同的产品ID优先安排内容的优先级，然后使用其他产品ID发布到应用程序的内容，然后发布到没有产品ID的应用程序的内容。

