---
description: 更改Mosaic应用程序的大小、宽度和交互选项。
seo-description: 更改Mosaic应用程序的大小、宽度和交互选项。
seo-title: 马赛克自定义
solution: Experience Manager
title: 马赛克自定义
uuid: e226d68-f517-4922-bc25-655d524 d7 d52 d
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 马赛克自定义{#mosaic-customizations}

更改Mosaic应用程序的大小、宽度和交互选项。

所有应用程序使用 **[!UICONTROL Style]** 和 **[!UICONTROL Config]** 选项 **[!UICONTROL App Designer]**。有关 **[!UICONTROL Style]****[!UICONTROL Config]** 在 **[!UICONTROL App Designer.]**

您可以使用App Designer中的以下其他选项自定义马赛克：

* **[!UICONTROL Content interaction]**. 设置将新内容加载到页面的样式：

   * **[!UICONTROL Hover Fade]** 当站点访问者将鼠标悬停在内容上时，淡入卡的另一侧。
   * **[!UICONTROL Hover Flip]** 当站点访问者将鼠标悬停在内容上时，翻转到卡的另一面。
   * **[!UICONTROL Click]** 当站点访问者单击内容时显示卡的另一面。

* **[!UICONTROL Number of Tiles to Load]**. 以马赛克形式加载的拼贴数。这会影响输出显示。除非您选择符合容器宽度的拼贴数量，否则Mosaic不会显示在网格中。您可能需要调整这些网格以正确显示网格。
* **[!UICONTROL Hide social branding when rights granted]** 在为某一内容授予权限时，切换开启以删除原始社交媒体网络(Twitter或Instagram)的标志。

* **[!UICONTROL Call-to-action button]** 您可以使用包含产品目录的“行动动员”按钮将用户定向到产品或您的站点进行进一步操作。

   * **[!UICONTROL Call-to-action button]** 切换切换以显示行动动员按钮。

   * **[!UICONTROL Require rights to display products]** 切换切换以要求内容所有者在为内容显示“行动动员”按钮之前为内容授予权限。

      >[!NOTE]
      >
      >即使未为内容授予权限，内容也会显示，但除非授予内容权限，否则“行动动员”按钮将不会显示内容。

   * **[!UICONTROL Show call-to-action in tile]**. 选择在站点访问者单击卡并在较大窗口中打开内容时，是否显示“幻灯片”拼贴上的行动号召按钮而不是显示行动动员按钮。
   * **[!UICONTROL Call-to-action indication text]** 要显示的文本，提示用户单击卡以打开行动动员模式。

   * **[!UICONTROL Call-to-action header text]** 要显示在内容模态中的行动动员按钮上方的标题中的词。默认措辞是：“购买这些产品：.

   * **[!UICONTROL Call-to-action button text]** 自定义“行动动员”按钮上的文本。默认文本为“立即购买”。

   * **[!UICONTROL Product display options]** 选择是否要显示和 **[!UICONTROL Photo]****[!UICONTROL Product name]** 使用行动动员按钮。

   * **[!UICONTROL Product URL referral tracking]** 切换切换以跟踪从此应用程序到关联产品页面的引用。

   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从应用程序内容到关联产品页面的引用跟踪。

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. 选择此选项可为多个产品页面创建一个应用程序。将特定于产品的UGC用于每个产品页面的应用程序。您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select Product folders]**. 选择用于筛选UGC的顶级产品文件夹。使用CTRL/Command+单击可选择多个文件夹。Livefyre使用该文件夹确定该文件夹中要显示在各种页面上的应用程序中的产品。
   * **[!UICONTROL Show related content]**. 切换此操作以显示发布到应用程序的内容，但标记为其他产品ID。在用于应用程序显示的产品特定内容之后，Livefyre会显示其他产品和未与产品关联的内容的内容。Livefyre首先优先使用相同产品ID，然后使用其他产品ID发布到应用程序的内容，然后使用没有产品ID的应用程序发布到应用程序。

有关如何使用Livefyre. js自定义Mosaic的更多信息，请参阅 [Mosaic选项](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) 。
