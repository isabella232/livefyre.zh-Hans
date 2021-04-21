---
description: 更改传送应用程序的大小、宽度和交互选项。
title: 使用Studio自定义传送
exl-id: f6f681ac-c601-40b9-9e99-bf5495f505f8
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# 使用Studio{#customize-a-carousel-using-studio}自定义传送

更改传送应用程序的大小、宽度和交互选项。

所有应用程序都使用&#x200B;**[!UICONTROL App Designer]**&#x200B;中的&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;选项。 有关&#x200B;**[!UICONTROL App Designer]**&#x200B;中所有应用程序的标准&#x200B;**[!UICONTROL Style]**&#x200B;和&#x200B;**[!UICONTROL Config]**&#x200B;选项的详细信息，请参阅自定义应用程序。

您可以使用应用程序设计器中的以下其他选项自定义传送：

* **[!UICONTROL Max Number of Items]**

   设置要在传送中显示的项目数。 默认值为 50。

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**。仅适用于计算机屏幕

   * 如果内容大于600像素，则水平显示
   * 如果内容小于600像素，则垂直显示
   * **垂直。** 适用于计算机屏幕或移动设备。在移动设备中，卡会缩小以适合屏幕大小。

* **[!UICONTROL Call-to-action button]** 您可以将行动动员按钮与产品目录结合使用，将用户引导到产品或您的站点以进一步操作。

   * **[!UICONTROL Call-to-action button]** 切换到可显示行动动员按钮。
   * **[!UICONTROL Require rights to display products]** 切换为，以要求内容所有者在内容显示行动动员按钮之前已授予内容权限。

   >[!NOTE]
   >
   >即使未授予内容权限，内容也会显示，但除非授予内容权限，否则行动动员按钮不会与内容一起显示。

   * **[!UICONTROL Show call-to-action in tile]**。选择是否在拼贴上显示行动动员按钮，而不是仅在站点访客单击卡并在较大窗口中打开内容时显示行动动员按钮。
   * **[!UICONTROL Call-to-action indication text]** 要显示的文本，提示用户单击卡以打开行动动员模式。
   * **[!UICONTROL Call-to-action header text]** 内容模式中行动动员按钮上方标题中显示的词语。默认文本为“Shop these products：”。
   * **[!UICONTROL Call-to-action button text]** 要在内容模式的行动动员按钮中显示的词。默认文本为“立即购买：”。
   * **[!UICONTROL Product display options]** 选择是否要使用 **[!UICONTROL Photo]** 行动 **[!UICONTROL Product name]** 动员按钮显示和。

   >[!NOTE]
   >
   >“照片”和“产品”名称按钮在启用时均突出显示蓝色。

   * **[!UICONTROL Product URL referral tracking]** 切换到，以跟踪从此应用程序到关联产品页面的引用。
   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从您的App内容到关联产品页面的引用跟踪。



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**。选择此选项可为多个产品页面创建一个应用程序。 将每个产品页面的特定于产品的UGC过滤到应用程序。 您可以选择一个或多个文件夹以将特定收藏集关联到应用程序。
   * **[!UICONTROL Select Product folders]**。选择要用于筛选UGC的顶级产品文件夹。 使用CTRL/Command +单击可选择多个文件夹。 Livefyre使用该文件夹确定该文件夹中要在不同页面上的应用程序中显示的产品。
   * **[!UICONTROL Show related content]**。切换此选项可显示已发布到应用程序但用其他产品ID标记的内容。 显示应用程序的特定产品内容后，Livefyre将显示其他产品的内容以及与某个产品无关的内容。 Livefyre首先使用相同的产品ID对内容进行优先级排序，然后使用其他产品ID发布到应用程序的内容，然后发布到没有产品ID的应用程序的内容。
