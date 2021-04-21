---
description: 更改Mosaic应用程序的大小、宽度和交互选项。
title: 马赛克自定义
exl-id: 0223a64c-ec33-4e01-85d7-11845c9b8476
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# 马赛克自定义{#mosaic-customizations}

更改Mosaic应用程序的大小、宽度和交互选项。

所有应用程序都使用&#x200B;**[!UICONTROL App Designer]**&#x200B;中的&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;选项。 有关&#x200B;**[!UICONTROL App Designer.]**&#x200B;中所有应用程序的标准&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;选项的详细信息，请参阅自定义应用程序

您可以在App Designer中使用以下其他选项自定义Mosaic:

* **[!UICONTROL Content interaction]**。设置将新内容加载到页面上的样式：

   * **[!UICONTROL Hover Fade]** 当站点访客将鼠标悬停在内容上时，淡入卡片的另一侧。
   * **[!UICONTROL Hover Flip]** 当站点访客将鼠标悬停在内容上时，可翻转到卡的另一侧。
   * **[!UICONTROL Click]** 以在站点访客单击内容上的鼠标时显示卡的另一侧。

* **[!UICONTROL Number of Tiles to Load]**。要载入马赛克中的拼贴数。 这会影响输出显示。 除非您选择与容器宽度相对应的正确拼贴数，否则马赛克将不会显示在网格中。 您可能需要调整这些参数才能正确显示网格。
* **[!UICONTROL Hide social branding when rights granted]** 打开此图标，在授予某条内容的权限时删除原始社交媒体网络(Twitter或Instagram)的徽标。

* **[!UICONTROL Call-to-action button]** 您可以将行动动员按钮与产品目录结合使用，将用户引导到产品或您的站点以进一步操作。

   * **[!UICONTROL Call-to-action button]** 切换到可显示行动动员按钮。

   * **[!UICONTROL Require rights to display products]** 切换为，以要求内容所有者在内容显示行动动员按钮之前已授予内容权限。

      >[!NOTE]
      >
      >即使未授予内容权限，内容也会显示，但除非授予内容权限，否则行动动员按钮不会与内容一起显示。

   * **[!UICONTROL Show call-to-action in tile]**。选择是否在幻灯片拼贴上显示行动动员按钮，而不是仅在站点访客单击卡并在较大窗口中打开内容时显示行动动员按钮。
   * **[!UICONTROL Call-to-action indication text]** 要显示的文本，提示用户单击卡以打开行动动员模式。

   * **[!UICONTROL Call-to-action header text]** 内容模式中行动动员按钮上方标题中显示的词语。默认措辞为“Shop these products：”。

   * **[!UICONTROL Call-to-action button text]** 自定义行动动员按钮上的文本。默认文本为“立即购买”。

   * **[!UICONTROL Product display options]** 选择是否要使用 **[!UICONTROL Photo]** 行动 **[!UICONTROL Product name]** 动员按钮显示和。

   * **[!UICONTROL Product URL referral tracking]** 切换到，以跟踪从此应用程序到关联产品页面的引用。

   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从您的App内容到关联产品页面的引用跟踪。

* **[!UICONTROL Product page filter]**。

   * **[!UICONTROL Filter UGC by Product ID]**。选择此选项可为多个产品页面创建一个应用程序。 将每个产品页面的特定于产品的UGC过滤到应用程序。 您可以选择一个或多个文件夹以将特定收藏集关联到应用程序。
   * **[!UICONTROL Select Product folders]**。选择要用于筛选UGC的顶级产品文件夹。 使用CTRL/Command +单击可选择多个文件夹。 Livefyre使用该文件夹确定该文件夹中要在不同页面上的应用程序中显示的产品。
   * **[!UICONTROL Show related content]**。切换此选项可显示已发布到应用程序但用其他产品ID标记的内容。 显示应用程序的特定产品内容后，Livefyre将显示其他产品的内容以及与某个产品无关的内容。 Livefyre首先使用相同的产品ID对内容进行优先级排序，然后使用其他产品ID发布到应用程序的内容，然后发布到没有产品ID的应用程序的内容。

有关如何使用Livefyre.js自定义Mosaic的详细信息，请参阅[Mosaic选项](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。
