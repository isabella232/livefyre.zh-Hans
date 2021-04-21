---
title: 幻灯片自定义
description: 幻灯片自定义
exl-id: 2765699f-7adc-4b17-acfb-ef594ff65e89
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 幻灯片自定义{#filmstrip-customizations}

所有应用程序都使用&#x200B;**[!UICONTROL App Designer]**&#x200B;中的&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;选项。 有关&#x200B;**[!UICONTROL App Designer.]**&#x200B;中所有应用程序的标准&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;选项的详细信息，请参阅自定义应用程序

您可以在应用程序设计器中使用以下其他选项自定义幻灯片：

* **[!UICONTROL Content fit]**。选择&#x200B;**[!UICONTROL crop]**&#x200B;以裁切内容以填充卡，或选择&#x200B;**[!UICONTROL Aspect Ratio]**&#x200B;以在卡中显示整个图像，无论是否填充整个卡。
* **[!UICONTROL Tile Size]**。输入拼贴的大小（以像素为单位）。
* **[!UICONTROL Show Notifications]**。选择是否在新内容流入幻灯片应用程序时显示通知。
* **[!UICONTROL Require rights]**。启用此选项可仅显示权限请求状态为“已授予”的内容。
* **[!UICONTROL Hide social branding when rights granted]** 打开此图标，在授予某条内容的权限时删除原始社交媒体网络(Twitter或Instagram)的徽标。
* **[!UICONTROL Call-to-action button]** 您可以将行动动员按钮与产品目录结合使用，将用户引导到产品或您的站点以进一步操作。

   * **[!UICONTROL Call-to-action button]** 切换到可显示行动动员按钮。
   * **[!UICONTROL Require rights to display products]** 切换为，以要求内容所有者在内容显示行动动员按钮之前已授予内容权限。

      >[!NOTE]
      >
      >即使未授予内容权限，内容也会显示，但除非授予内容权限，否则行动动员按钮不会与内容一起显示。

   * **[!UICONTROL Show call-to-action in tile]**。选择是否在幻灯片拼贴上显示行动动员按钮，而不是仅在站点访客单击卡并在较大窗口中打开内容时显示行动动员按钮。
   * **[!UICONTROL Call-to-action indication text]** 要显示的文本，提示用户单击卡以打开行动动员模式。
   * **[!UICONTROL Call-to-action header text]** 内容模式中行动动员按钮上方标题中显示的词语。默认文本为“Shop these products：”。
   * **[!UICONTROL Call-to-action button text]** 要在内容模式的行动动员按钮中显示的词。默认文本为“立即购买：”。
   * **[!UICONTROL Product display options]** 选择是否要显示 **[!UICONTROL Photo]** 带 **[!UICONTROL Product name]** 行动动员按钮的和。

      >[!NOTE]
      >
      >“照片”和“产品”名称按钮在启用时均突出显示蓝色。

   * **[!UICONTROL Product URL referral tracking]** 切换到，以跟踪从此应用程序到关联产品页面的引用。
   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从您的App内容到关联产品页面的引用跟踪。

* **[!UICONTROL Embed App in multiple pages]**。

   * **[!UICONTROL Filter UGC by Product ID]**。选择此选项可为多个产品页面创建一个应用程序。 将每个产品页面的特定于产品的UGC过滤到应用程序。 您可以选择一个或多个文件夹以将特定收藏集关联到应用程序。
   * **[!UICONTROL Select product folders]**。选择要用于筛选UGC的顶级产品文件夹。 使用CTRL/Command +单击可选择多个文件夹。 Livefyre使用该文件夹确定该文件夹中要在不同页面上的应用程序中显示的产品。
   * **[!UICONTROL Show related content]**。切换此选项可显示已发布到应用程序但用其他产品ID标记的内容。 显示应用程序的特定产品内容后，Livefyre将显示其他产品的内容以及与某个产品无关的内容。 Livefyre首先使用相同的产品ID对内容进行优先级排序，然后使用其他产品ID发布到应用程序的内容，然后发布到没有产品ID的应用程序的内容。

有关如何使用Livefyre.js自定义幻灯片的详细信息，请参阅[幻灯片选项](/help/implementation/c-getting-started/c-implementation-process/c-using-livefyre.js-to-create-customize-and-use-apps-on-your-site.md)。
