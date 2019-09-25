---
description: 更改Mosaic应用程序的大小、宽度和交互选项。
seo-description: 更改Mosaic应用程序的大小、宽度和交互选项。
seo-title: 马赛克自定义
solution: Experience Manager
title: 马赛克自定义
uuid: 4e226d68-f517-4922-bc25-655d524d7d52
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 马赛克自定义{#mosaic-customizations}

更改Mosaic应用程序的大小、宽度和交互选项。

所有应用程序 **[!UICONTROL Style]** 都使用 **[!UICONTROL Config]** 和中的选项 **[!UICONTROL App Designer]**。 有关Adobe cloud中所有应用程序的标准和选 **[!UICONTROL Style]** 项的详 **[!UICONTROL Config]** 细信息，请参阅自定义应用程序 **[!UICONTROL App Designer.]**

您可以在App Designer中使用以下其他选项自定义Mosaic:

* **[!UICONTROL Content interaction]**. 设置将新内容加载到页面时使用的样式：

   * **[!UICONTROL Hover Fade]** 当站点访问者将鼠标悬停在内容上时，淡入淡出卡的另一侧。
   * **[!UICONTROL Hover Flip]** 当站点访问者将鼠标悬停在内容上时，可翻转到卡的另一侧。
   * **[!UICONTROL Click]** 当站点访问者在内容上单击其鼠标时，显示卡的另一侧。

* **[!UICONTROL Number of Tiles to Load]**. 要加载到马赛克中的拼贴数。 这会影响输出显示。 除非您选择与容器宽度相对应的正确拼贴数，否则马赛克将不会显示在网格中。 您可能需要调整这些参数，以使网格正确显示。
* **[!UICONTROL Hide social branding when rights granted]** 打开此按钮可在授予某条内容的权限时删除源社交媒体网络（Twitter或Instagram）的徽标。

* **[!UICONTROL Call-to-action button]** 您可以将行动动员按钮与产品目录一起使用，以将用户定向到产品或您的站点以进一步执行操作。

   * **[!UICONTROL Call-to-action button]** 切换至开启以显示行动动员按钮。

   * **[!UICONTROL Require rights to display products]** 切换为打开，以要求内容所有者已授予内容权限，然后才会为内容显示行动动员按钮。

      >[!NOTE]
      >
      >即使未授予内容权限，内容也会显示，但除非授予内容权限，否则行动动员按钮将不显示内容。

   * **[!UICONTROL Show call-to-action in tile]**. 选择是否在“幻灯片”拼贴上显示行动动员按钮，而不是仅在站点访问者单击卡并在较大窗口中打开内容时显示行动动员按钮。
   * **[!UICONTROL Call-to-action indication text]** 要显示的文本，提示用户单击卡以打开行动动员模式。

   * **[!UICONTROL Call-to-action header text]** 内容模式中行动动员按钮上方标题中显示的词语。 默认措辞为“Shop these products:”。

   * **[!UICONTROL Call-to-action button text]** 自定义“行动动员”按钮上的文本。 默认文本为“立即购买”。

   * **[!UICONTROL Product display options]** 选择是否要显示 **[!UICONTROL Photo]** 和具 **[!UICONTROL Product name]** 有行动动员按钮的图标。

   * **[!UICONTROL Product URL referral tracking]** 切换至开启以跟踪从此应用程序到关联产品页面的引用。

   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从应用程序内容到关联产品页面的引用跟踪。

* **[!UICONTROL Product page filter]**.

   * **[!UICONTROL Filter UGC by Product ID]**. 选择此选项可为多个产品页面创建一个应用程序。 将特定于产品的UGC过滤为每个产品页面的应用程序。 您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select Product folders]**. 选择要用于筛选UGC的顶级产品文件夹。 使用CTRL/Command +单击可选择多个文件夹。 Livefyre使用该文件夹确定该文件夹中要在不同页面上的应用程序中显示的产品。
   * **[!UICONTROL Show related content]**. 切换此选项可显示已发布到应用程序但使用其他产品ID标记的内容。 显示应用程序的特定产品内容后，Livefyre将显示其他产品的内容以及与某个产品无关的内容。 Livefyre首先使用相同的产品ID优先安排内容的优先级，然后使用其他产品ID发布到应用程序的内容，然后发布到没有产品ID的应用程序的内容。

有关如 [何使用Livefyre](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md) .js自定义Mosaic的更多信息，请参阅Mosaic选项。
