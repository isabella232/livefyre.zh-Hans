---
description: 更改Mosaic应用程序的大小、宽度和交互选项。
seo-description: 更改Mosaic应用程序的大小、宽度和交互选项。
seo-title: 马赛克自定义
solution: Experience Manager
title: 马赛克自定义
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# 马赛克自定义{#mosaic-customizations}

更改Mosaic应用程序的大小、宽度和交互选项。

所有应用程序都使用&#x200B;**[!UICONTROL App Designer]**&#x200B;中的&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;选项。 有关&#x200B;**[!UICONTROL App Designer.]**&#x200B;中所有应用程序的标准&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;选项的详细信息，请参阅自定义应用程序。

您可以在App Designer中使用以下其他选项自定义Mosaic:

* **[!UICONTROL Content interaction]**。设置将新内容加载到页面上的样式：

   * **[!UICONTROL Hover Fade]** 当站点访客将鼠标悬停在内容上时，淡入卡片的另一侧。
   * **[!UICONTROL Hover Flip]** 当站点访客将鼠标悬停在内容上时，可翻转到卡的另一侧。
   * **[!UICONTROL Click]** 当站点访客在内容上单击其鼠标时，显示卡的另一侧。

* **[!UICONTROL Number of Tiles to Load]**。要加载到马赛克中的拼贴数。 这会影响输出显示。 除非您选择与容器宽度对应的正确拼贴数，否则马赛克将不会显示在网格中。 您可能需要调整这些参数，才能正确显示网格。
* **[!UICONTROL Hide social branding when rights granted]** 打开此图标，在授予某条内容的权限时删除原始社交媒体网络（Twitter或Instagram）的徽标。

* **[!UICONTROL Call-to-action button]** 您可以将行动动员按钮与产品目录结合使用，将用户引导到产品或您的站点以执行进一步操作。

   * **[!UICONTROL Call-to-action button]** 切换为开，显示行动动员按钮。

   * **[!UICONTROL Require rights to display products]** 切换为“打开”，要求内容所有者在为内容显示行动动员按钮之前已授予内容权限。

      >[!NOTE]
      >
      >即使未授予内容权限，内容也会显示，但“行动动员”按钮不会随内容一起显示，除非授予了内容权限。

   * **[!UICONTROL Show call-to-action in tile]**。选择是否在“幻灯片”拼贴上显示行动动员按钮，而不是仅在站点访客单击卡并在较大窗口中打开内容时显示行动动员按钮。
   * **[!UICONTROL Call-to-action indication text]** 显示的文本，提示用户单击卡以打开行动动员模式。

   * **[!UICONTROL Call-to-action header text]** 内容模式中行动动员按钮上方标题中显示的词。默认措辞为“Shop these products:”。

   * **[!UICONTROL Call-to-action button text]** 自定义“行动动员”按钮上的文本。默认文本为“立即购买”。

   * **[!UICONTROL Product display options]** 选择是否要显示 **[!UICONTROL Photo]** 带 **[!UICONTROL Product name]** 有行动动员按钮的和。

   * **[!UICONTROL Product URL referral tracking]** 切换为开启，以跟踪从此应用程序到关联产品页面的引用。

   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从您的App内容到关联产品页面的引用跟踪。

* **[!UICONTROL Product page filter]**。

   * **[!UICONTROL Filter UGC by Product ID]**。选择此选项可为多个产品页面创建一个应用程序。 将每个产品页面的产品特定UGC筛选为应用程序。 您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select Product folders]**。选择要用于筛选UGC的顶级产品文件夹。 使用CTRL/Command并单击可选择多个文件夹。 Livefyre使用该文件夹确定该文件夹中的哪些产品将在不同页面上的应用程序中显示。
   * **[!UICONTROL Show related content]**。切换此选项可显示已发布到应用程序但使用其他产品ID标记的内容。 显示应用程序的特定产品内容后，Livefyre将显示其他产品的内容以及与某个产品无关的内容。 Livefyre首先使用相同的产品ID排定内容的优先级，然后使用其他产品ID发布到应用程序的内容，然后使用没有产品ID发布到应用程序的内容。

有关如何使用Livefyre.js自定义Mosaic的更多信息，请参阅[Mosaic选项](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。
