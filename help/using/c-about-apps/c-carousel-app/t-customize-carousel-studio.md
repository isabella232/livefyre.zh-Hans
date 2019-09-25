---
description: 更改传送应用程序的大小、宽度和交互选项。
seo-description: 更改传送应用程序的大小、宽度和交互选项。
seo-title: 使用Studio自定义传送
solution: Experience Manager
title: 使用Studio自定义传送
uuid: 24f080fc-37bf-40d4-8c1a-a502ee8ac978
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# 使用Studio自定义传送{#customize-a-carousel-using-studio}

更改传送应用程序的大小、宽度和交互选项。

所有应用程序 **[!UICONTROL Style]** 都使用 **[!UICONTROL Config]** 和中的选项 **[!UICONTROL App Designer]**。 有关中所有应用程序的标准和选项的详细 **[!UICONTROL Style]** 信息， **[!UICONTROL Config]** 请参阅自定义应用程序 **[!UICONTROL App Designer]**。

您可以使用应用程序设计器中的以下其他选项自定义传送：

* **[!UICONTROL Max Number of Items]**

   设置要在传送中显示的项目数。 默认值为 50。

* **[!UICONTROL Orientation]**

   **[!UICONTROL Responsive]**. 仅适用于计算机屏幕

   * 如果内容大于600像素，则水平显示
   * 如果内容小于600像素，则垂直显示
   * **垂直。** 适用于计算机屏幕或移动设备。 在移动设备中，卡会缩小以适合屏幕大小。

* **[!UICONTROL Call-to-action button]** 您可以将行动动员按钮与产品目录一起使用，以将用户定向到产品或您的站点以进一步执行操作。

   * **[!UICONTROL Call-to-action button]** 切换至开启，显示行动动员按钮。
   * **[!UICONTROL Require rights to display products]** 切换为打开，以要求内容所有者已授予内容权限，然后才会显示内容的行动动员按钮。
   >[!NOTE]
   >
   >即使未授予内容权限，内容也会显示，但除非授予内容权限，否则行动动员按钮将不显示内容。

   * **[!UICONTROL Show call-to-action in tile]**. 选择是否在拼贴上显示行动动员按钮，而不是仅在站点访问者单击卡并在较大窗口中打开内容时显示行动动员按钮。
   * **[!UICONTROL Call-to-action indication text]** 要显示的文本，提示用户单击卡以打开行动动员模式。
   * **[!UICONTROL Call-to-action header text]** 内容模式中行动动员按钮上方标题中显示的词语。 默认文本为“Shop these products:”。
   * **[!UICONTROL Call-to-action button text]** 要在内容模式的“行动动员”按钮中显示的词。 默认文本为“立即购买：”。
   * **[!UICONTROL Product display options]** 选择是否要显示 **[!UICONTROL Photo]** 和具 **[!UICONTROL Product name]** 有行动动员按钮的图标。
   >[!NOTE]
   >
   >“照片”和“产品”名称按钮在启用时均突出显示为蓝色。

   * **[!UICONTROL Product URL referral tracking]** 切换至开启以跟踪从此应用程序到关联产品页面的引用。
   * **[!UICONTROL Referral tracking key-value pairs]** 添加参数以进一步指定从应用程序内容到关联产品页面的引用跟踪。



* **[!UICONTROL Embed App in multiple pages]**

   * **[!UICONTROL Filter UGC by Product ID]**. 选择此选项可为多个产品页面创建一个应用程序。 将特定于产品的UGC过滤为每个产品页面的应用程序。 您可以选择一个或多个文件夹，将特定集合关联到应用程序。
   * **[!UICONTROL Select Product folders]**. 选择要用于筛选UGC的顶级产品文件夹。 使用CTRL/Command +单击可选择多个文件夹。 Livefyre使用该文件夹确定该文件夹中要在不同页面上的应用程序中显示的产品。
   * **[!UICONTROL Show related content]**. 切换此选项可显示已发布到应用程序但使用其他产品ID标记的内容。 显示应用程序的特定产品内容后，Livefyre将显示其他产品的内容以及与某个产品无关的内容。 Livefyre首先使用相同的产品ID优先安排内容的优先级，然后使用其他产品ID发布到应用程序的内容，然后发布到没有产品ID的应用程序的内容。
